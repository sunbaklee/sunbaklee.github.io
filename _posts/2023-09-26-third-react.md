---
layout: post
published: true
title:  "리액트 state-1"
date: 2023-09-26
desc: "Quick test on writing code snippets in a blog post"
keywords: "React,website,blog,first"
categories: [React]
tags: [sunhak]
icon: icon-javascript
---

## <b>리액트 state-1</b>
<hr>

> ## <b>state 만드는 법</b>

원래 변수는 let a = 'b'이렇게 저장을 했었는데
리액트에서는 state를 사용하여 데이터 저장가능

```javascript
import { useState } from 'react';
import './App.css'

function App(){
 
  let [a,b] = useState('잠깐 저장');
  let c = '변수임';
  return (
    <div className="App">
      <div className="black-nav">
        <div>개발 blog</div>
      </div>
      <div className="list">
        <h4>글제목</h4>
        <p>9월 26일 발행</p>
        <hr/>
      </div>
    </div>
  )
}
```
맨 윗줄에 import {useState} from 'react'하고 <br>
원하는 곳에서 <b>useState('보관할 자료')</b>를 쓰면 state에 자료를 잠깐 저장이 가능하다.<br>
나중에 저장한 것을 사용하려면<br>
<b>let[a,b]= useState('잠깐 저장');</b><br>

> ## <b>let 자료형은 뭘까?</b>

```javascript
let array = ['Kim', 20];

let name = array[0];
let age = array[1]
```
이거를
```javascript
let [name, age] = ['Kim', 20]
```
이렇게 쉽게 가능하다<br><br>
리액트에서는 useState를 사용하면 [데이터1,데이터2]이 모양의 array가 남는다.<br>
데이터1 자리에는 자료, 데이터 2자리에는 state 변경을 도와주는 함수가 들어있다.<br>
따라서 직관적으로 <b>let[자료명,b] = useState('잠깐 저장');</b>이렇게 사용한다.

> ## <b>state를 사용하는 이유</b>
state는 변동사항이 생기면 state쓰는 html도 자동으로 재렌더링해준다.<br>
원래 그냥 자바스크립트는 변수내용이 바뀌면 코드를 짜서 바꿔야하지만 react는 state를 사용하면 자동으로 html를 재렌더링 해주어서 알아서 바뀐다.