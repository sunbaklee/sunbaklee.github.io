---
layout: post
published: true
title:  "리액트 레이아웃 기초"
date: 2023-09-15
desc: "Quick test on writing code snippets in a blog post"
keywords: "React,website,blog,first"
categories: [React]
tags: [sunhak]
icon: icon-html
---

## <b>리액트 레이아웃 기초</b>
기존 html, css로 짜거 웹페이지를 만드는 것과 비슷하지만 html 대신 JSX를 사용

<hr>

> ## <b>리액트프로젝트의 App.js</b>

App.js가 메인페이지
이곳에 코드를 짜면 된다
``` javascript
import './App.css';

function App(){
  return (
    <div className="App">
      //여기에 코드
    </div>
  )
}
```

> ## <b>상단바 제작해보기</b>

그냥 태그 넣으면 된다
```javascript
(App.js)

function App() {
  return (
    <div className="App">
      <header className="App-nav">
        <h4>앱바</h4>
      </header>
    </div>
  );
}
```
css 파일은 App.js가 있는 파일에 App.css에 넣으면 된다.
```javascript
(App.css)

.black-nav {
  background : black;
  width : 100%;
  display : flex;
  color : white;
  padding : 20px;
}
```

>## <b>JSX 문법 1.className 사용하기</b>

class명을 넣을때 class=""가 아니라 className=""사용 (App.js에 짜는 건 html이 아니고 JSX이기 때문)

원래 리액트에서는 div 만들떄 
React.createElement('div', null) 
이렇게 만드는데 쉽게 짜기 위해 JSX사용

근데 JSX는 일종의 자바스크립트라서 
자바스크립트에서 사용하는 예약어인 class라는 키워드를 막 사용하시면 안된다.
그래서 class=" " 넣고 싶으면 className이라고 써야한다.

>## <b>JSX 문법 2.변수를 사용할때 중괄호{}</b>

그냥 자바스크립트라면 document.getElementById().innerHTML = ?? 이런식으로 사용하지만
```javascript
function App(){

  var data = 'Red';
  return (
    <div className="App">
      <div className="black-nav">
        <div className={data}>,Blue, Green</div>
      </div>
    </div>
  )
}
```
이런식으로 사용가능하다<br>
href, id,className등 여러가지 hmtl속성에 사용가능
<br><br>
변수를 html에 넣는 것을 <b>데이터바인딩</b>이라고 한다.

>## <b>JSX 문법 3.html에 style 속성 바로 넣기</b>
기존의 <div style ="color:blue">이런 코드를 넣으려면
style={}를 사용하여 만들어야한다.

```javascript
<div style={ {color : 'blue', fontSize : '30px'} }> test </div>
```
 - {속성명 : '속성값'}이렇게 넣는다
 - 속성명에 대시기호 사용 불가능