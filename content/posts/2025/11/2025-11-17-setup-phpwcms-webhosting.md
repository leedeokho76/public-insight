---
title: "웹호스팅 환경에서 phpwcms 설치"
date: "2025-11-17"
slug: "setup-phpwcms-webhosting"
description: "cafe24 웹호스팅 환경에서 phpwcms-1.10.9 설치 및 초기 환경설정에 대한 내용"
tags: ["phpwcms", "setup", "webhosting"]
categories: ["Notes"]
draft: false
author: "Lee Deokho"
coverImage: ""
---

# 웹호스팅 환경에서 phpwcms 설치

## 1. 설치 첫화면

```
Welcome to the setup of phpwcms
This is the semi automatic setup script to install a new release of the web cms phpwcms.
phpwcms is open source software released under the GNU General Public License (GPL). Before you continue setting up phpwcms read the license very careful.

I agree GPL continue... 클릭
```

## 2. 서버 세팅 체크

```
1. Thanks! You have agreed to the GPL.
Now that you know the licence under which phpwcms is released you can continue to install or upgrade phpwcms.

2. Now lets check your server settings
Please proof all information about your system (recommend PHP 8.2+, MySQL 5.6+).

WWW server: Apache
PHP version: 8.4.10p1 OK  // 특히 버전확인 필요
MySQLi extension: installed OK
MySQLi client information: mysqlnd 8.4.10p1 (client lib)OK
PHP settingsSecurity risks
register_globals OffOK
GD2 bundled (2.1.0 compatible)GD2
Image types supported: GIFGIF supported/ PNGPNG supported/ JPGJPG supported
phpwcms has automatic image resizing capabilities. This works very well for standard graphics file formats like JPEG, GIF and PNG as long as your PHP installation has built-in support for GD — GD2 with freetype support is always recommend. Note: It is not necessary but recommend that you have installed ImageMagick and GhostScript on your server system which enables image resizing for nearly every graphics file format.

3. MySQL database settings
MySQL host and port:  // localhost 3306
DB user:  // db_user
DB password:  //	db_pass
DB database:  //	db_table   you have to create it before setup!!!
DB table prefix:  //	default: none (""), if filled in it will be prefix+_
use persistent database connection it should be safe to enable it // 지속연결 설정. 소규모 웹호스팅 사양에서는 권장하지 않음

4. Charset & MySQL (v10.6.17-MariaDB-log) settings Info
Info Charset: 한국어 - Korean [utf-8 / utf8mb4]

5. Default phpwcms database schema
create phpwcms db tables
Fine! All initial phpwcms tables were created or still exists.

6. Superuser settings
Name: 	Webmaster  // default: Webmaster
Admin login: 	admin  // default: admin
Admin password:  // default: phpwcms
Repeat password:
Admin email: 	// noreply@pub7.kr is used site wide

7. Path settings
site basis:  // current: https://www.pub7.kr do NOT add any subdir here like https://www.pub7.kr/wcms/

Settings for handling email sending in phpwcms

from/reply-to email:  // info@localhost
from/reply-to name:  // My Name
SMTP server:  // default: localhost
SMTP port :  // default: 25
mail method :  // default: mail (smtp, sendmail)
use SMTP_AUTH :  // default: ON
SMTP login:  // user
SMTP password:  // pass
secure connection:  // default (no secure connection)

8. 이후 진행되는 내용은 Default로 진행

```

## 3. 설치결과 확인

```
Ready to start phpwcms? Some "problems" maybe OK - you can check by testing phpwcms installation.

filestorage: 	 filearchive 		 OK (exists + writable)
deleted files: 	 filearchive/can_be_deleted 		 OK (exists + writable)
templates: 	 template 		 OK (exists + not writable)
template languages: 	 template/template_lang 		 OK (exists + writable)
ftp takeover: 	 upload 		 OK (exists + writable)
frontend content: 	 content 		 OK (exists + not writable)
frontend images: 	 content/images 		 OK (exists + writable)
frontend form: 	 content/form 		 OK (exists + writable)
frontend tmp: 	 content/tmp 		 OK (exists + writable)
frontend rss: 	 content/rss 		 OK (exists + writable)
frontend pages: 	 content/pages 		 OK (exists + not writable)
startup text: 	 template/inc_default/startup.php 		 OK (exists + writable)
main CSS file: 	 template/inc_css/frontend.css 		 OK (exists + writable)
index level settings: 	 include/config/conf.indexpage.inc.php 		 OK (exists + writable)
```

## 4. 후속조치

- setup 폴더 삭제
- templates, content, pages 디렉토리의 not writable 원인 해소를 위해 777->755 로 변경확인
- 설치경로/login.php 접속하여 관리자 로그인 후 콘텐츠 작성/이미지 업로드 테스트
- ImageMagick 확인 → 필요하다면 설치 및 경로 등록

## 참고자료

- [phpwcms Documentation](http://www.phpwcms.org/index.php?id=10,0,0,1,0,0)
- 기술문서를 해석하고 이해하는데 [Copilot](https://copilot.microsoft.com/)의 도움을 받았습니다.
