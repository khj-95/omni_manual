---
description: 사용자 함수
---

# callback

* DB에서 Record 검색 후 사용자 함수를 호출할 수 있도록 인터페이스를 정의하여 제공하고 있습니다.
* 아래 함수는 특정 필드의 값을 가공하기 위해 호출되는 프로세스를 정의한 인터페이스 입니다.
* 사용자가 작성한 class파일(JAVA로 컴파일)을 기본경로 혹은 수정된 경로에 복사하여 적용할 수 있습니다.
  * 기본경로: ib.omni.agent.callback.SampleMTTCallback
  * 경로 수정하기: config/msgConfig 파일의 callback.mtt.class configuration을 원하는 경로로 변경
* 주로 수신번호, 메시지를 암호화하여 사용하거나, 값을 변경하여 전송하고자 할 경우 사용 할 수 있습니다.

### interface

<pre class="language-java"><code class="lang-java"><strong>Boolean doTransform(IBUserObject userObject)
</strong></code></pre>

<table><thead><tr><th width="173">doTransform</th><th>전송 데이터 조회 후 변환된 데이터를 return 받기 위해 호출되는 메소드</th></tr></thead><tbody><tr><td>Parameter</td><td>userObject: 참조 개체<br>채널 별 content, 수신번호, mms 제목을 포함하여 그 외의 여분 필드 10개</td></tr><tr><td>Return</td><td>boolean</td></tr><tr><td>class#method</td><td>ib.omni.agent.util#getMaskingPersonalInfo(String): LOG에 수신 번호 표출 시 마스킹 처리</td></tr></tbody></table>
