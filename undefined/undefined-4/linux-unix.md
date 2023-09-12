# Linux/Unix

## 설치하기

*   업로드한 설치 파일(OMNI\_unix\_1.0.0.sh)에 실행 권한을 부여합니다.

    ```bash
    shell> chmod 775 OMNI_unix_1.0.0.sh
    ```
*   매개변수 "-c"를 입력하여 실행 후 설치마법사를 따라 설치합니다.

    ```
    shell> ./OMNI_unix_1.0.0.sh -c
    Starting Installer ...
    컴퓨터에 OMNI을(를) 설치합니다.
    확인 [o, [Enter]], 취소 [c]

    어디에 OMNI을(를) 설치하시겠습니까?
    [**설치경로입력**]

    폴더가 이미 존재합니다. 이 폴더에 설치하시겠습니까?
    예(Y) [1], 아니오(N) [2]

    symlink를 작성하시겠습니까?
    예(Y) [y, [Enter]], 아니오(N) [n]

    OMNI이(가) Symlinks를 작성할 폴더를 선택한 후, "다음"을 클릭하십시오.
    [/usr/local/bin]

    In this step, you configure the OMNI authentication information
    auth.id :
    [**OMNI계정ID**]

    auth.pwd :
    **OMNI계정비밀번호**

    In this step, you configure the Emma service
    Database     **데이터베이스 종류 선택**
    oracle [1, [Enter]]
    mssql [2]
    mysql [3]
    maria [4]
    postgre [5]
    db2 [6]
    tibero [7]

    DB IP:
    [**데이터베이스 접속 주소**]

    DB Port:
    [**데이터베이스 접속 포트번호**]

    DB Name :
    [**데이터베이스 명**]

    DB User :
    [**데이터베이스 접속 계정 명**]

    DB Password :
    **데이터베이스 접속계정암호**

    Oracle/Tibero의 경우,
    TABLE SPACE :
    [**테이블 스페이스명**]

    TABLE-INDEX SPACE :
    [**테이블 인덱스 스페이스명**]
    ```

### 선택사항

*   설정 파일에 저장할 접속정보들을 암호화하기 위해 실행하는 파일입니다.\
    OMNI Agent가 설치된 파일 경로에서 encrypt 파일을 실행합니다.

    ```bash
    shell> ./encrypt
    ```

## 실행하기

*   실행(start)

    ```bash
    shell> ./omnisvc start
    ```
*   상태 확인(status)

    ```bash
    shell> ./omnisvc status
    ```
*   종료(stop)

    ```bash
    shell> ./omnisvc start
    ```

    \- 종료 명령 이후 "Stoppeed."문구가 정상 출력되지 않으면 비정상적인 상태로 종료가 되지 않았을 수 있습니다. 따라서 종료 이후엔 상태 확인 명령어로 확인 작업이 필요합니다.\
    \- 종료가 지속적으로 되지 않을 경우 리눅스 강제 종료 명령어(kill)를 이용하여 종료한 뒤 Infobank에 문의하시기 바랍니다.

## 삭제하기

*   매개변수 "-c"를 입력하여 실행 후 설치마법사를 따라 설치합니다.

    ```bash
    shell> ./uninstall -c

    정말로 OMNI와(과) 구성 요소들을 완전히 제거하시겠습니까?
    예(Y) [y, [Enter]], 아니오(N) [n]

    OMNI 1.0.0 제거 중...
    ```
