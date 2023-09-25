---
layout: post
published: true
title:  "리액트 array, object state 변경하는 법"
date: 2023-09-18
desc: "Quick test on writing code snippets in a blog post"
keywords: "React,website,blog,first"
categories: [React]
tags: [sunhak]
icon: icon-javascript
---

## <b>리액트 array, object state 변경하는 법</b>
<hr>

> ## <b>글수정 버튼 만들기</b>
```javascript
function App(){
  
  let [글제목, 글제목변경] = useState( ['a', 'b', 'c'] );  
  
  return (
      <button onClick={ ()=>{ 글제목변경( ['a', 'b', 'c'] ) } }> 수정버튼 </button>
  )
}
```
이렇게 만들수 있다. 버튼을 누르면 첫 글제목이 바뀐다.

> ## <b>다르게 만들기</b>
```javascript
function App(){
  
  let [글제목, 글제목변경] = useState( ['a', 'b', 'c'] );  
  
  return (
    <button onClick={ ()=>{ 
      글제목[0] = 'd';
      글제목변경(글제목)
    } }> 수정버튼 </button>
  )
}
```
이런식으로 <b>array[x]='바꿀값'</b>으로도 변경이 된다.<br>
그것보다 좋은 방식도 있는데

```javascript
function App(){
  
  let [글제목, 글제목변경] = useState( ['a', 'b', 'c'] );  
  
  return (
    <button onClick={ ()=>{ 
      let copy = [...글제목];
      copy[0] = 'd';
      글제목변경(copy)
    } }> 수정버튼 </button>
  )
}
```
이런식으로도 사용이 가능하다.<br><br>

<b>let copy = [...글제목];</b> 이거를 <b>let copy = 글제목;</b> 이렇게 쓰면 바뀌지 않는데 그거는 추후 추가 예정