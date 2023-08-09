---
description: RCS 상세 메시지 타입 별 예제입니다.
---

# 메시지 타입 별 예제(Oracle)

{% code title="standalone, rcs_msgbase_id: SS000000" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_content, rcs_msgbase_id) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', '문자내용', 'SS000000');
```
{% endcode %}

{% code title="standalone, rcs_msgbase_id: SL000000" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'SL000000', 
'{ 
  "standalone": { 
    "title": "RCS 제목",
    "text": "rcs-standalone-SL000000 RCS LMS 문자 테스트입니다."
  }
}');
```
{% endcode %}

{% code title="standalone, rcs_msgbase_id: SMwThT00" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'SMwThT00', 
'{ 
  "standalone": { 
    "title": "RCS 제목",
    "text": "rcs-standalone-SMwThT00 RCS MMS 문자 테스트입니다.",
    "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
    "button": [
      {
        "type": "URL",
        "name": "버튼이름",
        "url" : "http://www.infobank.net"
      }
    ]
  }
}');
```
{% endcode %}

{% code title="standalone, rcs_msgbase_id: SMwThM00" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'SMwThM00', 
'{ 
  "standalone": { 
    "text": "rcs-standalone-SMwThM00 RCS MMS 문자 테스트입니다.",
    "button": [
      {
        "type": "URL",
        "name": "버튼이름",
        "url" : "http://www.infobank.net"
      }
    ]
  }
}');
```
{% endcode %}

{% code title="template-free, rcs_msg_base_id: UBR.JSUUE931f5-GG000F" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'UBR.JSUUE931f5-GG000F', 
'{ 
  "template": { 
    "description": "rcs-standalone-free UBR.JSUUE931f5-GG000F RCS 문자 테스트입니다.",
    "button": [
      {
        "type": "URL",
        "name": "버튼이름",
        "url" : "http://www.infobank.net"
      }
    ]
  }
}');
```
{% endcode %}

{% code title="template-description, rcs_msg_base_id: UBR.JSUUE931f5-Deposit20191220" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'UBR.JSUUE931f5-Deposit20191220', 
'{ 
  "template": { 
    "description": "rcs-standalone-description UBR.JSUUE931f5-Deposit20191220 RCS 문자 테스트입니다. 인포뱅크 고객님,\n회원가입을 축하드립니다",
    "button": [
      {
        "type": "URL",
        "name": "버튼이름",
        "url" : "http://www.infobank.net"
      }
    ]
  }
}');
```
{% endcode %}

{% code title="template-cell, rcs_msg_base_id: UBR.JSUUE931f5-ProductOrder20191220" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'UBR.JSUUE931f5-ProductOrder20191220', 
'{ 
  "template": { 
    "description": "rcs-standalone-free UBR.JSUUE931f5-GG000F RCS 문자 테스트입니다.",
    "product":"상품명", 
    "value":"1건",
    "button": [
      {
        "type": "URL",
        "name": "버튼이름",
        "url" : "http://www.infobank.net"
      }
    ]
  }
}');
```
{% endcode %}

{% code title="carousel, rcs_msg_base_id: CMwMhM0300" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'CMwMhM0300', 
'{ 
  "carousel": [
    { 
      "title": "RCS 제목(card1)",
      "text": "rcs-standalone-CMwMhM0300 RCS 캐로셀 문자 테스트입니다.(card1)",
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
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
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
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
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    }
  ]
}');
```
{% endcode %}



{% code title="carousel, rcs_msg_base_id: CMwMhM0400" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'CMwMhM0400', 
'{ 
  "carousel": [
    { 
      "title": "RCS 제목(card1)",
      "text": "rcs-standalone-CMwMhM0400 RCS 캐로셀 문자 테스트입니다.(card1)",
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
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
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
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
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
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
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    }
  ]
}');
```
{% endcode %}



{% code title="carousel, rcs_msg_base_id: CMwMhM0500" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'CMwMhM0500', 
'{ 
  "carousel": [
    { 
      "title": "RCS 제목(card1)",
      "text": "rcs-standalone-CMwMhM0500 RCS 캐로셀 문자 테스트입니다.(card1)",
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
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
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
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
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
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
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
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
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    }
  ]
}');
```
{% endcode %}



{% code title="carousel, rcs_msg_base_id: CMwMhM0600" overflow="wrap" fullWidth="true" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, rcs_msgbase_id, rcs_content) 
values (sq_msg_tran_01.nextval, 'rcs', sysdate, '발신번호', '수신번호', 'CMwMhM0600', 
'{ 
  "carousel": [
    { 
      "title": "RCS 제목(card1)",
      "text": "rcs-standalone-CMwMhM0600 RCS 캐로셀 문자 테스트입니다.(card1)",
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
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
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
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
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
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
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
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
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
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
      "fileKey": "test_951eb68af1894ed98a66f0226fed5f20",
      "button": [
        {
          "type": "URL",
          "name": "버튼이름",
          "url" : "http://www.infobank.net"
        }
      ]
    }
  ]
}');
```
{% endcode %}

