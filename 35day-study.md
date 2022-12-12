html link연결
```
<!DOCTYPE html>
<html lang="ko">
  <head>
    <title></title>
    <meta charset="utf-8" />
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css"/>
    <style>
        a {text-decoration: none;} 

        img {
          border-width: 0;
        }

        의사클래스(가상클래스)<br/>
                의사클래스는 선택자에 추가되는 키워드<br/>
                선택한 요소가 특별한 상태여야 만족할 수 있다.
                예) :hover :active :link :visited :checked :focus :
    /* unvisited link 방문전 링크크*/
    a:link {
      color: red;
    }
    /* visited link 방문후 링크*/
    a:visited {
      color: green;
    } 
    /* mouse over link 마우스 올라갔을때*/
    div:hover {
      color: hotpink;
      text-decoration: underline;
    }
    /* selected link 마우스로 누르고있을때*/
    a:active {
      color: blue;
    }
    /* a:hover MUST come after a:link and a:visited
    a:active MUST come after a:hover */
    a:link, a:visited {
  background-color: #f44336;
  line-height: 10px;
  color: white;
  padding: 14px 25px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
}
a:hover, a:active {
  background-color: red;
}
    </style>
  </head>
  <body>

    <pre id ="top">  </pre>
      OIP파일의 
      절대경로 : C:\vswk\images\OIP.jpg
      상대경로 :  images\OIP.jpg
      <a href="images\OIP.jpg" target="_blank">이쁜사진링크</a>
      <a href="https://www.youtube.com/watch?v=qe9tu4oFT_o&t=626s" target="_blank">누르시오</a>
      <a href="https://www.youtube.com/watch?v=qe9tu4oFT_o&t=626s" target="_parent">누르시오</a>
      <a href="https://www.youtube.com/" target="_self">누르시오</a>
      <a href="https://www.google.co.kr/" target="_blank"> <img src="images\images (1).png" alt="곰돌이 사진" title="로고"> </a>
      <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
      <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
      <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
      <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
      <!-- 위에올라가는 링크 -->
      <a href="#top"><span>위에 올라가기</span></a>

      <!-- 
      P294
      inlinelevel : 딱 적용된 자리만 차지한다. 높이 넓이 지정해도 차지한 자리만 잡고있으며, 
      줄바꿈이 없다.
      blocklevel : 한블럭을 차지한다. (hr,p,h1~6,div)/ 높이 넓이 지정하면 그만큼 자리를 차지하고있다. -->
      <h2>링크(106p)</h2>
      - 절대경로와 상대경로 이해하기.
      - 문법 a href="경로및 파일명" target="창뜨는서식"

  </body>
</html>

```

##2. displays 서식
```
<!DOCTYPE html>
<html lang="ko">
    <head>
        <title></title>
        <meta charset="utf-8">
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css">  
   
      <style>

    display : <style>
span.a {  /*인라인성격(같은줄에 표시되면서 칸이 아닌 그냥 글씨로서 역할 (위아래 줄침범가능))*/
  display: inline;  the default for span 
  width: 100px;
  height: 100px;
  padding: 5px;
  border: 1px solid blue;  
  background-color: yellow; 
}

span.b { /*인라인과 블록성격 한줄에 표시되면서 서로 영역 침범 x*/
  display: inline-block;
  width: 100px;
  height: 100px;
  padding: 5px;
  border: 1px solid blue;    
  background-color: yellow; 
}

span.c { /*각자 한줄로서 표현됨. 블록성격.*/
  display: block;
  width: 100px;
  height: 100px;
  padding: 5px;
  border: 1px solid blue;    
  background-color: yellow; 
}
    
.nav {
  background-color: yellow; 
  list-style-type: none;
  text-align: center;
  margin: 0;
  padding: 0;
}

.nav li {
  display: inline-block;
  font-size: 20px;
  padding: 20px;
}

      </style>
   
   
    </head>
    <body>
      <ul class="nav">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About Us</a></li>
        <li><a href="#clients">Our Clients</a></li>  
        <li><a href="#contact">Contact Us</a></li>
      </ul>
    </body>
</html>
```

##3. form ★★★★★
```
<!DOCTYPE html>
<html lang="ko">
    <head>
      <title></title>
      <meta charset="utf-8">
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css">  
      <style>

      </style>
    </head>
    <body>
      <h2>★★★ form(p_132)★★★★</h2>
      <hr/>
      <!-- form요소 action="요청을 처리할 서버측 문서"
      method="post || get(기본)"
      get방식 → 입력한 내용이 주소표시줄에 노출
      post방식 → 입력한 내용이 주소표시줄에 노출x. 중요한 데이터넘길경우 사용 -->
      <!-- 이름:  <input type="내용" name="파라미터명" value="초기값" title="마우스놓으면 선택값" > -->
      <form action="N_ok.html"  method="post">
        이름:  <input type="text" name="username" id="username" value="장" size="10" maxlength="7" title="검색"  >
        <br/><br/>
        별명:  <input type="text" name="nickname" id="nickname" size="10" required="required">
        <br/><br/>
        비번: <input type="password" name="pwd" size="14">
        <input type="submit" value="확인" title="클릭" >
        <input type="reset" value="취소">
      </form>
    </body>
</html>
```

##4. sever 연결

1번 ee설치
1. c드라이버에 webstudy폴더 만들기. 하위에 pg폴더와 webwk(이클립스용 작업폴더)만들기
2. https://www.eclipse.org/downloads/packages/release/2020-03/r 홈페이지에 들어가서 다운로드 (최신버전은 자바 8버전 안해준다.
3. 강의에서는 8버전 지원하는 최신인 2020-03버전을 다운받아서 했다.
4. Eclipse IDE for Enterprise Java Developers (includes Incubating components) 이 버전으로 사용했음. (EE)
5. e클립스 받은거 webstudy에 알집풀기 (알집에서는 안풀려서 반디집으로 풀었음). > 이클립스 바로가기 바탕화면에
2번 톰캣 설치.
1. 톰캣 최신버전받기 (알파버전 제외) > 자바버전 지원하는지 확인하면서. 하기
2. 본 강의에서는 9버전 받기.  download > 9버전 > 32-bit/64-bit Windows Service Installer 이걸로 다운받았음.
3. 1번과 2번 설치한 파일을 webstudy/pg에 보내기
4. 다운받은 톰캣 설치하기.> 계속 설치 후 configuretion 에서 설정 변경. 
5. 이름과 패스워드 작성하고 잘 기억해놓기. 
6. 여기서 아이디: admin 비번은 admin123 으로 했음. , create shortcuts for all users 체크하기. > 설치하기.
7.  설치파일에서 bin에서 startup에서 실행하고 shutdown으로 실행종료

3. 실행하기
 bin 파일에서 startup실행후  http://localhost:8080/index.jsp 인터넷에서 입력 
 만일 아이디 비번이 안들어가지면 전부다 종료 후 conf에서 fort번호 바꾸기 > sever.xml문서를 워드패드로 킨 후 Connector port="8080" 찾은 후
다른 포트번호 입력. > 포트번호만 바꿔서 실행 실습에서는 8087로했음. (개인 서버 만든것임)
이클립스 (서버용) 실행 후 저장위치를 webwk로 지정한다.

4. eclipse ee 환경설정
4-1. window > 환경설정 > 다크모드 > editors > texteditor > displayed tab width 를 2로 설정.
color and fonts 나에게 맞게 설정.
spelling에서 encoding을 utf-8로설정.
web browser에서 use external webbrowser체크 후 크롬설정.
work에서 text fil encoding을 utf-8로 설정.
맨아래에서 web에서 css files에서 encoding을 utf-8로 설정. (html, jsp 전부다 utf-8로설정.)

5. eclipse ee project만들기. 
  file > new > other > web > dynamic web project 만들기. > 프로젝트명 기입 후 new runtime 클릭> apache > tomcat설치버전.
  > tomcat installation directory > 톰캣설치한 폴더에서 톰캣9.0클릭후 선택 > jre는 jdk자바 설치버전 선택 > next 후 맨마지막장에서 generate xml 체크후> finish

  web content에서 폴더 하나 만든 후 html문서 만들기. (여기서 html의 설치 버전을 결정할수 있다.)
  > 내용 입력 후 > 아래 sever창에서 클릭 후 next > finish (서버만 끌어온것.)
  > 실행하면 아마 안될것이다. 그이유는 포트충돌때문이다. 그래서 수동으로 포트를 지정해줄것이다. > 
  > severs 에서 톰캣 설정한것에서 더블클릭 후 > 오른쪽에 보면 톰캣 정렬한 부분이 있다. > tomcat admin port를 8005로 설정
  > 왼쪽 project explorer > servers > server.xml 더블클릭. 포트 볼수있다. (포트번호 바꿀수있다.)

  web content에서 폴더 하나 만든 후 jsp문서 만들기. (여기서 jsp의 설치 버전을 결정할수 있다.)
  > 내용 입력 후 > 아래 sever창에서 클릭 후 next > finish (서버만 끌어온것.)
  > 실행하면 아마 안될것이다. 그이유는 포트충돌때문이다. 그래서 수동으로 포트를 지정해줄것이다. > 
  > severs 에서 톰캣 설정한것에서 더블클릭 후 > 오른쪽에 보면 톰캣 정렬한 부분이 있다. > tomcat admin port를 8005로 설정
  > 왼쪽 project explorer > servers > server.xml 더블클릭. 포트 볼수있다. (포트번호 바꿀수있다.)
