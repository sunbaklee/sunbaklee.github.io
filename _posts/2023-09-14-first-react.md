---
layout: post
published: true
title:  "리액트 초기세팅"
date: 2023-09-14
desc: "Quick test on writing code snippets in a blog post"
keywords: "React,website,blog,first"
categories: [React]
tags: [sunhak]
icon: icon-html
---
## <b>기초 세팅</b>
<hr>
## <b>1. node.js  설치하기</b>
node.js는 자바스크립트가 브라우저 밖에서도 동작하게 하는 환경을 의미한다.
리액트는 웹에서 작동을 하여 연관은 없지만 프로젝트를 개발하는데 주요 도구들이 node.js기반이기 떄문에 설치해야한다.
```
$ node -v (노드 버전 확인)
```  
<br>
## <b>2. CRA (Create React App) 설치</b> 
리액트 프로젝트를 시작하는데 필요한 개발환경을 세팅 해주는 도구 <br>
CRA는 리액트로 웹 어플리케이션을 만들기 위한 환경을 제공한다. CRA를 이용하면 하나의 명령어로 리액트 개발 환경을 구축할 수 있다
```
npx create-react-app 프로젝트명 
```
<br>
## <b>필요에 따른 라이브러리</b>
<hr>
## <b>3. React Router 설치</b>

사용자가 입력한 주소를 감지하는 역할을 하며, 여러 환경에서 동작할 수 있도록 여러 종유의 라우터 컴포넌트를 제공한다.
```
npm install react-router-dom --save
```
<br>
## <b>4. Sass 설치</b>
CSS의 단점을 보완하기 위해 만든 CSS 전처리기이다. 보통 CSS를 사용하다보면 단순 반복되는 부분이 많은 등, 불편함이 느껴지기 마련인데, SASS는 이 부분을 거의 완전히 해소시켜주는 스타일시트 언어다
```
npm install node -sass --save
```
