---
layout: post
published: true
title:  "리액트 style component"
date: 2023-10-03
desc: "Quick test on writing code snippets in a blog post"
keywords: "React,website,blog,first"
categories: [React]
tags: [sunhak]
icon: icon-javascript
---

## <b>리액트 style component</b>
<hr>

> ## <b>style component란?</b>

<b>기존 돔을 만드는 방식인 css, scss 파일을 밖에 두고, 태그나 id, class이름으로 가져와 쓰지 않고, 동일한 컴포넌트에서 컴포넌트 이름을 쓰듯 스타일을 지정하는 것을 styled-components라고 부른다</b>
<b>css 파일을 밖에 두지 않고, 컴포넌트 내부에 넣기 때문에, css가 전역으로 중첩되지 않도록 만들어주는 장점이 있다.</b>

> ## <b>기초세팅</b>

```javascript
npm install styled-components
```


> ## <b>style component예제</b>

```javascript
import React, { useState } from "react";
import styled from 'styled-components';

function App() {
  const [email, setEmail] = useState("");

  return (
    <ExampleWrap active={email.length}>
      <Button>Button</Button>
      <NewButton color="blue">new Button</NewButton>
    </ExampleWrap>
  );
}

const ExampleWrap = styled.div`
  background: ${({ active }) => {
    if (active) {
      return "white";
    }
    return "#eee";
  }};
  color: black;
`;

const Button = styled.button`
  width: 200px;
  padding: 30px;
`;

// Button 컴포넌트 상속
const NewButton = styled.Button`
  // NewButton 컴포넌트에 color가는 props가 있으면 그 값 사용, 없으면 'red' 사용
  color: ${props => props.color || "red"};
`;

export default App;
```

> ## <b>스타일 상속</b>
- const 컴포넌트명 = styled.스타일컴포넌트명스타일 넣기...문법

> ## <b>스타일에 props 적용</b>

- styled-component를 사용하는 장점 중 하나가 변수에 의해 스타일을 바꿀 수 있다는 점
- 예시도 state에 따른 값 변화 