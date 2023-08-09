# RCS

* 이미지가 포함된 RCS 메시지를 전송할 경우 사전에 이미지 파일 등록이 필요 합니다. 이미지 생성을 위해서는 '[FILE UPLOAD API](https://omniapi.gitbook.io/omni-api-specification/api-reference/registration/file)' 를 참조해 주세요. (rcs 이미지의 유효기간은 1년 입니다.)

## 메시지 종류

<div align="left">

<figure><img src="../../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

</div>

## 전송 관련 컬럼

### **필수 입력 컬럼**

<table><thead><tr><th width="210.23280423280426">COLUMN</th><th>입력값</th></tr></thead><tbody><tr><td>callback</td><td>발신번호</td></tr><tr><td>rcs_content</td><td><ul><li>rcs 내용 입력정보(json형태) - standalone, carousel, template</li><li>json 형식은 '<a href="https://omniapi.gitbook.io/omni-api-specification/api-reference/send/rcs#content">content_api</a>'를 참고하여 입력하세요.</li></ul></td></tr><tr><td>rcs_brand_key</td><td>생성한 브랜드마다 부여되는 Key</td></tr><tr><td>rcs_msgbase_id</td><td>rcs 메시지베이스 id(템플릿코드)</td></tr></tbody></table>

### **선택 입력 컬럼**

<table><thead><tr><th width="211.37696335078533">COLUMN</th><th>입력값</th></tr></thead><tbody><tr><td>rcs_agency_key</td><td>대행사 key(대행사의 경우 필수 입력 컬럼)</td></tr><tr><td>rcs_option</td><td><ul><li>rcs 옵션 입력정보(json형태) - header, footer</li><li>기타 옵션정보를 입력하는 컬럼입니다.</li><li>groupId, expiryOption, copyAllowed, header, footer, agencyId 옵션을 입력할 수 있습니다.</li><li>type과 description 정보는 '<a href="https://omniapi.gitbook.io/omni-api-specification/api-reference/send/omni#rcs">rcs_api</a>'를 참고하여 입력하세요.</li></ul></td></tr></tbody></table>
