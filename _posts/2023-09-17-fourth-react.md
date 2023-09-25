---
layout: post
published: true
title:  "리액트 state 공부겸 클리커 만들기"
date: 2023-09-17
desc: "Quick test on writing code snippets in a blog post"
keywords: "React,website,blog,first"
categories: [React]
tags: [sunhak]
icon: icon-javascript
---

## <b>클리커 제작</b>
<hr>

> ## <b>리액트 onclick 사용법</b>

일반 html

```html
<div onclick="자바스크립트">
```
리액트에서는

```javascript
<div onClick={실행할함수}>
```

1. Click이 대문자인거<br>
2. {} 중괄호 사용하는거<br>
3. 그냥 코드가 아니라 함수를 넣어야 잘 동작한다는거<br>

> ## <b>함수란?</b>

```javascript
function test_a(){
    console.log(1)
  }
```
이런거

> ## <b>중요 state 변경방법</b>

```javascript
function App(){
  
  let [ 클릭 ] = useState(0);
  return (
    <h4> 누르세요 <span onClick={ ()=>{ 클릭 = 클릭 + 1 } } >👍</span> { 클릭 }</h4>
  )
}
```
변수에 +1 해주고 싶으면 변수 = 변수+1 해주면 끝<br>
근데 안타깝게도 저건 변수가 아니라 state다.<br>
state는 state변경함수를 써서 state를 변경해야한다. <br>
안그러면 큰일남 (html 재렌더링 안됨) <br><br>

따라서 이렇게 해주어야한다.
```javascript
function App(){
  
  let [ 클릭, 클릭변경 ] = useState(0);
  return (
    <h4> 누르세요 <span onClick={ ()=>{ 클릭변경(클릭 + 1 )} } >👍</span> { 클릭 }</h4>
  )
}
```