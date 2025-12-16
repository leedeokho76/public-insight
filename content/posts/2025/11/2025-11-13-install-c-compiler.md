---
title: "Windows 11 환경에서 C 컴퍼일러 설치 및 환경설정"
date: "2025-11-13"
slug: "install-c-compiler"
description: "윈도우11 환경에서 C컴파일을 위한 컴파일러 설치 및 환경설정에 대한 설명"
tags: ["C", "compiler", "setting"]
categories: ["Notes"]
draft: false
author: "Lee Deokho"
coverImage: ""
---

# Windows 11 환경에서 C 컴퍼일러 설치 및 환경설정

## 설치

1. SourceForge에서 mingw-get-setup.exe 다운로드
2. Default 로 설치 진행
3. MinGW Installation Manger 연 상태에서 다음 4개 항목 선택
   - mingw-developer-toolkit
   - minigw32-base
   - mingw32-gcc-g++
   - msys-base
4. installation - Update Category 또는 Apply Changes

## Path 설정

1. 시스템 검색창에서 "시스템 환경변수 편집" 항목 검색 후 클릭
2. "환경변수" 클릭
3. 시스템변수 창에 Path 선택 후, 편집
4. "새로만들기" 클릭 후 경로(C:\MinGW\bin) 입력
5. 명령프롬프트창에서 다음 명령어로 버전 확인
   ```
   C:\Users\user>gcc -v
   ```
6. 다음 소스 저장

   ```
   // Hello.c

   #include <stdio.h>
   int main(void) {
   printf("%s", "Hello, World!!);
   return 0;
   }
   ```

7. 컴파일

   ```
   C:\Users\user>gcc Hello.c // a.exe 생성
   C:\Users\user>gcc -o Hello Hello.c // Hello.exe 생성
   ```

8. 실행결과 확인
