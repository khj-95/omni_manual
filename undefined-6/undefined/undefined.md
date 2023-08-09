---
description: 메시지 전송 시 공통 입력 컬럼에 대한 상세 설명입니다.
---

# 공통

## 전송 관련 컬럼

**필수 입력 컬럼**

<table><thead><tr><th width="189.44444444444446">COLUMN</th><th>설명</th></tr></thead><tbody><tr><td>client_key</td><td><ul><li>클라이언트 메세지의 고유 번호입니다.</li><li>oracle database의 경우 sq_msg_tran_01 시퀀스를 제공하여 nextval() 함수를 통해 client_key를 지정할 수 있습니다.</li></ul></td></tr><tr><td>priority</td><td><ul><li>전송 우선순위를 지정하는 컬럼입니다.</li><li>종류: slow, fast, veryfast</li><li>default 값은 'slow' 입니다.</li><li>priority 별 발송 비율 상세 설정은msgConfig 파일의 collect.priority~, send.priority~ 에서 수정 가능합니다.</li></ul></td></tr><tr><td>channel_order</td><td><ul><li>전송 채널 순서 컬럼입니다.</li><li>OMNI API 기준으로 채널이 구성되어 있습니다.</li><li>종류: sms, mms, alimtalk, friendtalk, rcs, international</li><li>단일발송의 경우, 하나의 채널을 입력 (ex. sms)</li><li>Fallback의 경우, 전송하고자 하는 순서대로 ',' 구분자를 통해 최대 3개의 채널을 입력(ex. rcs,alimtalk,sms)</li><li>국제 발송의 경우 단일발송만 가능합니다.</li></ul></td></tr><tr><td>msg_status</td><td><ul><li>메시지 상태 컬럼입니다.</li><li>1: 발송대기 2: 발송완료 3: 결과 수신 중 4: 결과 수신 완료</li><li>default 값은 '1' 입니다.</li></ul></td></tr><tr><td>request_date</td><td><ul><li>전송 요청 시간 컬럼입니다.</li></ul></td></tr><tr><td>recipient</td><td><ul><li>수신번호 컬럼입니다.</li><li>국제발송의 경우 국제 형식으로 입력합니다. (ex.821000000000)</li></ul></td></tr></tbody></table>

**선택 입력 컬럼**

<table><thead><tr><th width="190.44444444444446">COLUMN</th><th>설명</th></tr></thead><tbody><tr><td>payment_code</td><td><ul><li>정산용 부서코드</li></ul></td></tr><tr><td>agent_id</td><td><ul><li>agent 이중화시 사용되는 id 입니다.</li><li>active-active mode에서 agent를 구분하는 용도로 사용됩니다.</li></ul></td></tr><tr><td>ttl</td><td><ul><li>전송 유효시간 설정 컬럼입니다. (단위, 초)</li><li>default 값은 86400 입니다.</li></ul></td></tr><tr><td>origin_cid</td><td><ul><li>발신자 식별코드 입력 컬럼입니다.</li></ul></td></tr><tr><td>etc_text_1<br>etc_text2<br>etc_text3</td><td><ul><li>유저 기타필드를 입력할 수 있습니다.</li></ul></td></tr></tbody></table>
