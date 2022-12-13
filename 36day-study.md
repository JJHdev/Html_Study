## 1. form 정규표현식
워낙에 다양하고 많아서 인터넷에 찾아서 쓰는게 가장 편하다.
```
<!DOCTYPE html>
<html lang="ko">
  <head>
    <title></title>
    <meta charset="utf-8" />
<!--     <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.0/normalize.min.css"
    /> -->
    <style></style>
  </head>
  <body>
    <h2>★★★form(p132)★★★</h2>
    <hr />
    <!--
    https://search.naver.com/search.naver?where=nexearch
    &sm=top_hty
    &fbm=0
    &ie=utf8
    &query=winter


    https://www.google.com/search?
    q=iframe
    &oq=
    &aqs=chrome.1.69i59i450l8.1444671791j0j15
    &sourceid=chrome
    &ie=UTF-8

    http://127.0.0.1:5500/ok.html?userName=%EC%9D%B4%EC%88%9C%EC%8B%A0&nickName=%EC%98%81%EC%9B%85&pwd=123
-->


    <form action="ok.html" method="get">
      <!--<input type="text" name="파라미터명" value="초기값" /> -->
      <fieldset>
      	<legend>개인정보</legend>
      	 <ul>
      	 <!-- require속성은 필수입력 
      	 				autofocus속성은 자동으로 포커스위치
      	 				placeholder속성은 안내용정보제공 클릭후 사라짐.-->
      	<li>
    			 이름:
      			<input  type="text" 		 name="userName"   id="userName"  size="10"  maxlength="10" required="required" autofocus="autofocus" placeholder="이름입력"/>
      	</li>
      	<li>
      		별명:<input type="text" name="nickName" id="nickName" />
      	</li>
      	<li>
      		비번:<input type="password" name="pwd" size="30" required="required" />
      	</li>
      	<li><!--  radio는 단일선택.
      							 checked="checked"
      							 YES를 선택하면  snsYN=Y 
      	              NO를 선택하면  snsYN=N-->
      		sns수신여부(y/n):  
      		<input type="radio" name="snsYN" id="snsY" value="Y" checked="checked"/><label for="snsY">YES</label>
      		<input type="radio" name="snsYN" id="snsN" value="N"/><label for="snsN">NO</label>
      	</li>
      	<li> <!-- 다중선택가능. 
      								checked="checked"
      								여러개를 선택하면
      	 							hobby=game&hobby=sport&hobby=coding&hobby=study
      	 							하나의 hobby변수에  
      	 							동일한 String타입의 
      	 							서로 다른 값value가 저장되므로
      	 							js와 jsp에서는   배열Array로 취급되어 진다-->
      		취미: 
      		<input type="checkbox" name="hobby" id="h0" value="game" checked="checked"/>게임
      		<input type="checkbox" name="hobby" id="h1" value="sport"/>운동
      		<input type="checkbox" name="hobby" id="h2" value="coding"/>코딩
      		<input type="checkbox" name="hobby" id="h3" value="study"/>공부
      		<input type="checkbox" name="hobby" id="h4" value="sleep"/>잠자기
      	</li>
      	<li>
      		<!-- 단일선택시			예>loc=0      loc=newyork
      					 다중선택시   multiple="multiple"  예>loc=newyork&loc=jeju&loc=dockdo
      					 하나의 hobby변수에  동일한 String타입의 
      	 				 서로 다른 값value가 저장되므로
      	 				 js와 jsp에서는   배열Array로 취급되어 진다
      		-->
      		지역
      		<select name="loc" id="loc" size="10" multiple="multiple">
      		  <option value="0">선택</option>   
      			<option value="newyork">뉴욕</option> 
      			<option value="seoul">서울</option>
      			<option value="jeju">제주</option>
      			<option value="pusan">부산</option>
      			<option value="dockdo">독도</option>
      		</select>
      	</li>
      	<li> <!-- imgFile=cake1.jpg  파일자체가 아닌  jsp에서는 문자열로 일단 받는다 -->
      		파일찾기:<input type="file"  name="imgFile" id="imgFile"/>
      	</li>
      	<li> <!--memberNo=9872  개발자에게 필요한 정보를 숨겨서 넘긴다 -->
      		hidden:<input type="hidden"  name="memberNo" id="memberNo" value="9872"/>
      	</li>
      	<li>
      		비고:<textarea name="etc" id="etc" rows="5" cols="5"></textarea>
      	</li>
      	<li>
      		이메일:<input type="email" name="email" id="email" />
      	</li>
      	<li>
      		Site:<input type="url" name="siteUrl" id="siteUrl"/>
      	</li>
      	<li>
      		tel:<input type="tel" name="hp" id="hp"  
      										pattern="[0-9]{3}-[0-9]{3,4}-[0-9]{4}"
      										placeholder="010-1234-1234형식"/>
      	</li>
      </ul> 
      /fieldset>
      
     
     
     <fieldset>
     		<legend>주문정보</legend>
	     <ul>                                                     <!-- proSearch=computer -->
	     	<li>상품검색:<input type="search" name="proSearch" id="proSearch"></li>
	     	<li>주문수량:<input type="number" name="cnt" id="cnt" 
	     																	value="1"  min="0" max="10" step="1"/></li>
	     	<li>
	     		<!-- 크롬,엣지에서는
	     		         최저는 0, 최대는 100 
	     						기본값의 경우 range=50    -->
	     		range:<input type="range" name="range" id="range" 
	     													value="0"  min="0" max="10000" step="2000"				/></li>
				<li><!-- 블랙컬러의 경우  
										크롬,IE엣지 에서는 proColor=%23000000 -->
					color:<input type="color" name="proColor" id="proColor">
				</li>
				<li>
				 <!-- 크롬,IE엣지 에서는
								 orderDate=2022-12-13
								 orderWeek=2022-W50
								 orderMonth=2022-12        
								 datetime은 미지원
								 orderDTLocal=2022-12-13T11%3A19-->
				date:	<input type="date"    name="orderDate"     id="orderDate"/><br/>
				week:	<input type="week"   name="orderWeek"   id="orderWeek"/><br/>
				month:	<input type="month" name="orderMonth" id="orderMonth"/><br/>
				datetime:	<input type="datetime"    name="orderDT"     id="orderDT"/><br/>
				datetime-local:	<input type="datetime-local"    name="orderDTLocal"     id="orderDTLocal"/><br/>
				</li>
					<li>
						진행상태 progress: <progress name="delprogress" id="delprogress" value="7" max="15"></progress>
					</li>
					<li>
						값이 차지하는 크기표시  점유율(0.0~1.0) 사용량(0~100)<br/>
						meter점유율: <meter name=",m1" id="m1" value="0.8" max="1"></meter><br/>
						meter사용량: <meter name="m2" id="m2" value="88" max="100"></meter><br/>
						트래픽초과: <meter name="m3" id="m3" value="88" low="30"  high="70" min="0" max="100"></meter><br/>
						적절한트래픽: <meter name="m4" id="m4" value="50" optimum="50"min="0" max="100"></meter><br/>
				</li>
	     </ul>
     </fieldset>
     	<!-- <input type="image" >은 제출용으로 정의된다 -->
     	<input type="image"  src="images/OIP.jpg">
      <input type="submit" value="확인" />
      <input type="reset" value="취소" />
      <input type="butten" value="버튼" onclick="alert(안녕눈온다);"/>
      <button type="submit" style="border-style:none;"><input type="image"  src="images/OIP.jpg"></button>
      
    </form>
    
    
    
<pre>
form요소 action="요청을 처리할 서버측 문서" 
								method="post | get(기본)"
 *get방식=> 입력한 내용이 주소표시줄에 노출 
  										The length of a URL is limited (2048 characters)
 *post방식=>입력한 내용이 주소표시줄에 노출x. 중요한 데이터 넘길 때 이용
</pre>
  </body>
</html>
```


## 2. 자료 발송및 수신
### 2-1. 클라이언트
```
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>form01 문서</title>
</head>
<body>
	<form name="frm1" id="fim1" method="get"  action="ok.jsp">
		이름: <input type="text" name="mname" id="mname" size="10" maxlength="10" autofocus="autofocus"><br/>
		비번: <input type= "password" name="mpwd" id="mpwd"><br/>
		<input type="submit" name="submit" id="submit"><br/>
	</form>
</body>
</html>
```

###2-2. 서버
```
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>ok</title>
</head>
<body>
	<h3>ok.jsp문서</h3>
	<h4>form01문서에서 user가 입력한 데이터를 받아서 처리하는 서버측 페이지이다.</h4>
	<% /*한줄 주석문*/
			// Scriptlet(시크립트릿) 자바코드를 실행
		/*?mname=hong&mpwd=1234
		    파라미터명이 mname의 값을 가져와 변수에 저장
		    타입 변수명 = 객체참조변수명.메서드명(); 이용*/
				String mname = request.getParameter("mname");
		    String mpwd = request.getParameter("mpwd");
	%>
	
	
	<!-- html 주석문 -->
	<%-- jsp주석문 Expression표현식(<%=%>) 브라우저화면에 출력 --%>
	<!-- 유저가 입력한 데이터 -->
	<ul>
		<li>이름: <%=mname %></li>
		<li>비번: <%=mpwd %></li>
	</ul>
</body>
</html>
```
