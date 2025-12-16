---
title: "ZeroSSL 서비스를 이용한 SSL 무료 보안 인증"
date: "2024-08-10"
slug: "zerossl-https-ssl"
description: "무료인증서 서비스를 제공하는 ZeroSSL 서비스를 이용한 보안접속 환경 구현"
tags: ["ssl", "보안인증", "https", "보안접속"]
categories: ["Administration"]
draft: false
author: "Lee Deokho"
coverImage: ""
---

# ZeroSSL 서비스를 이용한 SSL 무료 보안 인증

## 최초 인증서 발급

1. [ZeroSSL 회원가입 및 로그인](https://app.zerossl.com)
2. Enter Domain name
3. Validity(유효기간): 무료는 90일
4. Add-Ons: 별도선택 불필요
5. CSR & Contact: Auto-Generate CSR
6. Encryption Algorithm: RSA 2048 is selected by default
7. Finalize Your Order: Free
8. Email Verification: 이메일을 통한 활성화 과정으로 수신할 수 있는 이메일은 admin·administrator·postmaster·hostmaster·webmaster@신청도메인네임 으로 제한
9. Install Certificate: Default Format으로 선택 후, 압축파일 다운로드

## ZeroSSL 웹사이트에서 발급 받은 인증서 등록

> Cafe24.com 호스팅을 가정하고 설명

1. "나의서비스관리" - "인증서관리" - "외부인증서관리"
2. "certificate.crt" 파일을 텍스트 에디터로 열어서 안의 코드 복사
3. "인증서(SSL CRT)" 항목에 복사한 코드를 붙여 넣고, "인증서 확인" 클릭
4. "private.key" 파일을 텍스트 에디터로 열어서 안의 코드 복사
5. "개인키(Private Key)" 항목에 복사한 코드를 붙여 넣고, "신청하기" 클릭

## 인증서 변환

> 다른 형식의 인증서 파일이 필요한 경우

1. Open certificate.crt
2. "자세히" Tab
3. "파일에 복사" Click
4. Format Selection

## 인증서 갱신

> 무료의 경우 3달마다 수동으로 갱신 필요

1. <a href="https://app.zerossl.com" target="_blank">ZeroSSL 로그인</a>
2. Expired Tab
3. in Certificates Click
4. Renew Click
5. Check E-mail
6. Go To Verification Page and then Enter Validation Code
7. Following Istruction for Certification Zip File Download
8. [최초로 발급받은 인증서 등록](#zerossl-웹사이트에서-발급-받은-인증서-등록) 반복
