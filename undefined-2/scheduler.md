---
description: 메시지 전송 이외의 기능에 대한 설명입니다.
---

# SCHEDULER

## 파일 업로드 : 이미지 파일 키 발급

* file\_upload 테이블에서 이미지 파일을 등록하고 관리할 수 있습니다.
* 기본 24시간 주기로 갱신되며 msgConfig 파일의fileUpload.ttl configuration에서 주기 설정을 변경할 수 있습니다.
* 등록된 이미지 파일은 유효기간 내 재사용 할 수 있습니다.
* 유효기간은 mms 7일, rcs 1년입니다.
* 이미지 파일 명은 최대 40자까지이며 영문, 숫자를 권장합니다.
* 파일 업로드 프로세스가 동작할 때 메시지 발송 건수가 많다면 업로드 프로세스는 skip 될 수 있습니다.

### **예제(ORACLE)**

{% code title="MMS 파일 업로드" overflow="wrap" %}
```sql
INSERT INTO FILE_UPLOAD (file_seq, file_path, channel_type) VALUES (sq_file_upload_01.nextval, 'C:\Infobank\OMNI-1.0.0\attach_file\mms/test.jpg', 'MMS');
```
{% endcode %}

{% code title="RCS 파일 업로드" overflow="wrap" %}
```sql
INSERT INTO FILE_UPLOAD (file_seq, file_path, channel_type) VALUES (sq_file_upload_01.nextval, 'C:\Infobank\OMNI-1.0.0\attach_file\rcs/test.jpg',  'RCS');
```
{% endcode %}

{% code title="FRIENDTALK 파일 업로드" overflow="wrap" %}
```sql
INSERT INTO FILE_UPLOAD (file_seq, file_path, channel_type, msg_type) VALUES ('sq_file_upload_01.nextval, 'C:\Infobank\OMNI-1.0.0\attach_file\/infobank_fi.jpg', 'FRIENDTALK', 'FI');
```
{% endcode %}

## 발송 차단 설정

* msg\_banlist 테이블을 통하여 수신번호, 메시지 내용 항목에 대해 메시지 발송 시 차단하는 기능을 제공합니다.
* 수신번호는 rta\_banlist 테이블에 입력 즉시 전송대상에서 차단됩니다.
* 메시지 내용은 agent 메모리에 올리는 주기가 존재하여 일정 시간 이후에 차단 됩니다.
* 갱신 주기는 msgConfig 파일의 scheduler.banCheck.interval 에서 설정 가능합니다.

### 예제(ORACLE)

{% code title="수신번호 차단" overflow="wrap" %}
```sql
INSERT INTO MSG_BANLIST VALUES(sq_msg_banlist_01.nextval,'R','차단할수신번호','Y');
```
{% endcode %}

{% code title="메시지 내용 차단" %}
```sql
INSERT INTO MSG_BANLIST VALUES(sq_msg_banlist_01.nextval,'T','차단내용','Y');
```
{% endcode %}

## 테이블 생성

* 주기적으로 테이블을 조회하여 존재하지 않는 테이블을 자동으로 생성합니다.
* 생성되는 테이블은 msg\_tran, msg\_report, msg\_banlist, file\_upload, msg\_log\_yyyymm, msg\_log\_yyyymm(+1) 총 6개 입니다.
* LOG 테이블의 경우 현재 달, 다음 달의 테이블을 생성합니다.

## 전송데이터 정리

* 전송이 완료되지 못한 발송 데이터들을 LOG 테이블로 이관하는 기능입니다.
* 기본 4일 이전의 데이터들이 대상이며, msgConfig 파일의 scheduler.clean.tran.range configuration에서 범위를 조정할 수 있습니다.
