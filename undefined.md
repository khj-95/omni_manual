---
description: Agent를 사용하기 위한 요구사항입니다.
---

# 준비하기

## 계정 및 설치파일

영업 담당자로부터 접속 계정 정보를 제공받아야 합니다.&#x20;

인포뱅크 비즈고 사이트에 접속하여 사용자 시스템에 맞는 설치파일을 다운로드 합니다.&#x20;



## 데이터베이스 접속 계정 및 권한

에이전트가 설치되는 서버에서 접속 가능 한 데이터베이스 계정 정보와 테이블 권한(SELECT/UPDATE/DELETE/CREATE)이 필요합니다.&#x20;



## 시스템 요구사항

SYSTEM

| 구분         | 설치 시 필요 환경            |
| ---------- | --------------------- |
| Linux/Unix | java(JDK/JRE) 8.0  이상 |
| Windows    | java(JDK/JRE) 8.0  이상 |

DATABASE

| VENDER               |
| -------------------- |
| Oracle               |
| Microsoft SQL Server |
| MySQL                |
| PostgreSQL           |
| MariaDB              |
| Tibero               |



## 네트워크 방화벽 허용

> [https://omni.bizgo.io> ](https://omni.bizgo.io)

API 요청을 위해 OMNI API BaseURL에 방화벽 허용(Outbound)이 필요합니다.&#x20;
