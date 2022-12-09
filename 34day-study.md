## 1. html background
```
<!DOCTYPE html>
<html lang="ko">
    <head>
        <title></title>
        <meta charset="utf-8">
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css">  
        <style>
            /* body{background-color: blanchedalmond;} */
            *{margin:10px;}
            body{
                /* background-image: url("images/5.jpg"), url("images/2.jpg");
                background-repeat: no-repeat, repeat;
                background-position: right bottom, left top;
                background-position: 50%,50%; 
                background-attachment: fixed;
                background-attachment: fixed; 
                border: 10px dashed black; */
                
                background:url("images/5.jpg") right bottom no-repeat fixed,url("images/2.jpg") left top repeat;
            }
                </style>
       
    </head>
    <body>
        <h2>색상(p256)과 배경(p260)</h2>
        <ul>
            <li>background-color: 배경색</li>
            <li>background-image:url(경로및 파일명)</li>
            <li>background-repeat : 이미지반복</li>
            <li>background-attachment: 배경이미지고정여부</li>
            <li>background-position: 이미지위치</li>
            <li>background (shorthand property)</li>
            <li>1</li>
            <li>1</li>
            <li>1</li>

            
        </ul>
        
        <hr/>
      
    </body>
</html>
```

## 2. 선택자 (1,2,3)
```
<!DOCTYPE html>
<html lang="ko">
    <head>
        <title></title>
        <meta charset="utf-8">
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css">  
        <style>
            ul li{border:1px dotted blue}
        </style>
    
    
    
    </head>
    <body>
        <h2>연결선택자(p421)</h2>
        <hr/>   
        <p>*팬션예약정보</p>
            <ul>
                <li>예약방법</li>
                <li>1차 시작</li>
                <div>두두등장 </div>
                <ul>
                    <li>직접통화</li>
                    <li>웹사이트 예약</li>
                    <ul>
                        <li>예약방법</li>
                        <li>요금</li>   
                    </ul>
                </ul>
            </ul>
            <p>하위 선택자 => 상위요소 공백 하위요소<br/>
                지정한 모든 하위요소에 스타일 적용    
            </p>
            <p>
                하위선택자(p421) => 부모요소 > 자식요소<br/>
                지정한 자식 요소에 스타일 적용
            </p>
    </body>
</html>
```


```
<!DOCTYPE html>
<html lang="ko">
    <head>
        <title></title>
        <meta charset="utf-8">
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css">  
        <style>
            p + ul {margin: 5px; border:1px solid goldenrod}

            ul ul{border:4px dotted blue;}

            h2 ~ p {font-size: 12px;}
            /* h2(기준요소)에서 뒤에 모든 p(형제요소)에 접근하겠다. */
            h2 + p {color:blueviolet;} 
            /* h2의 형제요소 중에서 가까운 p에서 그 인접한 p들에게전체 적용 */

        </style>
    
    
    </head>
    <body>
        <h2>연결선택자(p421)</h2>
        <p>하위 선택자 > 상위요소 공백 하위요소<br/>
            지정한 모든 하위요소에 스타일 적용    
        </p>
        <p>
            하위선택자(p421) => 부모요소 > 자식요소<br/>
            지정한 자식 요소에 스타일 적용
        </p>
        <p>
            인접형제선택자(p421) => (같은레벨)요소 + 요소<br/>
            형제중에서 가장 가까운 형제요소에 스타일 적용
        </p>
        <p>
            형제선택자(p427) => 요소 ~ 요소<br/>
            기준요소뒤의 모든 형제요소에 스타일 적용
        </p>
        <hr/>   
        <p>*팬션예약정보</p>
            <ul>
                <li>예약방법</li>
                <div>두두등장 </div>
                <ul>
                    <li>직접통화</li>
                    <li>웹사이트 예약</li>
                </ul>
                <li>1차 시작</li>
                <ul>
                    <li>예약방법</li>
                    <li>요금</li>   
                </ul>
            </ul>
    </body>
</html>
```


```
<!DOCTYliE html>
<html lang="ko">
    <head>
        <title></title>
        <meta charset="utf-8">
        <link rel="stylesheet" href="httlis://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css">  
        <style>
            li + ul {margin: 5lix; border:1lix solid goldenrod}

            ul ul{border:4lix dotted blue;}

            h2 ~ li {font-size: 12lix;}
            /* h2(기준요소)에서 뒤에 모든 li(형제요소)에 접근하겠다. */
            h2 + li {color:blueviolet;} 
            /* h2의 형제요소 중에서 가까운 li에서 그 인접한 li들에게전체 적용 */

            body li:nth-child(2n) {color:blueviolet;} 
            
            /* li요소위에 마우스가 올라가면 브라운 색상을 반영해라 */
            ul li:hover{color:brown;}

        </style>
    
    
    </head>
    <body>
        <h2>연결선택자(li421)</h2>
        <ul>
            <li>
                구조가상 클래(li440)<br/>
                구조가상클래스란? 웹문서 구조를 기준으로<br/>
                특정위치에 있는 요소를 찾아 스타일을 지정할 떄 사용하는<br/>
                가상 클래스 선택자이다.<br/>
            </li>
            <li>nth-child(n) n번째 요소적용<br/>
                nth-child(3n+1) n은 0부터 시작하여 3의 배수에서 +1 요소 적용<br/>
                nth-child(n+2):nth-child(-n+5)  2~ 5번째 요소적용<br/>
                nth-child(odd) : 홀수
                nth-child(even) : 짝수
            </li>
            <li>의사클래스(가상클래스)<br/>
                의사클래스는 선택자에 추가되는 키워드<br/>
                선택한 요소가 특별한 상태여야 만족할 수 있다.
                예) :hover
            </li>
            <li>하위 선택자 > 상위요소 공백 하위요소<br/>
                지정한 모든 하위요소에 스타일 적용    
            </li>
            <li>
                하위선택자(li421) => 부모요소 > 자식요소<br/>
                지정한 자식 요소에 스타일 적용
            </li>
            <li>
                인접형제선택자(li421) => (같은레벨)요소 + 요소<br/>
                형제중에서 가장 가까운 형제요소에 스타일 적용
            </li>
            <li>
                형제선택자(li427) => 요소 ~ 요소<br/>
                기준요소뒤의 모든 형제요소에 스타일 적용
            </li>
        </ul>
        <hr/>   
        <li>*팬션예약정보</li>
            <ul>
                <li>예약방법</li>
                <div>두두등장 </div>
                <ul>
                    <li>직접통화</li>
                    <li>웹사이트 예약</li>
                </ul>
                <li>1차 시작</li>
                <ul>
                    <li>예약방법</li>
                    <li>요금</li>   
                </ul>
            </ul>
    </body>
</html>
```



## 3. 확장연결.
1. Prettier - Code formatter → 왼쪽아래 관리 → 설정 → 검색창에 default formatter →Prettier 설정하기.→ 검색 format on save 설정체
 1-1. 화면하단에 prettier 체크된 부분 모임.

2. d2coding파일(카카오톡 내꺼에) 다운받고 > 압축풀기 > all용 설치하기 >  왼쪽아래 관리 → 설정 >
 2-1. editor:Font Famliy 항목에서 D2Coding 입력
 2-2. editor:Tab Size 항목 2dlqfur

3. Community Material Theme 검색설치
4. auto reman tag 검색설치
5. bracket pair colorizer 검색설치 
6. linked editing 체크

## 4. 이미지 삽입과 방법
```
<!DOCTYPE html>
<html lang="ko">
  <head>
    <title></title>
    <meta charset="utf-8" />
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css"
    />
    <style>
      #pic1 {
        width: 250px;
        height: 250px;
        border: 5px dotted red;
        border-radius: 15px;
      }
    </style>
  </head>
  <body>
    <!-- img src ="필수속성 경로및파일명" -->
    <img src="./images/5.jpg" />
    <!-- 아래는 3칸위에있는c드라이버에있는이미지 파일 상대주소값 -->
    <img src="../../img_tree.png" />
    <figure>
      <img
        src="images/3.gif"
        alt="사진"
        title="사지인"
        width="100%"
        height="250px"
      />
      <figcaption>250 250 사진</figcaption>
      <img src="C:/vswk/images/5.jpg" id="pic1" />
      <figcaption>절대경로 사진</figcaption>
    </figure>
    <figure>
      <img src="C:\vswk\images\OIP.jpg" id="a1" />
      <figcaption>사진1</figcaption>
      <img src="C:\vswk\images\OIP.jpg" id="a2" />
      <figcaption>사진2</figcaption>
      <img src="../OIP.jpg" id="a3" />
      <figcaption>사진3</figcaption>
    </figure>
    <h2>이미지(p94)</h2>
    <pre>
            절대경로(absolute url): 전체경로
            상대경로(relative url): 부분경로 (기준파일&다른파일)
    </pre>
  </body>
</html>
```

## 5. 이미지 및 텍스트로 링크하기.
```
<!DOCTYPE html>
<html lang="ko">
  <head>
    <title></title>
    <meta charset="utf-8" />
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css"/>
    <style>
        #a1{text-decoration: none;
            color: #222;}
    </style>
  </head>
  <body id="aa">
    <a id="a1" href="https://www.youtube.com/watch?v=qe9tu4oFT_o&t=626s" target="_blank">누르시오</a>
    <a id="a1" href="https://www.youtube.com/watch?v=qe9tu4oFT_o&t=626s" target="_parent">누르시오</a>
    <a id="a1" href="https://www.youtube.com/watch?v=qe9tu4oFT_o&t=626s" target="_self">누르시오</a>
    <a id="a1" href="https://www.youtube.com/watch?v=qe9tu4oFT_o&t=626s" target="_top">누르시오</a>
    
    <hr />

    <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
    <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
    <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
    <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

    <!-- 위에올라가는 링크 -->
    <a href="#aa"><span>위에 올라가기</span></a>


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
