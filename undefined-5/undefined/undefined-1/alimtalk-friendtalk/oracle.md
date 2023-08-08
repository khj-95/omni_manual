---
description: KKO 상세 메시지 타입 별 예제입니다.
---

# 메시지 타입 별 예제(Oracle)

{% code title="alimtalk-AT, nobutton" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, kko_msg_type, kko_content, kko_sender_key, kko_template_code) 
values (sq_msg_tran_01.nextval, 'alimtalk', sysdate, '발신번호', '수신번호', 'AT', '내용', '발신프로필키', '템플릿코드');
```
{% endcode %}

{% code title="alimtalk-AT, button" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, kko_msg_type, kko_content, kko_sender_key, kko_template_code, kko_option) 
values (sq_msg_tran_01.nextval, 'alimtalk', sysdate, '발신번호', '수신번호', 'AT', '내용', '발신프로필키', '템플릿코드', 
'{
  "button":[
      {
         "type":"WL",
         "name":"홈페이지",
         "url_mobile":"https://www.kakao.com",
         "url_pc":"https://www.kakao.com",
         "target": "out"
      }
   ]
}');
```
{% endcode %}

{% code title="alimtalk-AI, nobutton" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, kko_msg_type, kko_content, kko_sender_key, kko_template_code) 
values (sq_msg_tran_01.nextval, 'alimtalk', sysdate, '발신번호', '수신번호', 'AI', '내용', '발신프로필키', '템플릿코드');
```
{% endcode %}

{% code title="alimtalk-AI, button" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, kko_msg_type, kko_content, kko_sender_key, kko_template_code, kko_option) 
values (sq_msg_tran_01.nextval, 'alimtalk', sysdate, '발신번호', '수신번호', 'AI', '내용', '발신프로필키', '템플릿코드', 
'{
  "button":[
      {
         "type":"WL",
         "name":"홈페이지",
         "url_mobile":"https://www.kakao.com",
         "url_pc":"https://www.kakao.com",
         "target": "out"
      }
   ]
}');
```
{% endcode %}

{% code title="friendtalk-FT, nobutton" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, kko_msg_type, kko_content, kko_sender_key) 
values (sq_msg_tran_01.nextval, 'friendtalk', sysdate, '발신번호', '수신번호', 'FT', '내용', '발신프로필키');
```
{% endcode %}

{% code title="friendtalk-FI, nobutton" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, kko_msg_type, kko_content, kko_sender_key, kko_option) 
values (sq_msg_tran_01.nextval, 'friendtalk', sysdate, '발신번호', '수신번호', 'FI', '내용', '발신프로필키',
'{
  "attachment":{
    "image": {
      "imgUrl" : "이미지URL(파일키)",
      "imgLink" : "http://www.daum.net"
    }
  }
}');
```
{% endcode %}

{% code title="friendtalk-FW, nobutton" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, kko_msg_type, kko_content, kko_sender_key, kko_option) 
values (sq_msg_tran_01.nextval, 'friendtalk', sysdate, '발신번호', '수신번호', 'FW', '내용', '발신프로필키',
'{
  "attachment":{
    "image": {
      "imgUrl": "이미지URL(파일키)",
      "imgLink": "http://www.daum.net"
    }
  }
}
```
{% endcode %}

