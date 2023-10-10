---
layout: post
published: true
title:  "Next.js 기본 레이아웃"
date: 2023-10-08
desc: "Quick test on writing code snippets in a blog post"
keywords: "Jalpc,Jekyll,gh-pages,website,blog,easy"
categories: [React]
tags: [sunhak]
icon: icon-html
---

# <b>Next.js 기본 레이아웃</b>

> ## <b>1. Next.js 사용이유</b>

1. **성능**: Next.js는 자동 코드 분할, 서버 사이드 렌더링, 정적 사이트 생성과 같은 내장된 성능 최적화 기능을 제공하여 개발자가 최소한의 노력으로 빠르고 반응성 있는 웹 애플리케이션을 만들 수 있도록 도와준다.

2. **개발자 경험**: Next.js는 핫 모듈 교체, 자동 페이지 라우팅, 통합된 API 개발과 같은 기능을 제공하여 개발자가 애플리케이션을 쉽게 구축하고 반복적인 작업을 수행할 수 있도록 지원한다.

3. **유연성**: Next.js는 어떤 데이터 소스와도 함께 사용할 수 있으며, 기존 프로젝트에 쉽게 통합할 수 있어 다양한 웹 개발 요구에 유연하게 대응할 수 있다.

4. **생태계**: Next.js는 크고 활발한 개발자 커뮤니티를 가지고 있어, 개발자들이 애플리케이션을 구축하고 유지보수하기 위한 다양한 리소스, 타사 라이브러리 및 도구를 활용할 수 있다.

> ## <b>Next.js 설치 방법</b>

Next.js를 설치하려면 다음 단계를 따릅니다:

1. Node.js 설치: 먼저 컴퓨터에 Node.js를 설치합니다. [Node.js 공식 웹사이트](https://nodejs.org)에서 다운로드 및 설치할 수 있다.

2. 프로젝트 디렉터리 생성: 원하는 디렉터리에서 명령 프롬프트 또는 터미널을 열고 새로운 프로젝트 디렉터리를 생성

3. Next.js 설치: 다음 명령어로 Next.js를 설치합니다.

```javascript
npx create-next-app@latest
```
 - 설정 

Typescript : No

ESLink : Yes

Tailwind CSS : Yes

src/ directory : Yes

App Router : Yes

import alias : No


- 실행

1. 실행하기 위한 코드

```javascript
npm run dev
```

2. 빌드와 배포

2-1. 배포 가능한 버전의 어플 생성

```javascript
npm run build
```

2-2. 배포 버전 실행

```javascript
npm run start
```

---













