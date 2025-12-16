---
title: "Docsify를 이용한 콘텐츠 관리 및 정적 웹사이트 구축"
date: "2025-10-12"
slug: "docsify-static-website"
description: "Docsify를 이용한 정적 웹페이지로 콘텐츠를 관리하고, Github.com 리포지토리에 개인도메인을 할당하여 정적 웹사이트 구축"
tags: ["Docsify", "static-website", "정적웹사이트", "Github", "깃허브"]
categories: ["Development"]
draft: false
author: "Lee Deokho"
coverImage: ""
---


# Docsify를 이용한 콘텐츠 관리 및 정적 웹사이트 구축

## 콘텐츠 관리를 위한 Docsify
### 폴더구조
```
www 
│ index.html
│ _navbar.md
│ _sidebar.md
│ README.md // 메인페이지 콘텐츠
│ guide.md
│ favicon.svg // 파바콘이미지
├─content // 정적 콘텐츠
│ └─posts
│   └─year
│     └─month
├─css
├─js
├─images // 정적 콘텐츠에 사용될 이미지
│ └─year
│   └─month
├─assets // react/hugo 전환시 ux/ui에 사용될 이미지 등 
├─public // react 전환예정 예약폴더
├─static // hugo 전환예정 예약폴더
├─scripts // 데이터변환 등 py 스크립트 등
└─temp
```

### 필요패키지 설치 및 테스트서버실행

```
$ node -v // node.js 설치 확인
v22.17.1

$ npm -v // npm 설치 확인
10.9.2

$ npm install -g docsify-cli // Docsify Command Line Interface 를 전역설치

npm warn deprecated docsify-server-renderer@4.13.1: docsify-server-renderer 4.x and below is no longer supported while we investigate the future of SSR and SSG for Docsify
// Docsify의 서버 사이드 렌더링(SSR) 관련 패키지가 더 이상 지원되지 않는다는 경고(warning)

added 206 packages in 7s

17 packages are looking for funding
  run `npm fund` for details
npm notice
npm notice New major version of npm available! 10.9.2 -> 11.6.2
npm notice Changelog: https://github.com/npm/cli/releases/tag/v11.6.2
npm notice To update run: npm install -g npm@11.6.2
npm notice

$ docsify -v // Docsify-cli 설치 확인

docsify-cli version:
  4.4.4

$ npm install -g npm@11.6.2 // node.js 설치시 같이 설치된 npm 버전 업데이트

added 1 package in 4s

28 packages are looking for funding
  run `npm fund` for details

$ docsify serve . // index.html이 위치한 폴더에서 Docsify 로컬 서버 실행

Serving D:\dev\www now.
Listening at http://localhost:3000

// 서비스 종료시 Ctrl + C
```

