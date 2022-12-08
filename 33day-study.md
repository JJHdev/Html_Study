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
