---
title: "카카오 비즈니스 서비스 이용을 위한 환경설정"
date: "2024-08-06"
slug: "kakao-business-setup"
description: "카카오 비즈니스 서비스 이용을 위해 필요한 초기 환경설정 방법 정리"
tags: ["Tistory", "티스토리", "Daum", "다음스마트워크", "Domain", "외부도메인"]
categories: ["Administration"]
draft: false
author: "Lee Deokho"
coverImage: ""
---

# 카카오 비즈니스 서비스 이용을 위한 환경설정

## 티스토리 서비스에 외부 도메인 연결을 위한 환경설정

### 도메인 네임 서비스회사에서의 DNS 설정

DNS 레코드 설정 창에서 다음 2개의 DNS 레코드 설정 추가

|  Record Type | Sub Domain | Record Value    |
| :----------: | :--------: | --------------- |
|       A      |     @      | 27.0.236.139    |
|    CNAME     |    www     | host.tistory.io |

### 티스토리에서의 설정

관리 - 블로그 - 개인 도메인 설정

### 메인 도메인을 2차 도메인으로 리디렉션

소스편집 html head 태그 내에 다음 코드 삽입

```
<!-- 리디렉션 시작 -->
<script type-"text/javascript">
  var url1 = 'duqe.tistory.com'; // 티스토리 계정
  var url2 = 'duqe.kr'; // 개인 도메인
  var online = document.URL;
  if (online.match(url1)) document.location.href = online.replace(url1, url2);
</script>
<!-- 리디렉션 끝 -->
```

## 다음 스마트워크 이용을 위한 환경설정

### 도메인 네임 서비스회사에서의 DNS 설정

DNS 레코드 설정 창에서 다음 2개의 DNS 레코드 설정 추가

|  Sub Domain | Record Type | Record Value       |
| :---------: | :---------: | ------------------ |
|      @      |     MX      | ASPMX.daum.net     |
|      @      |     MX      | ALT.ASPMX.daum.net |

### 티스토리에서의 설정

관리 - 블로그 - 개인 도메인 설정

### 비즈니스 메일 설정

다음메일 로그인 - 다음 스마트워크

### 확장 메일 클라이언트 설정

|  구분 |    Server     | Port |
| :---: | :-----------: | :--: |
|  POP3 | pop.daum.net  | 995  |
| IMAP  | imap.daum.net | 993  |
| SMTP  | smtp.daum.net | 465  |

## 참고자료

- <a href="https://cs.kakao.com/helps?service=175&locale=ko" target="_blank">카카오 고객센터 - 티스토리</a>
- <a href="https://cs.daum.net/" target="_blank">다음 고객센터</a>
