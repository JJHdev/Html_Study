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
