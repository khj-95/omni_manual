---
description: KKO 상세 메시지 타입 별 예제입니다.
---

# 메시지 타입 별 예제(Oracle)

### <예시 데이터>

* 발신 프로필 키(Sender Key): “aaaaa22222bbbbb33333ccccc44444ddddd55555”
* 템플릿 메시지: “Test Message 입니다.”
* 템플릿 코드: “INFO\_001”
* (버튼 있는경우) 버튼 예시
  * 버튼타입 : AL
  * 버튼명 : 확인하기
  * schemeAndroid : daumapps://open
  * schemeIos : daumapps://open
* (버튼 있는경우) 버튼 예시 :&#x20;
  * 버튼타입 : 웹링크-WL
  * 버튼명 : 홈페이지
  * mobile\_url/pc\_url : https://soldevteam-tmp.gitbook.io/omniagent/
* (버튼 있는경우) 버튼 예시 :&#x20;
  * 버튼타입 : 메시지전달-MD
  * 버튼명 : 메시지확인

{% code title="alimtalk-AT, nobutton" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, kko_msg_type, kko_content, kko_sender_key, kko_template_code) 
values (sq_msg_tran_01.nextval, 'alimtalk', sysdate, '발신번호', '수신번호', 'AT', 'Test Message 입니다.', 'aaaaa22222bbbbb33333ccccc44444ddddd55555', 'INFO_001');
```
{% endcode %}

{% code title="alimtalk-AT, button" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, kko_msg_type, kko_content, kko_sender_key, kko_template_code, kko_option) 
values (sq_msg_tran_01.nextval, 'alimtalk', sysdate, '발신번호', '수신번호', 'AT', 'Test Message 입니다.', 'aaaaa22222bbbbb33333ccccc44444ddddd55555', 'INFO_001', 
'{
  "attachment" : {
    "button":[
      {
		"name": "확인하기",
		"type": "AL",
		"schemeAndroid": "daumapps://open",
		"schemeIos": "daumapps://open"
      }
    ]
  }
}');
```
{% endcode %}

{% code title="alimtalk-AI, nobutton" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, kko_msg_type, kko_content, kko_sender_key, kko_template_code) 
values (sq_msg_tran_01.nextval, 'alimtalk', sysdate, '발신번호', '수신번호', 'AI', 'Test Message 입니다.', 'aaaaa22222bbbbb33333ccccc44444ddddd55555', 'INFO_001');
```
{% endcode %}

{% code title="alimtalk-AI, button" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, kko_msg_type, kko_content, kko_sender_key, kko_template_code, kko_option) 
values (sq_msg_tran_01.nextval, 'alimtalk', sysdate, '발신번호', '수신번호', 'AI', 'Test Message 입니다.', 'aaaaa22222bbbbb33333ccccc44444ddddd55555', 'INFO_001',
'{
  "attachment" : {
    "button":[
      {
         "name":"배송조회",
         "type":"DS"
      },
      {
        "name": "웹링크",
        "type": "WL",
        "urlPc": "https://soldevteam-tmp.gitbook.io/omniagent/",
        "urlMobile": "https://soldevteam-tmp.gitbook.io/omniagent/"
      }
    ]
  }
}');
```
{% endcode %}

{% code title="friendtalk-FT, nobutton" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, kko_msg_type, kko_content, kko_sender_key) 
values (sq_msg_tran_01.nextval, 'friendtalk', sysdate, '발신번호', '수신번호', 'FT', 'Test Message 입니다.', 'aaaaa22222bbbbb33333ccccc44444ddddd55555');
```
{% endcode %}

{% code title="friendtalk-FI, nobutton" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, kko_msg_type, kko_content, kko_sender_key, kko_option) 
values (sq_msg_tran_01.nextval, 'friendtalk', sysdate, '발신번호', '수신번호', 'FI', 'Test Message 입니다.', 'aaaaa22222bbbbb33333ccccc44444ddddd55555',
'{
  "attachment":{
    "image": {
      "imgUrl" : "발급받은이미지",
      "imgLink" : "이미지연결링크"
    }
  }
}');
```
{% endcode %}

{% code title="friendtalk-FW, nobutton" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, kko_msg_type, kko_content, kko_sender_key, kko_option) 
values (sq_msg_tran_01.nextval, 'friendtalk', sysdate, '발신번호', '수신번호', 'FW', 'Test Message 입니다.', 'aaaaa22222bbbbb33333ccccc44444ddddd55555',
'{
  "attachment":{
    "image": {
      "imgUrl": "발급받은이미지",
      "imgLink": "이미지연결링크"
    }
  }
}');
```
{% endcode %}
