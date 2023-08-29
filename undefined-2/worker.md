---
description: 메시지 전송과 관련된 worker에 대한 설명입니다.
---

# WORKER

### collector

* 데이터베이스를 조회하여 발송 대상 데이터를 SEND QUEUE(메모리큐)에 저장한다.

### sender

* SEND QUEUE 내부의 데이터를 OMNI 통합메세지 SEND API를 통해 인포뱅크 G/W로 송신한다.

### receiver

* OMNI 통합메세지 REPORT API를 통해 전송 결과를 수신하여 MSG\_REPORT 테이블에 저장한다.

### reportMigrator

* TRAN 테이블 데이터에 REPORT 테이블의 데이터 전송 결과를 업데이트한다.

### logMigrator

* REPORT 수신이 완료된 TRAN 테이블의 데이터를 LOG 테이블로 이관한다.
