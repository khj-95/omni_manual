---
description: alimtalk, friendtalk 전송 시 공통 입력 컬럼에 대한 상세 설명입니다.
---

# ALIMTALK, FRIENDTALK

## 메시지 종류(msg\_type)

* AT: 알림톡
* AI: 알림톡이미지
* FT: 친구톡
* FI: 친구톡 이미지
* FW: 친구톡 와이드 이미지

## 공통

### **필수 입력 컬럼**

<table><thead><tr><th width="200.12060301507535">COLUMN</th><th>입력값</th></tr></thead><tbody><tr><td>kko_msg_type</td><td>카카오 메시지 타입(알림톡-AT,AI 친구톡-FT,FI,FW)</td></tr><tr><td>kko_content</td><td>카카오 내용 입력정보</td></tr><tr><td>kko_sender_key</td><td>카카오 발신 프로필 키</td></tr></tbody></table>

## ALIMTALK

### **필수 입력 컬럼**

<table><thead><tr><th width="203.12060301507535">COLUMN</th><th>입력값</th></tr></thead><tbody><tr><td>kko_template_code</td><td>알림톡 메시지 유형 템플릿 코드</td></tr></tbody></table>

### **선택 입력 컬럼**

<table><thead><tr><th width="204.12060301507535">COLUMN</th><th>입력값</th></tr></thead><tbody><tr><td>kko_option</td><td><ul><li>카카오 옵션 입력정보(json형태) - 강조문구, 버튼</li><li>기타 옵션정보를 입력하는 컬럼입니다.</li><li>title, attatchment, price, currencyType, supplement 옵션을 입력할 수 있습니다.</li><li>옵션의 상세 type과 description은 '<a href="https://infobank-guide.gitbook.io/omni_api/api-reference/send/kakao#alimtalk">alimtalk_api</a>'를 참고하여 입력하세요.</li></ul></td></tr></tbody></table>

## FRIENDTALK

{% hint style="danger" %}
친구톡 서비스는 2024년 12월 31일 종료 예정 입니다.
{% endhint %}

* 이미지가 포함된 친구톡을 전송할 경우 사전에 이미지 파일 등록이 필요 합니다. 이미지 url 생성을 위해서는 '[FILE UPLOAD API](https://omniapi.gitbook.io/omni-api-specification/api-reference/registration/file)' 를 참조해 주세요.

### 선택 입력 컬럼

<table><thead><tr><th width="211.12060301507535">COLUMN</th><th>입력값</th></tr></thead><tbody><tr><td>kko_option</td><td><ul><li>카카오 옵션 입력정보(json형태) - 강조문구, 버튼</li><li>기타 옵션정보를 입력하는 컬럼입니다.</li><li>adFlag, attatchment옵션을 입력할 수 있습니다.</li><li>type과 description 정보는 '<a href="https://infobank-guide.gitbook.io/omni_api/api-reference/send/kakao#friendtalk">friendtalk_api</a>'를 참고하여 입력하세요.</li></ul></td></tr></tbody></table>
