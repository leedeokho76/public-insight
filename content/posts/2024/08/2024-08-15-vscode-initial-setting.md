---
title: "JavaScript 개발 환경을 고려한 VS Code 설정"
date: "2024-08-15"
slug: "vscode-initial-setting"
description: "VS Code 최초설치 후 JavaScript 개발을 고려한 환경설정"
tags: ["vscode", "setting"]
categories: ["Development"]
draft: false
author: "Lee Deokho"
coverImage: ""
---

# JavaScript 개발 환경을 고려한 VSCode 설정

## 1. 초기 화면 및 언어 설정(option)

### 1.1. 화면

- Commonly Used > Workbench: Color Theme
- **Dark Modern**

### 1.2. 언어

- (Extension) **Korean Language Pack** 다운로드
- 앱 다시 연 후, 언어가 변경된 것을 확인
- Ctrl + Shft + P 로 명령어 입력창 연 후, Configure Display Language 입력으로 언어설정 변경 가능

## 2. 자동 저장

### 2.1. Text Editor > Files > Auto Save

- off 미사용
- (Person) **after Delay** 일정시간 경과 후 저장
- onFocusChange 다른 앱(파일)으로 포커스 이동시 저장
- onWindowChange 다른 창(또는 창 최소화) 진행시 저장

### 2.2. Text Editor > Files > Auto Save Delay

- 밀리초 단위
- (Person) **600000**

## 3. 들여쓰기

### 3.1. Text Editor > Editor: Tab Size

- 가독성과 협업을 고려
- (Person) **2**
- 범위 설정 후 Shft + Alt + F 로 자동 포멧팅

### 3.2. Text Editor > Editor: Insert Spaces

- 다양한 에디터에서의 일관성 유지를 위해 탭 대신 공백 사용
- (Default) check

### 3.3. Text Editor > Editor: Detect Indentation

- 자동 감지 해제
- (Person) **uncheck**

## 4. 자동 줄바꿈

### 4.1. Text Editor > Editor: wordWrap

- 화면 넓이에 맞춰 줄바꿈
- (Person) **on**

### 4.2.Text Editor > Editor: wordWrapColumn

- 줄바꿈 기준 너비
- (Default) 80

### 4.3. Text Editor > Editor: Wrapping Indent

- 줄바꿈된 줄의 들여쓰기 방식
- (Default) same

## 5. 글꼴

### 5.1. Text Editor > Font > Editor: Font Family

- 한글 사용 및 가독성 고려
- (Person) **D2Coding** 추가

### 5.2. Text Editor > Font > Editor: Font Size

- (Person) **16**

### 5.3. Text Editor > Font > Editor: Font Ligatures

- 가독성 고려
- (Person) **true**

## 6. 포멧터 설정

### 6.1. Text Editor > Editor: Default Formatter

- (Extension) Prettier - Code formatter 다운로드
- (Person) **Prettier - Code formatter** 선택

### 6.2. Text Editor > Formatting > Editor: Format On Save

- 저장시 자동으로 포멧 맞춤
- (Person) **check**

### 6.3. Extension > Prettier > Prettier: Tab Width

- (Person) **2**

### 6.4. Extension > Prettier > Prettier: Single Quote

- JS, React 에서는 문자열에 작은따옴표, JSX에서는 큰따옴표 사용
- (Person) **check**

## 7. 추가 Extension

### 7.1. 언어 확장 도구

- (JS) ESLint: 자바스크립트 문법 오류와 스타일 체크
- (JS) Code Runner: js코드작성 후 Ctrl + Alt + N 실행
- (JS) Live Server:  코딩 후 마우스 우클릭 open Live Server 선택하면 브라우저 실행
- (JS) CSS Peek: 클래스에 컨트롤 눌러 CSS 확인 및 이동 가능
- (JS) Prettier - Code Formatter
  - 설치 후 Extensions - Prettier - Prettier: Single Quote
    - 체크해제 **Use single instead of double quotes.**
- (Py) Python
- (Py) Remote -SSH
- (Py) Remote Development
- (Py) Jupyter
- (Ra) ES7+ React : 리액트 탬플릿 생성

### 7.2. 생산성

- (MK) Auto Close Tag: 닫는 태그 자동 생성
- (MK) Auto Rename Tag: 여는 태그와 닫는 태그 자동 완성
- (HC) HTML to CSS autocompletion
- (HC) HTML CSS Support
- (Spelling) Code Spell Checker
- (Numpy) vscode-numpy-viewer
- (CSV) RainbowCSV
- (View) Night Owl: 컬러테마
- (Path) Path Intellisense:  자동 패스 입력
- (MD) Markdown Preview Github Styling
