# INTERNATIONAL

* 국제 발송의 경우 단일 발송만 가능합니다.&#x20;
* 수신번호는 국제번호의 형식으로 입력합니다.&#x20;

## 전송 관련 컬럼

### **필수 입력 컬럼**

<table><thead><tr><th width="160">COLUMN</th><th>입력값</th></tr></thead><tbody><tr><td>callback</td><td>발신번호</td></tr><tr><td>mt_content</td><td>문자 내용 입력정보</td></tr></tbody></table>

## 예제(Oracle)

{% code overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, mt_content) 
values (sq_msg_tran_01.nextval, 'international', sysdate, '15882460', '+821056232189', 'international 국제 문자 테스트입니다.');
```
{% endcode %}