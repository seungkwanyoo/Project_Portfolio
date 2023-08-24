1. FinalProject_3Team_ONECOIN_STS.zip 파일의 압축을 푼다.
 1-1) cmd 창을 열어서 sqlplus system 계정으로 접속합니다.
      create user one identified by one;
      grant connect,resource,dba to one;
      conn one/one;
      show user;
      입력합니다.
 1-2) Oracle SQL Developoer를 실행하여 사용자 이름에 one 비밀번호에 one SID에 orcl을 입력하고 테스트를 누릅니다
      테스트가 성공하면 저장 후 one계정에 접속 합니다. 2번 sql 파일을 불러오신 후 ctrl+A ctrl+Enter 합니다.
 1-1) src-> main -> webapp -> WEB-INF -> spring -> root.context.xml 파일에 DataBase의 아이디/비밀번호를 확인한다.
 1-1) ONECOIN_STS (오른쪽마우스)-> Run As -> Run on Server 클릭하여 서버를 구동시킨다.

2. FinalProject_3Team_ONECOIN_ReactBackEnd 의 압축을 푼다.
 2-1) src -> resources -> application.properties 파일을 클릭후 아래 사항을 확인해준다.
	① server.port = 9008
	② spring.datasource.username = one 
	③ spring.datasource.password = one
	③ spring.jpa.hibernate.ddl-auto = update
 2-2) Run As -> Spring Boot App 클릭하여 서버를 구동시킨다.

3. FinalProject_3Team_ONECOIN_ReactFrontEnd 의 압축을 푼다.
 3-1) 위 상단에 Terminal 클릭 New Terminal 클릭 후 하단 오른쪽에 + 버튼을 눌러 command Prompt(cmd)를 선택해준다
 3-2) 파일경로(cd..)를 찾아 들어간후 npm install 입력하여 module을 설치해준다.
 3-3) 설치가 끝나면 package.json 파일에 "proxy":"http://localhost:9008"를 추가해준다.
 3-4) Terminal의 command Prompt(cmd)에서 npm start로 서버를 구동시켜준다.

4. FinalProject_3Team_ONECOIN_Android_Backend 의 압축을 푼다.
 4-1) src -> resources -> application.properties 파일을 클릭후 아래 사항을 확인해준다.
	① server.port = 9003
	② spring.datasource.username = one 
	③ spring.datasource.password = one
	③ spring.jpa.hibernate.ddl-auto = update 
 4-2) Onecoin_SpringBoot_AndroidApp (오른쪽마우스) -> Run As -> Spring Boot App 클릭하여 서버를 구동시킨다.

5. FinalProject_3Team_ONECOIN_Android_Frontend 의 압축을 푼다.
 5-1) app-> java -> com.androidstudy.toolbarscrollviewexample 안에 있는 MainActivity, SignUpActivity 파일의 내용을 아래와 동일한지 확인해준다.
	① MainActivity 68번째 줄 retrofit.baseUrl("http://192.168.0.48:9003/")	본인의 ip 입력
	② SignUpActivity 60번째 줄 retrofit.baseUrl("http://192.168.0.48:9003/")본인의 ip 입력


※안드로이드 앱은 따로 볼 필요 없다고 하시면 Android_Frontend와 Android_Backend 파일을 안받으시거나 압축해제 안하셔도 됩니다.

6. STS를 Run as하여서 사이트에 접속하셨으면 admin/1234 로 로그인을 합니다.
강의영상 메뉴에서는 'SPRING 배우고싶은사람 모여라' 에서 'Spring security'에 마우스를 대시면 '유승관선생님'이 뜹니다.
현재 이 페이지에서는 이 부분만 링크 연결이 되어있으니  'Spring securtiy'를 누르시면 상품 상세페이지로 넘어갑니다.












