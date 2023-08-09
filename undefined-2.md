---
description: OmniAgent를 설치한 후의 directory 구조입니다.
---

# 디렉토리 구조

```shell
OMNI_HOME
|   encrypt
|   faq
|   history
|   logTailer
|   omni
|   omnisvc
|   readme
|   uninstall
+---attach_file
|   +---mms
|   \\---rcs
+---classes
|   \\---mapper
|       +---db2
|       |       common.xml
|       |       msg.xml
|       |
|       +---maria
|       |       common.xml
|       |       msg.xml
|       |
|       +---mssql
|       |       common.xml
|       |       msg.xml
|       |
|       +---mysql
|       |       common.xml
|       |       msg.xml
|       |
|       +---oracle
|       |       common.xml
|       |       msg.xml
|       |
|       +---postgre
|       |       common.xml
|       |       msg.xml
|       |
|       \\---tibero
|               common.xml
|               msg.xml
|
+---config
|       dbConfig.yml
|       logback.xml
|       msgConfig.yml
|
+---lib
|       omniAgent-1.0.0-SNAPSHOT.jar
|       jdbc Jars
|
+---logs
\\---src
```

* encrypt: 암호화 유틸 실행 모듈
* faq: OmniAgent 설치 시, 또는 운영 중 자주 질문되는 내용을 요약한 파일
* history: Agent 버전 별 수정사항을 요약한 파일
* logTailer: log 파일을 분석하여 worker 성능 측정 유틸 실행 모듈
* omni: OmniAgent  설치 시 테스트용 실행 모듈
* omnisvc: OmniAgent  실행 모듈
* readme
* uninstall: 삭제 시 실행 모듈
* attach\_file:  file\_upload scheduler를 통해 mms, rcs 파일키 발급 및 사용시  첨부파일이 존재하는 폴더
* classes-mapper: OmniAgent에서 동작하는 db별xml 파일이 존재하는 폴더
* config: OmniAgent 설정파일이 포함된 폴더
* lib: OmniAgent에서 사용하는 라이브러리가 포함된 폴더
* logs: 로그파일이 생성되는 폴더
* src: callback 소스가 포함된 폴더
