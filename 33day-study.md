## 1. css사용방법
```
<!DOCTYPE html>
<html>
    <head>
        <title></title>
        <meta charset="utf-8">
        <!-- external방식 외부에서 css가져온것 -->
        <!-- 외부에서 가져온것은 크로스브라우징에 의하여 안될수도 있다.-->
        <!-- 아래는 로컬컴퓨터에 저장한 05css파일을 연결 -->
        <link rel="stylesheet" href="css폴더/05css.css">
        <!-- 아래는 크로스브라우징을 위한 normalize.min.css파일을 cnd방식으로 연결 -->
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css">  

        <!-- internal방식  -->
        <style>
            /* 선택자*은 모든 요소를 의미 */
            *{margin:5px;}
            dt{background-color: bisque;}
            dd{color: burlywood;}
        </style>
    </head>
    <body>
        <!-- inline방식 : 특성요소에 style속성을 이용 -->
        <dl style = "border-style:solid;border-width:3px;border-radius:5px;">
         <dt>CSS</dt>
         <dd>cascadting Style Sheet. 웹문서 서식</dd>
         <dt>Cascading</dt>
         <dd>선택자에 적용된 많은 스타일 중에 어떤 스타일을 나타낼지를 결정함.</dd>
        </dl>
        <hr/>
        <h4>스타일 우선순위 (p203)</h4>
            <div>1. 사용자스타일시트가 최우선</div>
            <div>2. !important가 붙은 스타일</div>
            <div>3. 사용자 정의 일반스타일(제일빈번)</div>
            <div>4. 기본적인 브라우저 스타일 시트
                 >브라우저마다 각기 다른 default스타일 (여백,글자크기등)은
                 normalize.css파일 or reset200802.css파일등을 이용하여 평준화 또는 초기화 할수있다.</div>
        <hr/>
                <H2>Css의 선언방식 3가지(p190)</H2>
        - internal방식 : html문서안의 head요소에 style선언
         -문법
         <head>
            <style>
                선택자 {css속성명:값; css속성명:값;}
            </style>
        </head>
        - external방식 : html문서 밖에서 별도의 css문서
          = 문법
          <head>
            <link rel="stylesheet" href="경로/파일명.css">
          </head>
        -inline방식 : 특정요소에 style속성을 이용
         = 문법
          <태그명 style="css속성명:값; css송성명:값;"></태그명>
    </body>
</html>
```

## 2. 글자 기본조정
```
<!DOCTYPE html>
<html>
    <head>
        <tilte></tilte>
        <meta charset="utf-8">
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css">  
        <style>
            *{margin:3px;} 
            /* 폰트:문자체 두께 크기/줄간격 문서체 */
            #i1 {font:italic 900 24px/48px 궁서체;}

            .c1{color: goldenrod;text-decoration:underline}
        </style>
    </head>
    <body>

        <h4>텍스트스타일(p228)</h4>
        <span class="c1">color:글자색</span>
        <!-- 자간사이 조절 -->
        <span style="letter-spacing: -3px;"> thisisacsd1</span>
        <!-- 단어사이 조절 -->
        <span style="word-spacing: -3px;"> thisisacsd2</span>
        <span class="c1">text-decoration:텍스트에 줄표현</span>
        <br/><br/>
        <spam style="text-decoration:underline;">★★text-decoration:underline</spam>
        <br/><br/>
        <spam style="text-decoration:line-through;">text-decoration:line-through</spam>
        <br/><br/>
        <spam style="text-decoration:overline;">text-decoration:overline</spam>
        <br/><br/>
        <spam style="text-decoration:none;">★★★text-decoration:none</spam>
        <hr/>

        <h4>글꼴관련스타일 (p215)</h4>
        <div id="i1"> font속성: 글꼴관련속성을 한꺼번에 묶어 표현</div>
        <div style="font-weight: 500;"> font-weight: 500  </div> <!--글자 굵기-->
        <div style="font-size: 30px;"> font-size: 30px </div> <!--글자 크기-->
        <div style="font-family: fantasy,sans-serif;"> font-family: fantasy,sans-serif </div><!--글꼴 -->
        <div style="font-style:italic;">font-style:italic;</div> <!--이탤릭체 normal-->


        <hr>
        <h2> 선택자(selector p194)</h2>
        <xmp>
        태그명 : html문서내의 지정된 모든 태그를 선택하여 style서식 적용
        #id명 : 지정한 id명을 가진 요소에 적용 id명은 unique.
        .class명 : 지정한 class명을 가진 요소에 적용. class명은 동일 → 공통적인 서식 사용
        * : 전체선택자. 모든요소에 적용 (모든 하위요소에 한꺼번에 스타일 적용)
        </xmp>
        <hr/>
    </body>
</html>
```
## 3. 문단 사이 조절
```
<!DOCTYPE html>
<html>
    <head>
        <tilte></tilte>
        <meta charset="utf-8">
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css">  
        <!-- html유효성 검사기 -->
        <link rel="stylesheet" href="https://jigsaw.w3.org/css-validator/validator">
        <style>
            #i1{text-align: justify;
                /* border 두께 선종류 색상 */
                border: 3px dotted red;
                border-radius: 20px;
                width: 200px;}  /*너비*/
        </style>
        <title> 문단스타일</title>
    </head>
    <body>
        <div style="text-align:left">text-align:left</div>
        <div style="text-align:center">text-align:center</div>
        <div style="text-align:right">text-align:right</div>
        <!-- 양쪽에 맞추어 문단을 정렬 -->
        <div style="text-align:justify">text-align:justify</div>
        <div id="i1">text-align:justify</div>
        <hr>
    </body>
</html>
```
- 이미지 넣기 
   style #i{list-style-position: inside;  list-style-image:url('images/다운로드.jpg');}
   body <img src="images/다운로드.jpg" width:="250" height="250" alt="빠른연산">
   
   
## 4. css박스모델
```
<!DOCTYPE html>
<html>
    <head>
        <title> </title>
        <style>
            div{border: 1px solid red;}
        </style>
    </head>
    <body>
        <h2>padding이란 content와 border사이 여백 (p320)</h2>
        <div style="padding-top:50px;">padding-top:50px</div>
        <div style="padding-left:200px;">padding-left:200px</div>
        <div style="text-align:right; padding-right:50px;">padding-right:50px</div>
        <div style="padding-bottom:50px;">padding-bottom:50px</div>

    </body>
</html>
<html>
    <head>
        <title> </title>
        <style>
            div{border: 1px solid red;}
        </style>
    </head>
    <body>
        <h2>margin 이란 칸(요소)에서의와 border사이 여백 (p320)</h2>
         <!-- margin과 margin은 서로의 영역에 침범할수있다. (위,아래) 
              좌우는 겹치지 않는다. -->
        <div style="margin-bottom:50px;">padding-bottom:200px</div>
        <div style="margin-left:200px;">padding-left:200px</div>
        <div style="text-align:right; margin-right:50px;">padding-right:50px</div>
        <div style="margin-top:50px;">padding-top:200px</div>

    </body>
</html>
```
        
## 5. backgroud color model
```
```
