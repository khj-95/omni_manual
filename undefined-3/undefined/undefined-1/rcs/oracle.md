---
description: RCS 상세 메시지 타입 별 예제입니다.
---

# 메시지 타입 별 예제(Oracle)

### SMS

{% code title="standalone, rcs_msgbase_id: SS000000" overflow="wrap" fullWidth="false" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_content, rcs_msgbase_id, rcs_brand_key) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'rcs-standalone-SS000000 RCS SMS 문자 테스트입니다.', 'SS000000', 'RCS브랜드키');
```
{% endcode %}

### LMS

{% code title="standalone, rcs_msgbase_id: SL000000" overflow="wrap" fullWidth="false" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content, rcs_brand_key) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'SL000000', 
'{ 
  "standalone": { 
    "title": "RCS 제목",
    "text": "rcs-standalone-SL000000 RCS LMS 문자 테스트입니다."
  }
}', 'RCS브랜드키');
```
{% endcode %}

### MMS-TALL IMG

{% code title="standalone, rcs_msgbase_id: SMwThT00" overflow="wrap" fullWidth="false" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content, rcs_brand_key) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'SMwThT00', 
'{ 
  "standalone": { 
    "title": "RCS 제목",
    "text": "rcs-standalone-SMwThT00 RCS MMS 문자 테스트입니다.",
    "media": "발릅받은이미지",
    "button": [
      {
        "type": "URL",
        "name": "버튼이름",
        "url" : "http://www.infobank.net"
      }
    ]
  }
}', 'RCS브랜드키');
```
{% endcode %}

### MMS-MEDIUM IMG

{% code title="standalone, rcs_msgbase_id: SMwThM00" overflow="wrap" fullWidth="false" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content, rcs_brand_key) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'SMwThM00', 
'{ 
  "standalone": { 
    "text": "rcs-standalone-SMwThM00 RCS MMS 문자 테스트입니다.",
    "media": "발릅받은이미지",
    "button": [
      {
        "type": "URL",
        "name": "버튼이름",
        "url" : "http://www.infobank.net"
      }
    ]
  }
}', 'RCS브랜드키');
```
{% endcode %}

### MMS(CAROUSEL), CARD 3

{% code title="carousel, rcs_msg_base_id: CMwMhM0300" overflow="wrap" fullWidth="false" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content, rcs_brand_key) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'CMwMhM0300', 
'{ 
  "carousel": [
    { 
      "title": "RCS 제목(card1)",
      "text": "rcs-standalone-CMwMhM0300 RCS 캐로셀 문자 테스트입니다.(card1)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    },
    { 
      "title": "RCS 제목(card2) ",
      "text": "rcs-standalone-CMwMhM0300 RCS 캐로셀 문자 테스트입니다.(card2)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    },
    { 
      "title": "RCS 제목(card3) ",
      "text": "rcs-standalone-CMwMhM0300 RCS 캐로셀 문자 테스트입니다.(card3)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    }
  ]
}', 'RCS브랜드키');
```
{% endcode %}

### MMS(CAROUSEL), CARD 4

{% code title="carousel, rcs_msg_base_id: CMwMhM0400" overflow="wrap" fullWidth="false" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content, rcs_brand_key) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'CMwMhM0400', 
'{ 
  "carousel": [
    { 
      "title": "RCS 제목(card1)",
      "text": "rcs-standalone-CMwMhM0400 RCS 캐로셀 문자 테스트입니다.(card1)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    },
    { 
      "title": "RCS 제목(card2) ",
      "text": "rcs-standalone-CMwMhM0400 RCS 캐로셀 문자 테스트입니다.(card2)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    },
    { 
      "title": "RCS 제목(card3) ",
      "text": "rcs-standalone-CMwMhM0400 RCS 캐로셀 문자 테스트입니다.(card3)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    },
    { 
      "title": "RCS 제목(card4) ",
      "text": "rcs-standalone-CMwMhM0400 RCS 캐로셀 문자 테스트입니다.(card4)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    }
  ]
}', 'RCS브랜드키');
```
{% endcode %}

### MMS(CAROUSEL), CARD 5

{% code title="carousel, rcs_msg_base_id: CMwMhM0500" overflow="wrap" fullWidth="false" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content, rcs_brand_key) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'CMwMhM0500', 
'{ 
  "carousel": [
    { 
      "title": "RCS 제목(card1)",
      "text": "rcs-standalone-CMwMhM0500 RCS 캐로셀 문자 테스트입니다.(card1)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    },
    { 
      "title": "RCS 제목(card2) ",
      "text": "rcs-standalone-CMwMhM0500 RCS 캐로셀 문자 테스트입니다.(card2)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    },
    { 
      "title": "RCS 제목(card3) ",
      "text": "rcs-standalone-CMwMhM0500 RCS 캐로셀 문자 테스트입니다.(card3)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    },
    { 
      "title": "RCS 제목(card4) ",
      "text": "rcs-standalone-CMwMhM0500 RCS 캐로셀 문자 테스트입니다.(card4)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    },
    { 
      "title": "RCS 제목(card5) ",
      "text": "rcs-standalone-CMwMhM0500 RCS 캐로셀 문자 테스트입니다.(card5)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    }
  ]
}', 'RCS브랜드키');
```
{% endcode %}

### MMS(CAROUSEL), CARD 6

{% code title="carousel, rcs_msg_base_id: CMwMhM0600" overflow="wrap" fullWidth="false" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content, rcs_brand_key) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'CMwMhM0600', 
'{ 
  "carousel": [
    { 
      "title": "RCS 제목(card1)",
      "text": "rcs-standalone-CMwMhM0600 RCS 캐로셀 문자 테스트입니다.(card1)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    },
    { 
      "title": "RCS 제목(card2) ",
      "text": "rcs-standalone-CMwMhM0600 RCS 캐로셀 문자 테스트입니다.(card2)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    },
    { 
      "title": "RCS 제목(card3) ",
      "text": "rcs-standalone-CMwMhM0600 RCS 캐로셀 문자 테스트입니다.(card3)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    },
    { 
      "title": "RCS 제목(card4) ",
      "text": "rcs-standalone-CMwMhM0600 RCS 캐로셀 문자 테스트입니다.(card4)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    },
    { 
      "title": "RCS 제목(card5) ",
      "text": "rcs-standalone-CMwMhM0600 RCS 캐로셀 문자 테스트입니다.(card5)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    },
    { 
      "title": "RCS 제목(card6) ",
      "text": "rcs-standalone-CMwMhM0600 RCS 캐로셀 문자 테스트입니다.(card6)",
      "media": "발급받은이미지",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    }
  ]
}', 'RCS브랜드키');
```
{% endcode %}

### FREE-TEMPLATE

{% code title="template-free, rcs_msg_base_id: UBR.JSUUE931f5-GG000F" overflow="wrap" fullWidth="false" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content, rcs_brand_key) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', '발급받은템플릿아이디', 
'{ 
  "template": { 
    "description": "rcs-standalone-free UBR.JSUUE931f5-GG000F RCS 문자 테스트입니다."
  }
}', 'RCS브랜드키');
```
{% endcode %}

### FREE-DESCRIPTION

{% code title="template-description, rcs_msg_base_id: UBR.JSUUE931f5-Deposit20191220" overflow="wrap" fullWidth="false" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content, rcs_brand_key) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', '발급받은템플릿아이디', 
'{ 
  "template": { 
    "description": "{{n1}} 인증번호 {{n2}}를 입력해주세요."
  }
}', 'RCS브랜드키');
```
{% endcode %}

### FREE-CELL

{% code title="template-cell, rcs_msg_base_id: UBR.JSUUE931f5-ProductOrder20191220" overflow="wrap" fullWidth="false" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content, rcs_brand_key) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', '발급받은템플릿아이디', 
'{ 
  "template": { 
    "description": "iMessage 인증 문자입니다. ",
    "name":"홍길동", 
    "value":"10000000원"
  }
}', 'RCS브랜드키');
```
{% endcode %}
