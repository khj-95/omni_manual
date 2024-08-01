---
description: 메시지 별로 순차 Fallback 처리해주는 통합메시지를 전송합니다
---

# 통합 메시지 전송하기

* channel\_order 컬럼에 담긴 메시지 순서( ',' 으로 구분)대로 전송 처리합니다.
* 첫번째 channel 실패 시 다음 메시지로 Fallback 처리 됩니다.
* 예시\
  channel\_order 컬럼 값: alimtalk,rcs,sms\
  alimtalk 실패 시 rcs 발송. rcs 실패 시 sms 발송
* DB에 데이터 입력 시 각각의 채널 전송에 필요한 데이터를 모두 기입하셔야 합니다. ([채널 별 전송하기](undefined-1/) 참조)
* 전송 시 최대 2개 채널의 Fallback이 가능합니다. (총 3개)

## 예제(Oracle)

{% code title="alimtalk 실패 시 sms 발송 (alimtalk,sms)" overflow="wrap" fullWidth="false" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, kko_msg_type, kko_content, kko_sender_key, kko_template_code, mt_content) 
values (sq_msg_tran_01.nextval, 'alimtalk,sms', sysdate, '발신번호', '수신번호', 'AT', 'alimtalk-AT-nobutton 버튼 없는 알림톡 문자 테스트입니다.', '발신프로필키', '템플릿코드', 'sms 문자 테스트입니다.');
```
{% endcode %}

{% code title="alimtalk 실패 시 rcs 발송. rcs 실패 시 sms 발송 (alimtalk,rcs,sms)" overflow="wrap" fullWidth="false" %}
```sql
insert into msg_tran(client_key, channel_order, request_date, callback, recipient, kko_msg_type, kko_content, kko_sender_key, kko_template_code, rcs_content, rcs_msgbase_id, rcs_brand_key, mt_content) 
values (sq_msg_tran_01.nextval, 'alimtalk,rcs,sms', sysdate, '발신번호', '수신번호', 'AT', 'alimtalk-AT-nobutton 버튼 없는 알림톡 문자 테스트입니다.', '발신프로필키', '템플릿코드', 'RCS_content입력', 'RCS메시시베이스ID(템플릿코드)', 'RCS브랜드키', 'sms 문자 테스트입니다.(RCS 페일백)');
```
{% endcode %}
