---
layout: post
published: true
title:  "리액트 div 줄이기"
date: 2023-09-19
desc: "Quick test on writing code snippets in a blog post"
keywords: "React,website,blog,first"
categories: [React]
tags: [sunhak]
icon: icon-javascript
---

## <b>리액트 div 줄이기</b>
<hr>

> ## <b>리액트 html 주의할 점</b>

return () 안에 html 태그를 나란히 적으면 안된다.<br>
return () 태그 안레는 하나로 시작해서 하나의 태그로 끝나함<br>

불가능한 코드
```javascript
return(
  <div></div>
  <div></div>
)
```
가능한 코드
```javascript
return(
  <div>
    <div></div>
    <div></div>
  </div>
)
```
이떄 쓸모없는 div를 쓰기 싫으면 <></>로 사용해도 된다.<br>
이걸 fragment 문법이라 한다.
> ## <b>리액트 Component 문법</b>

리액트는 긴 HTML을 한 단어로 깔끔하게 치환해서 넣을 수 있는 문법을 제공한다.<br>
Component라고 한다.<br>
이걸 이용하면 함수 만들듯, 변수 만들듯 HTML을 깔끔하게 한 단어로 치환해서 원하는 곳에 꽂아넣을 수 있다.<br>

```javascript
function App (){
  return (
    <div>
      (생략)
      <Modal></Modal>
    </div>
  )
}

function Modal(){
  return (
    <div className="modal">
      <h4>제목</h4>
      <p>날짜</p>
      <p>상세내용</p>
    </div>
  )
}
```

> ## <b>Component 주의할점</b>

1. component 작명할 땐 영어대문자로 보통 작명합니다. <br>
2. return () 안엔 html 태그들이 평행하게 여러개 들어갈 수 없습니다. <br>
3. function App(){} 내부에서 만들면 안됩니다. <br>
4. <컴포넌트></컴포넌트> 이렇게 써도 되고 <컴포넌트/> 이렇게 써도 됩니다. <br>

> ## <b>arrow function 사용가능</b>
```javascript
function Modal(){
  return ( <div></div> )
}

let Modal = () => {
  return ( <div></div>) 
}
```