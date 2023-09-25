---
layout: post
published: true
title:  "리액트 map 맛보기"
date: 2023-09-20
desc: "Quick test on writing code snippets in a blog post"
keywords: "React,website,blog,first"
categories: [React]
tags: [sunhak]
icon: icon-javascript
---

## <b>리액트 map 맛보기</b>
<hr>

> ## <b>기존 자바 스크립트의 map함수</b>

```javascript
var arr = [2,3,4];
arr.map(function(){
  console.log(1)
});
```
<b>기능1.</b>arr의 자료 개수만큼 코드 반복 실행

```javascript
var arr = [2,3,4];
arr.map(function(a){
  console.log(a)
});
```
<b>기능2.</b>arr의 자료 출력

```javascript
var 어레이 = [2,3,4];
var newArray = 어레이.map(function(a){
  return a * 10
});
console.log(newArray)
```
<b>기능3.</b>arr의 자료 담기

> ## <b>JSX의 map함수</b>

html을 반복생성하고 싶으면 사용가능
```javascript
function App (){
  return (
    <div>
      { 
        [1,2,3].map(function(){
          return ( <div>안녕</div> )
        }) 
      }
    </div>
  )
}
```
이러면 안녕이 3개가 나온다<br>
state에도 사용이 가능한데
```javascript
function App (){
  return (
    <div>
      (생략)
      { 
        글제목.map(function(){
          return (
          <div className="list">
            <h4>{ 글제목[0] }</h4>
            <p>2월 18일 발행</p>
          </div> )
        }) 
      }
    </div>
  )
}
``` 
이렇게 사용이 가능하다<br>
하지만 이러면 같은 글만 3가지가 나오는데 그게 싫으면
```javascript
function App (){
  return (
    <div>
      (생략)
      { 
        글제목.map(function(a){
          return (
          <div className="list">
            <h4>{ a }</h4>
            <p>2월 18일 발행</p>
          </div> )
        }) 
      }
    </div>
  )
}
```
이렇게 사용이 가능하다

(참고) map 반복문으로 반복생성한 html엔 key={i} 이런 속성을 추가해야합니다. 

 
```javascript
<div className="list" key={i}> 
```
그래야 리액트가 <div>들을 각각 구분할 수 있어서 그렇다. <br>

for문도 사용은 가능하다