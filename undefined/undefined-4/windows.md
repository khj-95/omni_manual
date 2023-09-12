# Windows

## 설치하기

* 설치파일을 더블 클릭하여 실행된 마법사를 따라 설치합니다.\
  ![](<../../.gitbook/assets/image (1).png>)
* OMNI AGENT가 설치될 경로를 설정하고 '다음(N)>' 버튼을 클릭합니다.\
  ![](<../../.gitbook/assets/image (2).png>)
* 바로 가기 버튼을 생성할지, 시작 메뉴 폴더 생성을 안할지 선택 한 후 '다음(N)' 버튼을 클릭합니다.\
  ![](<../../.gitbook/assets/image (3).png>)
* OMNI 계정 아이디와 비밀번호를 입력하고 '다음(N)' 버튼을 클릭합니다. (해당 부분 입력하지 않아도 추후 \~omni설치폴더\conf\msgconfig.yml 파일에서 수정 가능합니다.)\
  ![](<../../.gitbook/assets/image (4).png>)
* 접속할 데이터베이스 종류를 선택하고 데이터베이스 정보들을 입력한 후 '다음(N)' 버튼을 클릭합니다. (해당 부분 입력하지 않아도 추후 \~omni설치폴더\conf\dbconfig.yml 파일에서 수정 가능합니다.)\
  ![](<../../.gitbook/assets/image (5).png>)
* Window 서비스에 등록할지, 부팅 시 시작할지 선택 한 후 '다음(N)' 버튼을 클릭합니다. (서비스 수동 등록 및 삭제를 위해서는 CMD에서 sc create, sc delete 명령어를 이용해 주세요.)\
  ![](<../../.gitbook/assets/image (6).png>)
* 설치가 진행되고 '완료' 버튼을 클릭하여 완료합니다.\
  ![](<../../.gitbook/assets/image (7).png>)

### 선택사항

*   설정 파일에 저장할 접속정보들을 암호화하기 위해 실행하는 파일입니다.\
    omniAgent가 설치된 파일 경로에서 encrypt.exe 파일을 실행합니다.

    <div align="left">

    <figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

    </div>

## 실행하기

* 서비스(제어판>관리도구>서비스, 실행>services.msc)를 사용합니다.
  * 실행(start)\
    \- omnisvc 서비스에서 오른쪽 버튼 클릭 후 '시작(S)'을 클릭합니다.
  * 상태 확인(status)\
    \- omnisvc 서비스의 상태 영역을 확인합니다.\
    \- 상태가 변경되지 않는 경우 omnisvc 서비스에서 오른쪽 버튼 클릭 후 ‘새로 고침(F)’을 클릭합니다.
  * 종료(stop)\
    \- omnisvc 서비스에서 오른쪽 버튼 클릭 후 '중지(O)'를 클릭합니다.\
    \- 종료 명령에도 비정상적인 상태로 종료가 되지 않았을 수 있습니다. 따라서 종료 이후엔 상태 영역을 새로고침하여 확인이 필요합니다.\
    \- 종료가 지속적으로 되지 않을 경우 Windows의 작업관리자 메뉴를 통하여 '작업 끝내기' 명령으로 종료한 뒤 인포뱅크에 문의 하시기 바랍니다.

## 제거하기

* 설치된 경로에서 uninstall.exe를 더블클릭하여 실행된 마법사를 따라 삭제합니다.\
  ![](<../../.gitbook/assets/image (9).png>)
* 삭제가 진행되고 '완료(F)'버튼을 클릭하여 완료합니다.\
  ![](<../../.gitbook/assets/image (10).png>)
