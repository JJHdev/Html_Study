## 1.html 작업.
-- 로컬 디스크에 wbstudy > webwk 파일 만들기 
https://code.visualstudio.com/download 홈페이지 들어가기 >  환경에 맞는 프로그램 다운로드. 
한글 패치하기 (프로그램 안에korean 검색후 설치)
live server(riwick dey) > 설치하기. > open in 설치
파일 > 작업영역에 폴더추가 하기 (c드라이버에 원하는 파일 만들어서 진행) > html 작업환경 맞추기

 * elements    : 요소
 * attributes  : 
 * <> : tag라고 한다.
 * <h1> : h1은 테그이름 첫 헤드 </h1> (스타트테그부터 엔드테그까지 합쳐서 요소라고한다.)
 * <p> 첫 문장 </p>
 * 



## 2. html 코드 

#### 2-1. 줄,태그
```
<!-- html의 주석문-->
<!-- DOCTYPE은 html의 선언부 부분-->
<!DOCTYPE html>
<html>
    <head>
        <title> 제목 </title>
    </head>
    <body>
        <p>나는 ~~~~ </p><!-- 한문장 다음 줄로 줄바꿈. -->
        ★★★요소는(element)는 start tag와 end tag사이의 모든부분을 의미!!
        <hr/>  <!-- 선을 만들어준다. -->
        <h1>h1태그</h1> <!-- 글자 크기 진하게 써주기. 내려갈수록 크기줄어듬 -->
        <h2>h2태그</h2>
        <h3>h3태그</h3>
        <h4>h4태그</h4>
        <h5>h5태그</h5>
        <h6>h6태그</h6>

        첫 번째 줄~ <br/><br/> <!-- 여러번 사용하면 줄 계속 바뀐다. -->
        <p/> <!--empty tag -->
        <p></p> <!-- 여러번 사용해도 줄크기가 늘어나진 않는다. -->
        두 번째 줄~~


    </body>
</html>
```

#### 2-2. 문체
```
<!DOCTYPE html>
<html>
    <head>
        <title> 제목 </title>
    </head>
    <body>
        보통
        <b>진하게</b>   
        <strong>진하게</strong> 
        <!-- 중요도를 높이고 싶다면 strong를 사용한다. -->
        <!-- 화면리더기에서는 strong태그의 의미를 파악할수 있다. -->
        <i>기울임i</i>
        <em>기울임em</em>
        <!--중요도를 높이고 싶다면 em을 사용한다-->
        <!-- 화면리더기에서는 em의 의미를 파악할수 있다. -->
        <u>밑줄</u>

        <hr/>
        <pre><!--프리뷰 결과가 직접 줄바꾼것도 바뀌어서 보여지는것-->
            <b>진하게</b>   
            <strong>진하게</strong> 
            <!-- 중요도를 높이고 싶다면 strong를 사용한다. 시멘틱요소 -->
            <!-- 화면리더기에서는 strong태그의 의미를 파악할수 있다. -->
            <i>기울임i</i>
            <em>기울임em</em>
            <!--중요도를 높이고 싶다면 em을 사용한다-->
            <!-- 화면리더기에서는 em의 의미를 파악할수 있다. -->
            <u>밑줄</u>
            <mark>mark태그</mark> <!--형광팬 표시.-->
        </pre>
        <hr/>
        <xmp> <!--코드가 보여지는것-->
            <b>진하게</b>   
            <strong>진하게</strong> 
            <!-- 중요도를 높이고 싶다면 strong를 사용한다. 시멘틱요소 -->
            <!-- 화면리더기에서는 strong태그의 의미를 파악할수 있다. -->
            <i>기울임i</i>
            <em>기울임em</em>
            <!--중요도를 높이고 싶다면 em을 사용한다-->
            <!-- 화면리더기에서는 em의 의미를 파악할수 있다. -->
            <u>밑줄</u>
        </xmp>

    </body>
</html>
```


#### 2-3. 목록, 색상, 목록에 이미지넣기.
```
<!DOCTYPE html>
<html lang="ko"><!--한국어 사용-->
    <head>
        <title> 제목 </title>
        <meta charset="utf-8">
        <!--html주석문-->
        <!-- internal방식 : head태그내부에 style선언-->
        <style>
            /* css의 주석문 */
            /*selecter {property:value;}*/
            /* 선택자  {속성:값;}*/
            /* 태그 html문서안의 모든 지정태그에 적용*/
            body{background-color:rgb(166, 168, 179); color:rgb(44, 16, 16)}
       
            ul{list-style-type: circle;}
            /* #id명 html문서안의 특정id명을 가진 태그에 적용*/
                li#i1{list-style-type:circle; color:rgb(211, 42, 42)}
                li#i2{background-color: blueviolet;}
                li#i3{color:chartreuse}
                #i4{background-color: coral;}
                #i5{list-style-type: decimal;}
                #i6{list-style-type: upper-alpha;}
                #i7{list-style-type: lower-alpha;}
                #i8{list-style-type: upper-roman;}
                #i9{list-style-type: lower-roman;}
                #i{list-style-image:url('ab.gif');}

            /* html문서안의 모든 ol에 공통적인 list-style-type:decimal
               기본 숫자서식  */
            ol{list-style-type: decimal-leading-zero;}

        </style>
   
    </head>
    <body>
        <h2>ul태그1</h2>
        <!-- css목록스타일 (p247) -->
            <ul>  <!--unorder list 순서없는 점으로 앞에 목록표현-->
                <li style="list-style-type:none;">블릿없애기.</li>
                <li style="color: red;">빨강</li>
                <!-- attribute name type, attribute value "값" -->
                <li type="circle">노랑</li>
                <li type="square">주황</li>
                <!-- type attribute default값은 disc -->
                <li type="disc">초록</li>
                <li type="a">파랑</li>
            </ul>
        <!--inline방식 : 태그에 style속성에 서식적용-->
        <hr/>
        <hr style="border-color:rgb(255, 0, 0);"/>

        <h2>ol태그1</h2>
            <ol id="i4"> <!--order list순서있는 숫자로 앞에 목록표현-->
                <li >15억 집(type="1"기본)</li>
                <li type="A">비싼차(type="A")</li>
                <li type="a">돈(type="a")</li>
                <li type="I">행복(type="I")</li>
                <li type="i">사랑(type="i")</li>
            </ol>
        <hr/>
             <dl>
                <dt>HTML</dt><!--첫문장-->
                    <dd>Hypter Text Markup Language.</dd><!--내어쓰기-->
                <dt>CSS</dt>
                    <dd>Cascading Style Sheet</dd>
                    <dd>웹문서의 서식담당</dd>
             </dl>   
        <hr/>
        <hr style="border-color:darkred;"/>

        <h2>ul태그2</h2>
        <!-- css목록스타일 (p247) -->
            <ul>  <!--unorder list 순서없는 점으로 앞에 목록표현-->
                <li >빨강</li>
                <!-- attribute name type, attribute value "값" -->
                <li id="i1">노랑</li>
                <li id="i2">주황</li>
                <!-- type attribute default값은 disc -->
                <li id="i3">초록</li>
                <li>파랑</li>
            </ul>
        <hr/>
        <hr style="border-color:rgb(77, 20, 20);"/>

        <h2>ol태그2</h2>
        <ol> <!--order list순서있는 숫자로 앞에 목록표현-->
            <li id="i5">15억 집</li>
            <li id="i6">비싼차</li>
            <li id="i7">돈</li>
            <li id="i8">행복</li>
            <li id="i9">사랑</li>
        </ol>

        <h2>블릿대신 이미지 넣기(p249)</h2>
        <ul id="i">
            <li>회사소개</li>
            <li>로그인</li>
            <li>이메일</li>
            <li>사이트맵</li>           
        </ul>
    </body>
</html>
```
