# nodejscafe24upload

# link define
http://ysbkey.cafe24app.com/ (  <br>


npm install
npm start 로컬에서 확인한 후에

MySql 외부 IP 접근설정하기
카페24 서비스 사용현황에서 본인 컴퓨터 ip 등록하기(git 업로드하기전 로컬에서 테스트할 때 사용함)
https://help.cafe24.com/cs/cs_faq_view.php?idx=240&page=1&mode=&s_value=&faq_list=35&categoryIdx=35&select_os=&contentNum=20<br><br>
http://hputty.org/<br>
![1545317869](https://user-images.githubusercontent.com/62067363/162691054-603b9ce5-87ec-400a-82e6-08abcbacbec8.jpg)

db.js 파일에서 <br>
host : '도메인(예:ysbkey.cafe24app.com)', <br>
user : '카페24 아이디', <br>
password : '데이터베이스 비밀번호', <br>
database : '데이터베이스명은 카페24 아이디'와 동일함 <br>
로컬에서 카페24 mysql 서버 사용할 수 있음 <br>

카페24 앱을 생성한 후에 publick key 연결하기
1. vsc 터미널 bash 창에서 ssh-keygen -t rsa -C '이메일주소'
2. Enter file in which to save the key (/c/Users/nedry/.ssh/id_rsa) : 공용키 저장경로는 기본경로 그냥 엔터
3. Enter passphrase (empty for no passphrase) : 데이터베이스 비밀번호
4. .ssh 폴더에서 .pub 파일을 메모장에서 열어서 보이는 코드를 전부 복사
5. 카페24 public key 관리에서 공개키 등록
6. 앱생성관리에서 key 할당
7. ![git005](https://user-images.githubusercontent.com/62067363/162690137-20dc5bcb-8fe4-48dd-80cc-9ece7ac75f1e.jpg)


깃(git) 통해 소스코드 업로드하기 <br>
카페24에 업로드할 때는 파일명을 반드시 web.js 로 할 것(server.js를 web.js로 변경) <br>
PORT 번호는 카페24 앱생성관리에서 확인한 번호(주로 8001)로 수정할 것  <br>
모든 경로를 상대경로에서 절대경로로 변경 함 <br>
/home/hosting_users/oktobat1235/apps/oktobat1235_ysbkey/web.js <br>
/home/hosting_users/아이디/apps/아이디_앱이름/web.js  <br><br>


vsc 터미널창에서 git bash 화면에서 업로드하기 <br>
1. 프로젝트 폴더로 이동
2. git init (코드를 수정할때는 .git 폴더를 삭제한 후에)
3. git add .
4. git commit -m '커밋메세지'
5. git remote add 저장소별칭(영어) 카페24git저장소명(예 oktobat1235@ysbkey.cafe24app.com:oktobat1235_ysbkey )
6. git remote -v 로 연결확인
7. git remote show 로 저장소명 확인
8. git push 저장소명 +master 또는 +main
9. 카페24 앱생성관리에서 앱 실행을 중지한 후 다시 실행








