# LOG 설정파일 (logback.xml)

* OMNI Agent는 기본적으로 자바 오픈 소스 로깅 프레임워크인 logback을 사용합니다.

## log level 수정

* \<appender-ref ref="FILE" /> 의 "" 부분을 수정하여 log level 을 수정할 수 있습니다.
* LEVEL
  * FILE: info
  * DEBUG: debug
  * ERROR: error

```
...
<root level="INFO">
	<appender-ref ref="STDOUT" />
	<appender-ref ref="FILE" />
	<!-- appender-ref ref="ERROR" /-->
	<!-- appender-ref ref="DEBUG" /-->
</root>
```
