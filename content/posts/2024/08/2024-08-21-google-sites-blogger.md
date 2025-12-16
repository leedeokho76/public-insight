---
title: "Google 사이트 도구 및 Blogger 사용을 위한 초기 설정"
date: "2024-08-21"
slug: "google-sites-blogger"
description: "구글 사이트 도구와 블로거 사용을 위한 초기 환경 설정"
tags: ["Google", "Sites", "구글", "Blogger", "블로거"]
categories: ["Administration"]
draft: false
author: "Lee Deokho"
coverImage: ""
---

# Google 사이트 도구 및 Blogger 사용을 위한 초기 설정

## 구글 사이트 도구를 위한 도메인 설정

### 커스텀 도메인 설정

1. Sites 관리자 > 설정 > 커스텀 도메인 > 설정 시작
   1. 도메인 입력
   2. 소유권 확인
   3. TXT 레코드 값 복사
2. Domain Service 업체의 DNS 레코드 추가
   |TXT|CNAME|
   |:---:|:---:|
   |TXT 레코드 값|ghs.googlehosted.com. (마지막 마침표까지 포함)|

## 구글 블로거를 위한 도메인 설정

### 개인 도메인 설정

1. Blogger 관리자 > 설정 > 게시 중 > 맞춤도메인 > 도메인 정보 입력 후 저장
   - 이 때 아래와 같은 메시지가 표시되면 DNS 등록할 정보이므로 메모장 등에 저장
     ```
     "블로그 CNAME: 이름에 'blog.' 또는 'www.' 같은 하위 도메인 이름을 입력합니다. 목적지 URL에 'ghs.google.com'을 입력합니다.
         보안 CNAME: '이름: 블라블라블라...,
         목적지 URL: 블라블라블라...'"
     ```
2. Domain Service 업체의 DNS 레코드 추가
   |타입|호스트|값|
   |:---:|:---:|:---:|
   |CNAME|blog|ghs.google.com|
   |CNAME|보안CNAME이름|목적지 URL|

### www로 리디렉션

1. Domain Service 업체의 DNS설정에 다음 정보를 기초로 A래코드 추가
   - 216.239.32.21
   - 216.239.34.21
   - 216.239.36.21
   - 216.239.36.21
2. Blogger 관리자화면의 좌측 메뉴 중 '설정' 클릭
   - '게시' 아래에서 도메인 리디렉션(mydomain.com에서www.mydomain.com으로)을 사용 설정

## 구글 블로거 초기 사용환경 변경

### 설정

- 기본: 제목, 설명
- 개인정보 보호
- HTTPS
- 글: 이미지 라이트박스
- 서식: 날짜 헤더 양식, 타임 스탬프 형식
- 메타 태크
- 사이트 피드: 제목 및 첨부한 링크

### 테마

- Contempo Light
  - 백그라운드
    - 이미지 변경
    - 기본 색상 테마
  - 고급
    - 탭 텍스트
      - 글꼴: Arial 20px
    - 글
      - 글 제목 글꼴: Arial 32px

### 크롬에서 구텐베르크 에이터 와이드화면 사용

- Installation Stylus Extension App in Google Chrome Market and Activate Stylus
- 크롬에서 적용하고자 하는 Website 방문 후, Click Stylus
- 새 스타일 작성
  - Input Name
  - a89Sje {max-width: 900px;}
  - Save
