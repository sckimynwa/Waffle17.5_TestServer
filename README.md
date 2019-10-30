# Waffle17.5_TestServer

WaffleStudio17.5 Rookies Final Assignment Test Server


> ## 와플 스튜디오 Rookies 마지막 과제를 위한 TestServer입니다
테스트 서버는 Express.js. Postgresql, Typeorm을 이용하여 구현하였습니다.




> ## 로컬 환경에 서버 구축하기




### 1. 로컬 저장소(노트북 등)의 적절한 위치에 위 저장소를 git clone 해줍니다.
 
 >- Terminal 명령어 git clone https://github.com/sckimynwa/Waffle17.5_TestServer.git
 

### 2. Waffle17.5_TestServer폴더 안에서 npm install을 해줍니다. (터미널 명령어로)



### 3. postgresql을 다운받아줍니다. 
  
  >- https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-18-04 참고
  >- 다운받을 때에 username과 port를 잘 유의하여 지정해주시기 바랍니다.
  >- port의 경우 기본 속성은 5432번을 사용합니다.
  
  
  
### 4. express server와 postgresql을 연결해줍니다. 
  
  >- clone받은 경로로 들어가 ormconfig.json파일을 찾고, 3에서 설정해준 port와 username, password로 수정해줍니다. 
  >- ormconfig.json 파일에 보면 "database": "waffle"이라고 되어 있는데, 이는 서버가 연결할 데이터베이스의 이름이 "waffle"이라는 뜻입니다. 다른 이름을 사용하고 싶을 경우에, 다른 데이터베이스 이름을 사용해도 상관없습니다. 다만, 해당 이름을 가진 데이터베이스가 로컬 환경에 존재해야 합니다.
  
  
  
### 5. database를 생성해 줍니다.

 >- postgresql이 정상적으로 설치된 상태에서 터미널에 psql를 치면 '#'로 시작하는 콘솔창이 열립니다. 이 콘솔창 위에 CREATE DATABASE waffle이라고 입력해 줍니다. 
 >- 로컬에 생성된 후에 '#'로 시작하는 콘솔창이 유지된 상태에서 \list를 입력하면 생성된 모든 데이터베이스의 목록을 확인할 수 있습니다.
 >- \q를 입력하면 psql의 콘솔창을 종료하게 됩니다.
 
 
 ### 6. 모든 설정이 끝났습니다. 
 
 >- 이제 다시 Waffle17.5_TestServer디렉토리로 돌아가서 콘솔창에 tsc를 입력해줍니다. (typescript파일을 javascript로 컴파일해주는 명령어)
 >- 그 후에 콘솔창에 node src/app.js를 입력해 줍니다. 
 >- 데이터 베이스의 기본 쿼리들 SELECT * FROM .... 이 나오면 성공한 것입니다.
 
 * https://github.com/typeorm/typeorm/blob/master/docs/example-with-express.md 참고
 
 
 Insomnia, Postman등의 서비스를 통해 localhost:3000/users등의 주소로 get이나 post명령을 요청하게 되면 정상적인 응답이 되돌아 올 것입니다.
 
 
 
 > ## 데이터베이스 정의
 
 위의 과정이 성공한 후에 터미널에 psql waffle을 입력하게 되면 waffle라는 이름을 가진 데이터베이스를 조회할 수 있게 됩니다.
 데이터 베이스 조회 및 여러 명령어는 아래 링크를 참고해 주세요

https://dbrang.tistory.com/749
