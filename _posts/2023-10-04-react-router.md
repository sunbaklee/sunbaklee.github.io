---
layout: post
published: true
title:  "리액트 Router"
date: 2023-10-04
desc: "Quick test on writing code snippets in a blog post"
keywords: "React,website,blog,first"
categories: [React]
tags: [sunhak]
icon: icon-javascript
---

## <b>리액트 Router</b>
<hr>

> ## <b>Routes 컴포넌트</b>

- <Routes>컴포넌트는 여러 Route를 감싸서 그 중 규칙이 일치하는 라우트 단 하나만을 렌더링 시켜주는 역할을 한다.
- <Route>는 path속성에 경로, element속성에는 컴포넌트를 넣어 준다. 여러 라우팅을 매칭하고 싶은 경우 URL 뒤에 *을 사용하면 된다.

<b>예시</b>
```javascript
function App() {
  return (
    <div>
      <h1>이세돌 화이팅</h1>
      <ul>
          <li><a href="/">Home</a></li>
          <li><a href="/topics">Topics</a></li>
          <li><a href="/contact">Topics</a></li>
      </ul>
      <Routes>
          <Route path="/" element={<Home />}></Route>
          <Route path="/topics" element={<Topics />}></Route>
          <Route path="/contact" element={<Contact />}></Route>
      </Routes>
    </div>
    );
}
```

> ## <b>1. exact</b>

- 정확하게 path가 일치해야 매치해줌
```javascript
          <Route exact path="/" element={<Home />}></Route>
```

> ## <b>2. switch</b>

- exact를 쓰지 않고 사용한 효과 내기 
```javascript
    <Switch>
      <Routes>
          <Route path="/" element={<Home />}></Route>
          <Route path="/topics" element={<Topics />}></Route>
          <Route path="/contact" element={<Contact />}></Route>
      </Routes>
    </Switch>
```
path와 일치하는 컴포넌트 발견시 나머지 컴포넌트를 버림

> ## <b>3. Not found</b>

잘못된 경로로 들어가면 Not found 출력
```javascript
function App() {
  return (
    <div>
      <h1>이세돌 화이팅</h1>
      <ul>
          <li><a href="/">Home</a></li>
          <li><a href="/topics">Topics</a></li>
          <li><a href="/contact">Topics</a></li>
      </ul>
      <Routes>
          <Route path="/" element={<Home />}></Route>
          <Route path="/topics" element={<Topics />}></Route>
          <Route path="/contact" element={<Contact />}></Route>
          <Route path="/">Not found</Route>
      </Routes>
    </div>
    );
}
```

> ## <b>4. Link</b>

페이지 변경없이 리로드
```javascript
function App() {
  return (
    <div>
      <h1>이세돌 화이팅</h1>
      <ul>
          <li><Link to="/">Home</Link></li>
          <li><Link to="/topics">Topics</Link></li>
          <li><Link to="/contact">Topics</Link></li>
      </ul>
      <Routes>
          <Route path="/" element={<Home />}></Route>
          <Route path="/topics" element={<Topics />}></Route>
          <Route path="/contact" element={<Contact />}></Route>
          <Route path="/">Not found</Route>
      </Routes>
    </div> 
    );
}
```

> ## <b>5. Nav Link</b>

사용자가 어디에 있는지 위치 표현이 가능 active가 나옴

```javascript
<li><Link exact to="/">Home</Link></li>
```

> ## <b>6. Nested Routing</b>

중첩 라우팅이란 서브 페이지를 만든다고도 할 수 있는데 해당하는 페이지에서 조금 더 구체적으로 구분을 지어 화면을 교체(표시) 해줄 필요가 있을 때 사용된다. 

> ## <b>7. Parameter</b>

URL 파라미터 문법은 페이지의 주소를 정의할때, 유동적인 값을 전달하기 위한 문법이다

> ## <b>8. useParam</b>

react-router-dom의 useParams hook을 사용해서 컴포넌트에서 전달 받는 URL Parameter를 사용해서 적용해볼 수 있도록한다. 즉, URL 경로에 매개변수를 도입할 수 있게 되는 것이다.

```javascript
import { useParams } from "react-router-dom";

let {id} = useParams();
```
이런식으로 사용시 저 id 값이 사이트에 접속한사람이 입력한 값으로 들어간다
