## 3. HTML에서 테이블만들기
```
<!DOCTYPE html>
<html>
    <head>
        <title> 표(table 77p) </title>
        <meta charset="utf-8">
        <!-- internal방식 : 문서안의 head태그내부에 style선언 -->
        <style>
            /* 선택자 {속성:값,속성:값;}
            selector {property:value;}
            bordar-style : 선모양
            border-color : 선색상*/
            table,th,td{border-width:1px;
                 border-style:solid;
                 border-color: chartreuse;
                 border-collapse: collapse;}
            h2 {border-bottom :5px dashed  rgb(71, 28, 224);}
        </style>
    </head>
    <body>
        <h2> 표(table 77p)</h2>
                <!-- Css박스모델(p294★★★★)
                padding : border와 컨텐트와의 여백 
                border : 테두리
                margin : 요소와 요소사이의 여백 
                cellpadding : cell의 넓이 두깨
                width : cell넓이
                height : cell두께
                cellspacing : cell과 cell사이의 여백
                collapse : 셀의 테두리 붕괴. -->

        <table bgcolor="purple" height="300" cellpadding="10" cellspacing="3" width="400" 
                border="1" align="center"> <!--border은 테이블과 셀의 테두리다. -->
            <caption> 표 제목 </caption>
            <thead>
                <tr>
                    <th></th>
                    <th>1-2</th>
                    <th>1-3</th>
                    <th>학생수</th>
                    <th>교원수</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <!-- rowspan : 셀 열 병합 
                        colspan : 셀 행 병합 -->
                    <td rowspan="2">2-1</td>
                    <td>2-2</td>
                    <td>2-3</td>
                    <td colspan="2">2-4</td>
                    
                </tr>
            <tr>
                <td bgcolor="red">3-2</td>
                <td>3-3</td>
                <td>3-4</td>
                <td>3-5</td>
            </tr>
            <tr>
                <td>4-1</td>
                <td>4-2</td>
                <td>4-3</td>
                <td colspan="2" rowspan="2">4-4
                    <table border="1" align="center">
                        <tr>
                            <td>1줄 1칸</td>
                        </tr>
                    </table>
                </td>
            </tr>
            </tbody>
            <tfoot>
                <tr>
                    <td>5-1</td>
                    <td>5-2</td>
                    <td>5-3</td>
                </tr>
            </tfoot>
        </table>
    </body>
</html>
```
