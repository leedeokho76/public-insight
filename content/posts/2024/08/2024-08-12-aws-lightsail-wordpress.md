---
title: "AWS Lightsail에서 WordPress 환경설정"
date: "2024-08-12"
slug: "aws-lightsail-wordpress"
description: "AWS의 LightSail 환경에서 WordPress 운용을 위한 Bitnami 등의 환경설정"
tags:
  ["Lightsail", "WordPress", "Bitnami", "라이트세일", "워드프레스", "비트나미"]
categories: ["Administration"]
draft: false
author: "Lee Deokho"
coverImage: ""
---

# AWS Lightsail에서 워드프레스 운영

## 워드프레스 구축

### Lightsail - Service Selection

1. Create an instance
2. Instance location: Seoul
3. Select a platform: Linux
4. Select a blueprint: Apps+OS WordPress
5. Choose your instance plan: $3.5
6. Identify your instance: Lightsail-Warehouse

### Lightsail - Find initial password

Connect using SSH in created Instance

```
cat ~/bitnami_application_password
```

### Browser - Access WordPress

To connect https://publicIPAddress/wp-admin and confirm login screen

### Lightsail - DNS zone & Static IP

1. Domains & DNS: Create DNS zone
   - Domain source: Use a domain from another registrar
   - Domain name: duqelee.com
2. Select a Region: Seoul
   - Attach to an instance: Select created Instance
   - Identify your static IP: Lightsail-Warehouse-IP

### Domain Hosting company - Name servers setting

Domains & DNS: select created DNS zone

- ns-574.awsdns-07.net
- ns-337.awsdns-42.com
- ns-1217.awsdns-24.org
- ns-1573.awsdns-04.co.uk

### Lightsail - Add DNS record

Domains & DNS: select created DNS zone
|DNS records|Record name|Resolves|
|:---:|:---:|:---:|
|Add A record|@|static IP|
|Add CNAME record|www|redirecting domain|

## 비트나미 툴을 이용한 SSL 인증

생성된 인스턴스에 콘솔 실행

```
===========================================
bitnami@ip-172-26-15-22:~$ sudo /opt/bitnami/bncert-tool
---------------------------------------------------------------------
Welcome to the Bitnami HTTPS Configuration tool.
---------------------------------------------------------------------
Domains
Please provide a valid space-separated list of domains for which you wish to configure your web server.
Domain list []: duqelee.com www.duqelee.com
---------------------------------------------------------------------
Enable/disable redirections
Please select the redirections you wish to enable or disable on your Bitnami installation.
Enable HTTP to HTTPS redirection [Y/n]: y
Enable non-www to www redirection [Y/n]: y
Enable www to non-www redirection [y/N]: n
---------------------------------------------------------------------
Changes to perform
The following changes will be performed to your Bitnami installation:
1. Stop web server
2. Configure web server to use a free Let's Encrypt certificate for the domains: duqelee.com www.duqelee.com
3. Configure a cron job to automatically renew the certificate each month
4. Configure web server name to: www.duqelee.com
5. Enable HTTP to HTTPS redirection (example: redirect http://duqelee.com to https://duqelee.com)
6. Enable non-www to www redirection (example: redirect duqelee.com to www.duqelee.com)
7. Start web server once all changes have been performed
Do you agree to these changes? [Y/n]: y
---------------------------------------------------------------------
Create a free HTTPS certificate with Let's Encrypt
Please provide a valid e-mail address for which to associate your Let's Encrypt certificate.
Domain list: duqelee.com www.duqelee.com
Server name: www.duqelee.com
E-mail address []: xxxxxx@xxx.xxx
The Let's Encrypt Subscriber Agreement can be found at:
https://letsencrypt.org/documents/LE-SA-v1.3-September-21-2022.pdf
Do you agree to the Let's Encrypt Subscriber Agreement? [Y/n]: y
---------------------------------------------------------------------
Performing changes to your installation
The Bitnami HTTPS Configuration Tool will perform any necessary actions to your Bitnami installation. This may take some time, please be patient.
---------------------------------------------------------------------
Success
The Bitnami HTTPS Configuration Tool succeeded in modifying your installation.
The configuration report is shown below.
Backup files:
--------- Skipped for security. ---------
Find more details in the log file:
/tmp/bncert-202308070556.log
If you find any issues, please check Bitnami Support forums at:
https://github.com/bitnami/vms
Press [Enter] to continue:
bitnami@ip-172-26-15-22:~$
===========================================
```

## 참고자료

### Lightsail

- <a href="https://lightsail.aws.amazon.com/ls/docs/en_us/articles/log-in-to-your-bitnami-application-running-on-amazon-lightsail" target="_blank">Getting the application user name and password for your Bitnami instance in Amazon Lightsail</a>
- <a href="https://lightsail.aws.amazon.com/ls/docs/en_us/articles/amazon-lightsail-quick-start-guide-wordpress" target="_blank">Quick start guide: WordPress on Amazon Lightsail</a>
- <a href="https://lightsail.aws.amazon.com/ls/docs/en_us/articles/lightsail-how-to-create-dns-entry" target="_blank">Creating a DNS zone to manage your domain’s DNS records in Lightsail</a>

### Bitnami

- <a href="https://docs.bitnami.com/aws/how-to/understand-bncert/" target="_blank">Learn about the Bitnami HTTPS Configuration Tool</a>
