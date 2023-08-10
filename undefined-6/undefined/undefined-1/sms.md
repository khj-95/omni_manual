---
description: SMS 전송
---

# SMS

* SMS 최대 90bytes까지 전송 가능합니다.

## 전송 관련 컬럼

### **필수 입력 컬럼**

<table><thead><tr><th width="190.44444444444446">COLUMN</th><th>입력값</th></tr></thead><tbody><tr><td>callback</td><td>발신번호</td></tr><tr><td>mt_content</td><td>문자 내용 입력정보</td></tr></tbody></table>

### 예제(Oracle)

<pre class="language-sql" data-title="sms" data-overflow="wrap" data-full-width="false"><code class="lang-sql"><strong>insert into msg_tran(client_key, channel_order, request_date, callback, recipient, mt_content) 
</strong>values (sq_msg_tran_01.nextval, 'sms', sysdate, '15882460', '발신번호', 'sms 문자 테스트입니다.');
</code></pre>
