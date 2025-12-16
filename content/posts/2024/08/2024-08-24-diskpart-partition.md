---
title: "Diskpart를 이용한 파티션 관리"
date: "2024-08-24"
slug: "diskpart-partition"
description: "Diskpart를 이용하여 하드디스크 파티션 분할병합 및 포멧 등의 관리방법"
tags: ["Diskpart", "harddisk", "partition", "파티션"]
categories: ["CaseStudy"]
draft: false
author: "Lee Deokho"
coverImage: ""
---

# DiskPart를 이용한 파티션 관리

## 버전

- Microsoft Diskpart 버전 10.0.19041.964

## 멸령어 일람

|   명령어    | 설명                                                                                                                                                                         |
| :---------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|   ACTIVE    | 선택한 파티션을 활성으로 표시                                                                                                                                                |
|     ADD     | 단순 볼륨에 미러를 추가                                                                                                                                                      |
|   ASSIGN    | 선택한 볼륨에 드라이브 문자 또는 탑재 지점을 할당                                                                                                                            |
| ATTRIBUTES  | 볼륨 또는 디스크 특성을 조작                                                                                                                                                 |
|   ATTACH    | 가상 디스크 파일을 연결                                                                                                                                                      |
|  AUTOMOUNT  | 기본 볼륨의 자동 탑재를 사용 및 사용 안 함으로 설정                                                                                                                          |
|    BREAK    | 미러 집합을 나눔                                                                                                                                                             |
|    CLEAN    | 디스크에서 구성 정보 또는 모든 정보를 삭제하고, 디스크를 닫음                                                                                                                |
|   COMPACT   | 파일의 물리적 크기 축소                                                                                                                                                      |
|   CONVERT   | 서로 다른 디스크 형식으로 변환                                                                                                                                               |
|   CREATE    | 볼륨, 파티션 또는 가상 디스크 생성                                                                                                                                           |
|   DELETE    | 개체를 삭제                                                                                                                                                                  |
|   DETAIL    | 개체 정보를 제공                                                                                                                                                             |
|   DETACH    | 가상 디스크 파일을 분리                                                                                                                                                      |
|    EXIT     | DiskPart 종료                                                                                                                                                                |
|   EXTEND    | 볼륨을 확장                                                                                                                                                                  |
|   EXPAND    | 가상 디스크에서 사용할 수 있는 최대 크기를 확장                                                                                                                              |
| FILESYSTEMS | 볼륨의 지원되는 파일 시스템과 현재 파일 시스템을 표시                                                                                                                        |
|   FORMAT    | 볼륨 또는 파티션을 포맷                                                                                                                                                      |
|     GPT     | 특성을 선택한 GPT 파티션에 할당                                                                                                                                              |
|    HELP     | 명령 목록을 표시                                                                                                                                                             |
|   IMPORT    | 디스크 그룹 가져옴                                                                                                                                                           |
|  INACTIVE   | 선택한 파티션을 비활성 상태로 표시                                                                                                                                           |
|    LIST     | 개체 목록을 표시                                                                                                                                                             |
|    MERGE    | 자식 디스크를 부모 디스크와 병합                                                                                                                                             |
|   ONLINE    | 현재 오프라인으로 표시된 개체를 온라인 상태로 만듬                                                                                                                           |
|   OFFLINE   | 현재 온라인으로 표시된 개체를 오프라인 상태로 만듬                                                                                                                           |
|   RECOVER   | 선택한 팩에 있는 모든 디스크의 상태를 새로 고침. 잘못된 팩에 있는 디스크에 대해 복구를 시도하고 미러된 볼륨과 부실 플렉스 또는 패리티 데이터가 있는 RAID5 볼륨을 다시 동기화 |
|     REM     | 아무 작업도 하지 않음. 스크립트를 설명하는데 사용                                                                                                                            |
|   REMOVE    | 드라이브 문자 또는 탑재 지점 할당을 제거                                                                                                                                     |
|   REPAIR    | 실패한 구성원이 있는 RAID-5 볼륨을 복구                                                                                                                                      |
|   RESCAN    | 디스크 및 볼륨을 다시 검색                                                                                                                                                   |
|   RETAIN    | 단순 볼륨에 보유된 파티션 생성                                                                                                                                               |
|     SAN     | 현재 부팅된 OS에 대한 SAN 정책을 표시하거나 설정                                                                                                                             |
|   SELECT    | 포커스를 개체로 이동                                                                                                                                                         |
|    SETID    | 파티션 형식을 변경                                                                                                                                                           |
|   SHRINK    | 선택한 볼륨을 축소                                                                                                                                                           |
|  UNIQUEID   | 디스크의 GPT(GUID 파티션 테이블) 식별자 또는 MBR(마스터 부트 레코드) 서명을 표시하거나 설정                                                                                  |

## 사용방법

```
C:\diskpart in Shell or CLI
// list disk and select the Target disk
// list partition and select the Target partition

del part override
// delete partition. If it is impossible, use the next
```
