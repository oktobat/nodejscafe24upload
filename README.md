# nodejscafe24upload

npm install
npm start 로컬에서 확인한 후에

MySql 외부 IP 접근설정하기
카페24 서비스 사용현황에서 본인 컴퓨터 ip 등록하기(git 업로드하기전 로컬에서 테스트할 때 사용함)
https://help.cafe24.com/cs/cs_faq_view.php?idx=240&page=1&mode=&s_value=&faq_list=35&categoryIdx=35&select_os=&contentNum=20
db.js 파일에서
host : '도메인(예:ysbkey.cafe24app.com)',
user : '카페24 아이디',
password : '데이터베이스 비밀번호',
database : '데이터베이스명은 카페24 아이디와 동일함
로컬에서 카페24 mysql 서버 사용할 수 있음

Public key 관리에서 공용키 등록하기
터미널 Git bash 창에서 ssh-keygen -t rsa -C "키명칭으로 본인이메일주소"
Enter file in which to save the key (/c/Users/nedry/.ssh/id_rsa) : 공용키 저장경로는 기본경로 그냥 엔터
Enter passphrase (empty for no passphrase) : 비밀번호도 빈 값으로 그냥 엔터
동일한 비번 입력하고 한번 더 엔터
C드라이브>사용자 폴더에서 .ssh 폴더에서 id_rsa.pub 파일 열어서 키값 복사하기 ssh-rsa 부터 끝까지 복사한 후에
카페24 Public key 관리창에 등록하고 앱생성관리에서 앱에 key할당하기

깃(git) 통해 소스코드 업로드하기
카페24에 업로드할 때는 파일명을 반드시 web.js 로 할 것(server.js를 web.js로 변경)
모든 경로를 상대경로에서 절대경로로 변경 함 /home/hosting_users/oktobat1235/apps/oktobat1235_ysbkey/web.js
/home/hosting_users/아이디/apps/아이디_앱이름/web.js
PORT 번호는 카페24 앱생성관리에서 확인한 번호로 수정할 것
vsc 터미널창에서 git bash 화면에서 업로드하기

프로젝트 폴더로 이동(https://git-scm.com/book/ko/v2/Git%EC%9D%98-%EA%B8%B0%EC%B4%88-%EB%A6%AC%EB%AA%A8%ED%8A%B8-%EC%A0%80%EC%9E%A5%EC%86%8C)
git init
git add .
git commit -m '커밋메세지'
git remote add 저장소명(영어) 카페24git저장소명(예 oktobat1235@ysbkey.cafe24app.com:oktobat1235_ysbkey )
git remote -v 로 연결확인
git push 저장소명 +master

깃 저장소 확인하기 git remote show
깃 저장소 삭제하기 git remote remove 저장소명








