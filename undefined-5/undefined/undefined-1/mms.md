---
description: MMS 전송
---

# MMS

* MMS 최대 2,000byte(제목 40byte) 까지 전송 가능 합니다.
* MMS 이미지 메시지를 전송할 경우 사전에 이미지 파일 등록이 필요 합니다. 이미지 생성을 위해서는 '[FILE UPLOAD API](https://omniapi.gitbook.io/omni-api-specification/api-reference/registration/file)' 를 참조해 주세요. (MMS 이미지의 유효기간은 7일 입니다.)

## 전송 관련 컬럼

### **필수 입력 컬럼**

<table><thead><tr><th width="160">COLUMN</th><th>입력값</th></tr></thead><tbody><tr><td>callback</td><td>발신번호</td></tr><tr><td>mt_content</td><td>문자 내용 입력정보</td></tr><tr><td>mt_subject</td><td>문자 제목 입력정보</td></tr><tr><td></td><td></td></tr></tbody></table>

### **선택 입력 컬럼**

<table><thead><tr><th width="160">COLUMN</th><th>입력값</th></tr></thead><tbody><tr><td>mt_file_key</td><td><ul><li>전송할 이미지 파일키 입력정보</li><li>',' 구분자를 통해 최대 3개의 이미지 파일키를 입력할 수 있다.</li></ul></td></tr></tbody></table>

## 예제(Oracle)

{% code title="file 있는 mms" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, mt_content, mt_subject, mt_file_key) 
values (sq_msg_tran_01.nextval, 'mms', sysdate, '발신번호', '수신번호', '문자내용', '문자제목', '파일키');
```
{% endcode %}

{% code title="file 없는 mms" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, mt_content, mt_subject) 
values (sq_msg_tran_01.nextval, 'mms', sysdate, '발신번호', '수신번호' , '문자내용', '문자제목');
```
{% endcode %}
