---
layout: post
published: true
title:  "리액트 props 맛보기"
date: 2023-09-21
desc: "Quick test on writing code snippets in a blog post"
keywords: "React,website,blog,first"
categories: [React]
tags: [sunhak]
icon: icon-javascript
---

## <b>리액트 props 맛보기</b>
<hr>

> ## <b>props란?</b>

<b>서로 다른 컴포넌트에 state를 전송해주는 것 부모에서 자식으로</b>

> ## <b>props로 부모 -> 자식 state 전달 방법</b>

<b>1. 자식컴포넌트 사용하는 곳에 가서 <자식컴포넌트 작명={state이름}/> </b>
<b>2. 자식컴포넌트 만드는 function으로 가서 props라는 파라미터 등록 후 props.작명 사용</b>

```javascript
function App (){
  let [글제목, 글제목변경] = useState(['a', 'b', 'c']);
  return (
    <div>
      <Modal 글제목={글제목}></Modal>
    </div>
  )
}

function Modal(props){
  return (
    <div className="modal">
      <h4>{ props.글제목[0] }</h4>
      <p>날짜</p>
      <p>상세내용</p>
    </div>
  )
}
```

> ## <b>props는 함수 파라미터 문법이랑 같다</b>

```javascript
function Modal(props){
  return (
    <div className="modal" style={{ background : 'skyblue' }}>
      <h4>{ props.글제목[0] }</h4>
      <p>날짜</p>
      <p>상세내용</p>
    </div>
  )
}
```