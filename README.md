# test

✨~ test ~ repository ~ ~~~✨

<br>

**React.js - Spring Boot 통신 테스트 및 빌드 성공**

<img src = "/images/success.png">

<br>
<br>

<h3><a href = "https://velog.io/@u-nij/Spring-Boot-React.js-%EA%B0%9C%EB%B0%9C%ED%99%98%EA%B2%BD-%EC%84%B8%ED%8C%85">참고 블로그</a></h3>

<br><br>

**간단 정리**

1. React 설치 <br>
   **cd src/main** <br>
   **npx create-react-app frontend** <br>
   ==> 이후 frontend 폴더가 생성됨.

<br>

2. Spring Boot - React 연동 <br>
   Proxy 설정 : src/main/frontend 폴더에서 계속 작업 <br>
   **npm install http-proxy-middleware --save** <br>
   <br>src/main/frontend/src에 setProxy.js 파일 생성, 코드 붙여넣기 (이건 코드 복붙 참고하기)<br>
   => 이렇게 하면 프론트엔드에서 '/api'로 요청을 보내면 백엔드가 설정한 포트로 요청이 도착함

<br>

3. Axios를 이용한 서버 통신 <br>
   **프론트엔드** <br>
   src/main/frontend/src/App.js의 내용을 지우고 위 파일에 맞게 코드 붙여넣기 (확인용 코드)
   <br><br>
   **백앤드** <br>
   Controller 패키지를 생성하고, TestController.java 파일을 만들어주기. 코드는 위 파일에 맞게 붙여넣기 (확인용)

<br>

4. 확인하기 <br>
   npm start로 리액트도 실행시키고, 스프링 프로젝트를 빌드하고 실행하면서 localhost에 들어가 잘 통신이 되었는지 확인한다.

<br>

5. 빌드하기 <br>
   (build.gradle 주석 아래부분을 참고..) <br>
   build.gradle 파일 하단에 코드를 추가하기 <br>
   **SpringBoot 프로젝트가 build 될 때 React 프로젝트가 먼저 build되고, 결과물을 SpringBoot 프로젝트 build 결과물에 포함시킨다는 스크립트**
