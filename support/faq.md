---
description: 자주 묻는 질문
---

# FAQ

## OMNI Agent 설정 관련 FAQ

<details>

<summary>인증 아이디 오류</summary>

설치 후 OMNI Agent를 실행했는데, 토큰(TOKEN) 정보 요청 오류가 날 경우, 토큰 발급에 문제가 없는지 Infobank에 문의한다.

</details>

<details>

<summary>방화벽 확인</summary>

Infobank G/W에 접속이 안될 경우 방화벽을 체크한다.

#### OMNI API 서버, DNS lookup 가능

```
telnet omni.ibapi.kr 443
```

#### OMNI API 서버, DNS lookup 불가능

Infobank 서비스 문의 응대 담당자로부터 IP를 요청하여 연동한다.

</details>

<details>

<summary>Windows 환경에서 한 서버에 여러 EMMA 설치 시 서비스 수동 등록</summary>

Windows에서 여러 EMMA를 설치 시 서비스 명이 동일하기 때문에 기존 서비스 명을 덮어쓰게 된다.

이 경우는 Service를 수동으로 등록하여 주어야 한다.

#### Windows 서비스 수동 등록 방법

```
- sc create OMNI_SVC1 binpath= "C:\Infobank\OMNI-1.0.0\omnisvc.exe"^
displayName= "OMNI_SVC1" type= own start= auto
- sc delete OMNI_SVC1
```

</details>

## DB 설정 관련 FAQ

<details>

<summary>DB 권한</summary>

OMNI Agent는 DB 연동 방식이며 서비스 로그를 월별 로그 테이블을 생성하여 저장하므로 테이블에 대한 생성 권한이 주어져야 한다.

</details>
