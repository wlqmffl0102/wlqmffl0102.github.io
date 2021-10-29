---
title: HTML - 많이 사용되는 태그 28선
author: Dodev 하다
date: 2021-10-16 20:01:00 +0900
categories: [html]
tags: [html, study]
---

## 두서
---

## 많이 사용되는 태그 28선
---
사실 태그의 종류는 워낙 많기 때문에, 모든 태그를 다 외울 수는 없습니다. 그래서 적당히 필요한 태그를 다뤄보고자 하는데 어떤 것을 순차적으로 쓰면 좋을까 생각하다 사용빈도가 높은 태그들을 다루는것으로 결정했습니다. 
[Advanced Web Ranking](https://www.advancedwebranking.com/html/)페이지를 참조하여, 사용빈도가 높은 태그는 아래와 같습니다.

![Desktop View](/assets/img/2021-10-16/1.png){: width="70%" } 

홈페이지상으로는 32선으로 확인되나, 차트는 28개가 확인되어 28개로 진행하겠습니다!

---

### html 태그
역시 `<html>`태그가 1위 입니다. 모든 웹 페이지는 해당 태그가 무조건 들어가야 합니다. 
시작태그 `<html>`과 종료태그 `</html>`이 있습니다.
```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>THIS IS A TITLE</title>
    </head>
    <body>
        <p>This is a page<p>
    </body>
</html>
```

위와 같이 모든 태그들은 `<html>`태그 안에 존재해야합니다. 

---

### head 태그
대부분 웹 브라우저 화면상에는 나타나지 않지만, html에서 필요한 여러가지 정보들이 해당 태그 안에 들어갑니다. 
`<meta>`(인코딩 타입), `<title>`(페이지 제목), `<style>`(CSS) 등의 태그 등이 `<head>`태그 안에서 사용됩니다. 
대부분이 웹 브라우저에 나타나지 않지만 `<title>`태그는 브라우저 상단 페이지 제목으로 브라우저에서 표시됩니다. 
하나의 문서당 단 하나의 head태그가 존재합니다.
시작태그 `<head>`와 종료태그 `</head>`가 있습니다.
```html
    <head>
        <meta charset="utf-8">
        <title>THIS IS A TITLE</title>
    </head>
```

---

### body 태그
브라우저의 실질적인 표시 영역입니다. 여러가지 태그들이 사용되어 화면을 구성합니다.
시작태그 `<body>`와 종료태그 `</body>`가 있습니다.
```html
    <body>
        <p>안녕하세요. Dodev 하다 입니다.</p>
    </body>
```

---

### title 태그
웹 브라우저의 상단 제목 표시줄에 나타납니다. 
`<head>`태그 안에 속해있어야 합니다.
시작태그 `<title>`과 종료태그 `</title>`이 있습니다.
```html
    <head>
        <title>THIS IS A TITLE</title>
    </head>
```

---

### meta 태그
해당 웹 페이지의 인코딩 및 문서 키워드, 요약 정보를 가집니다.
`<head>`태그 안에 속해있어야 합니다.
시작태그 `<meta>`만 있습니다.
```html
    <head>
        <!--인코딩 설정-->
        <meta charset="utf-8"> 
    </head>
```

---

### div 태그
Division의 약자로, 아무런 의미를 뜻하지는 않지만 레이아웃을 나누는데에 사용됩니다. 여러가지 내용을 묶어서 표현해야 할 때 사용됩니다.
시작태그 `<div>`와 종료태그 `</div>`가 있습니다

---

### a 태그
Anchor의 약자로, 다른 웹 페이지로 연결해줍니다. 보통 "하이퍼링크"라고 생각하는 것이 이 `<a>`태그를 이용하여 만들어집니다.
시작태그 `<a>`와 종료태그 `</a>`가 있습니다
```html
<a href="https://wlqmffl0102.github.io/"> Dodev 하다의 블로그 </a>
```
a태그의 href(hypertext reference)속성을 이용하여 사용됩니다.

인터넷에서 a태그 관련 정보를 보시면 아래와 같이 href속성값이 "#"인 것을 많이 보실텐데요.

```html
<a href="#"> Dodev 하다의 블로그 </a>
```
이 링크는 어디로도 연결되지 않습니다. 그냥 모양만 있고 작동은 하지 않습니다. `null링크` 라고 합니다. 사용하지 않는것이 좋다고 생각합니다!

---

### script 태그
script코드를 사용하기 위해 반드시 필요한 태그 입니다. 
html은 기본적으로 정적인 페이지이지만 html과 script코드를 사용해서 동적인 페이지로 사용할 수 있습니다.
보통은 javascript를 사용하기 위해 해당 태그를 사용합니다.
시작태그 `<script>`와 종료태그 `</script>`가 있습니다.

---

### link 태그
외부의 리소스를 현재 작성중인 문서로 불러올때 사용합니다.
보통 CSS문서를 가져오는데에 많이 사용되지만 favicon(파비콘)연결 등 에서도 사용됩니다.
시작태그 `<link>`만 있습니다.

현재 작성중인 문서는 html만 작성하고, CSS는 완전히 별개로 작성한 뒤 .css파일로 저장해둡니다.
이후 저장된 .css파일을 작성중인 문서와 연결하여 사용할때 link태그를 사용해 연결합니다.
```html
<link href="https://cdnjs.cloudflare.com/ajax/libs/nvd3/1.8.2/nv.d3.css" rel="stylesheet" type="test/css">
```

위 예시는 현재 작성중인 문서에 외부 문서. 즉 nv.d3.css파일을 연결하겠다는 의미입니다.

a태그와 마찬가지로 href(hypertext reference)속성을 이용해 어떤 파일과 연결할지 명명합니다.
해당 파일은 CSS이므로 rel(relation)속성에 stylecheet라고 적어줍니다.
type 또한 text로 이루어진 css파일임을 명시합니다.

연결이 정상적으로 되었다면 현재 작성중인 html문서에 css를 하나도 작성하지 않았더라도 nv.d3.css와 연결되어 있어 nv.d3.css에 작성된 style을 바로 사용할 수 있습니다.

또한, favicon(파비콘)을 연결할때에는 아래와 같이 사용됩니다.
favicon이란 웹 사이트 가장 상단, 제목 바로 앞에 붙는 아이콘을 말합니다.
```html
<link rel="icon" href="favicon.ico" type="image/png">
```

href속성을 이용해 어떤 파일이 favicon으로 보여질지 작성합니다.
rel속성과 type속성도 맞추어 icon, imag/png로 작성합니다.

---

### img 태그
이미지를 넣을때에 사용되는 속성입니다. 한 태그당 하나의 이미지를 넣을 수 있습니다.
시작태그 `<img>`만 있습니다.

```html
<img src="https://img.insight.co.kr/static/2018/02/12/700/vrk5z3a409vt02d3jvb7.jpg" />
```

주로 사용되는 속성은
- src : 이미지 경로
- alt : 이미지를 표시할 수 없을 때 나오는 내용
- width : 이미지 가로 크기
- height : 이미지 세로 크기

등이 있습니다.

---

### span 태그
[div 태그](#div-태그)와 비슷한 태그입니다.
div태그와 동일하게 아무런 의미가 없는 태그 입니다. div와 차이점은 div태그는 자동으로 줄바꿈이 되지만, span태그는 자동으로 줄바꿈이 되지 않는다는 것 입니다.
시작태그 `<span>`과 종료태그 `</span>`이 있습니다.
```html
<!DOCTYPE html>
<html>
    <body>
        <div>안녕하세요.</div>
        <div>Dodev 하다입니다.</div>
        <br>
        <br>
        <span>안녕하세요.</span>
        <span>Dodev 하다입니다.</span>
    </body>
</html>
```

예시 코드를 돌려보면 아래와 같이 확인됩니다.

![Desktop View](/assets/img/2021-10-16/2.PNG){: width="50%" }

---

### p 태그
paragraph의 약자로, 하나의 문단(단락)을 만들때 사용되는 태그입니다. 
시작태그 `<p>`와 종료태그 `</p>`가 있습니다.
```html
<!DOCTYPE html>
<html>
    <body>
        <p> 안녕하세요 </p>
        <p> Dodev 하다 입니다. </p>
    </body>
</html>
```

---

### li 태그
아래에 나올 `ul태그` 또는 `ol태그`안에서 목록을 사용하는데에 사용되는 태그입니다. 항상 `ul(unordered list)` 또는 `ol(ordered list)`과 함께 쓰이며 단독으로 쓰이지 않습니다.
시작태그 `<li>`와 종료태그 `</li>`가 있습니다.
```html
<!DOCTYPE html>
<html>
    <body>
        <ul> <!--또는 <ol>-->
            <li> 목록내용 1 </li>
            <li> 목록내용 2 </li>
        </ul><!--또는 </ol>-->
    </body>
</html>

```

---

### ul 태그
unordered list의 약자로, 순서없는 목록을 만드는데에 사용됩니다.
`ol태그`는 ordered list의 약자로, 순서가 있는 목록을 만드는데에 사용됩니다.
시작태그 `<ul>`과 종료태그 `</ul>`이 있습니다.
그리고 시작태그 `<ol>`과 종료태그 `</ol>`이 있습니다.

ul태그는 순서가 없으므로 글 머리에 특수기호(●)가 붙습니다.

ol태그는 순서가 있으므로 글 머리에 default로 숫자가 붙습니다.
```html
<!DOCTYPE html>
<html>
    <body>
        <ul> 
            <li> ul 목록내용 1 </li>
            <li> ul 목록내용 2 </li>
        </ul>
        <ol> 
            <li> ol 목록내용 1 </li>
            <li> ol 목록내용 2 </li>
        </ol>
    </body>
</html>

```

![Desktop View](/assets/img/2021-10-16/3.PNG){: width="50%" }

---

### style 태그
스타일 정보 정의를 위해 사용합니다. 보통 CSS를 명시하며 `head`태그 안에 사용됩니다.
시작태그 `<style>`과 종료태그 `</style>`이 있습니다.

여기서 잠시. 

CSS 적용방법에관해서 3가지 방법이 존재합니다.
- 인라인(inline) 스타일
- 내부스타일시트 -> 이 방법이 style태그를 이용하는 방법입니다.
- 외부스타일시트 -> 가장 권장되는 사용법입니다. 


**인라인 스타일** : style적용을 하고 싶은 태그에 style 속성을 작성
```html
<!DOCTYPE html>
<html>
    <body>
        <p style="color:red; font-size:20px;"> Dodev 하다</p>
    </body>
</html>

```

**내부스타일시트** : `head`태그 안에 style태그를 이용해 작성
```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            body { background-color:black; }
            p { color:white; font-size:20px; }
        </style>
    </head>
    <body>
        <p> Dodev 하다 </p>
    </body>
</html>
```

**외부스타일시트** : 별도의 css파일을 작성한 뒤, `heaed`태그 안에 `link`태그를 사용해 현재 작성중인 html파일에 연결하여 사용. 가장 권장되는 사용법.

아래와 같이 별도의 style을 정의한 .css파일을 생성한다.
```css
body { background-color:skyblue; }
p { color:purple; text-decoration:underline; font-size: 20px; }
```

생성된 .css파일을 .html파일과 연결한다.
```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" href="./test.css">
    </head>
    <body>
        <p> Dodev 하다</p>
    </body>
</html>
```

순서대로 인라인스타일, 내부스타일시트, 외부스타일시트 사용 결과입니다!

![Desktop View](/assets/img/2021-10-16/4.PNG){: width="30%" }

![Desktop View](/assets/img/2021-10-16/5.PNG){: width="30%" }

![Desktop View](/assets/img/2021-10-16/6.PNG){: width="30%" }

---

### br 태그
줄바꿈 태그입니다. 시작태그 `<br>`만 있습니다.

---

### h2 태그
heading태그 중 하나 입니다. 
시작태그 `<h2>`와 종료태그 `</h2>`가 있습니다.
`head`태그와 `heading`태그는 전혀 다릅니다.

heading태그는 총 6개로, 주로 머리말이나 제목을 표현하기위해 사용됩니다.
- h1 : heading태그 중 글자 크기가 가장 큽니다.
- h2
- h3
- h4
- h5
- h6 : heading태그 중 글자 크기가 가장 작습니다.

h1~6까지만 heading태그로 지원되며, h7~는 heading태그로 지원되지 않고 일반 텍스트로 표현됩니다.

---

### input 태그
form태그 내부의 태그 입니다. form은 웹 페이지의 입력 양식을 나타내는 태그입니다. 그냥 양식을 만드는 태그이기 때문에, 그안에서 사용자로부터 입력을 받기 위한 태그 input이 존재합니다.
시작태그 `<input>`만 있습니다.

말 그대로 사용자로부터 어떠한 입력을 받기 위해 사용되는 태그이기 때문에 어떤 유형의 입력을 받을 것 인지, 입력받은 값은 무엇인지 등 여러가지 속성이 있습니다
```html
<form>
    <p>아이디</p>
	<input type="text" name="name" value="아이디">
</form>
```
input태그에는 여러가지 속성이 존재합니다.
  1. type 속성 : 입력 태그의 유형
     - text : 일반 텍스트
     - hidden : 화면에는 표시되지 않지만 서버로 데이터를 전송시 함께 전송됨
     - password : 비밀번호 입력
     - tel : 전화번호 입력
     - email : 이메일 입력
     - number : 숫자 입력(화살표로 조절)
     - range : 숫자 입력(슬라이드바로 조절)
     - radio : 라디오 버튼 -> 여러가지 옵션 중 하나만 선택 가능
     - checkbox : 체크박스 -> 여러가지 옵션 중 다중 선택 가능
     - submit : 서버 전송 버튼
     - button : 버튼
     - reset : 리셋 버튼
     - ... 등

  2. name 속성 : 사용자로부터 입력받은 데이터의 이름(임의지정가능). 서버로 보내지는 데이터명
  3. value 속성 : defualt(기본값)로 보여지는 내용.
  4. id 속성 : id값을 통해 여러가지 input태그를 구별
  5. 그 외 속성(readonly, placeholder, autofocus, max/min, required 등)
     - readonly : 읽기 전용 필드. 입력 불가.
     - placeholder : 어떤 값을 입력해야 하는지 알려주는 힌트 내용
     - autofocus : 페이지가 열리자 마자 마우스 커서가 표시되도록 설정
     - max/min : 필드의 최대/최소값 설정
     - required : 필수 입력 필드.

여러 속성들이 존재하지만 그중 `type 속성`이 가장 중요합니다. type속성에 따라 보여지는 input태그의 모습이 바뀌어 사용자로부터 받는 값이 변하기 때문입니다.

```html
<!DOCTYPE html>
<html>
    <body>
        <!-- form을 하나 만듭니다. 해당 form을 모두 작성한 뒤 submit버튼을 누르면 get방식으로 전송되어 main.html 페이지로 넘어갑니다. -->
        <form method="get" action="/main.html">
            <p>
                <!-- 브라우저에서 보이지 않으나 submit버튼을 누르면 해당 값이 함께 서버로 전송됨 -->
                <input type="hidden" name="country" value="korea">
            </p>
                <!-- onclick 이벤트를 걸어 버튼을 누르면 alert의 내용이 메시지 창으로 뜨게 됨 -->
                <button type="button" onclick="alert('아래 양식을 입력해주세요!')">버튼 클릭(메시지 표시)</button>
            <p>
                아이디
                <!-- placeholder는 '힌트' 그렇기 때문에 입력창의 value값이 아님. 마우스 커서를 올려보면 커서가 가장 앞에 위치 -->
                <input type="text" name="name" placeholder="아이디">
            </p>
            <p>
                비밀번호
                <input type="password" name="password" value="비밀번호">
            </p>
            <p>
                이름
                <!-- value는 '값' 마우스 커서를 올려보면 value의 내용(디폴트값)이 선택됨. 해당 기본값을 지우고 값을 작성해야함 -->
                <input type="text" name="name" value="이름">
            </p>
            <p>
                성별
                <!-- 둘 중 하나만 선택 가능함 -->
                <input type="radio" name="gender" value="M">남자
                <input type="radio" name="gender" value="F">여자
            </p>
            <p>
                나이
                <!-- number는 입력창 옆에 화살표 버튼이 있으며, text 타입처럼 키보드로 숫자를 적어넣을 수도 있음 -->
                <input type="number" name="age" value="0">
            </p>
            <p>
                전화번호
                <input type="tel">
            </p>
            <p>
                이메일 주소
                <input type="email">
            </p>
            <p>
                
            </p>
            <p>
                좋아하는 숫자
                <!-- range는 막대 바 형식의 숫자입력창. max(최대값), min(최소값), step(숫자의 간격) 등의 속성이 사용됨 -->
                <!-- step속성의 값이 10으로 설정되어 있기 때문에, 0, 10, 20, 30, 40... 과 같이 선택가능함 -->
                <!-- 사용자의 브라우저가 range타입을 지원하지 않으면 text타입으로 보여짐 -->
                <input type="range" name="favorite_num" min="0" max="100" value="10" step="10">
            </p>
            <p>
                좋아하는 꽃
                <!-- 다중선택가능 -->
                <input type="checkbox" name="flower" value="rose">장미
                <input type="checkbox" name="flower" value="hyacinth">히야신스
            </p>
            <p>
                <!-- 입력한 내용들을 서버로 제출함. form에서는 필수 요소 -->
                <input type="submit" value="제출">
        
                <input type="reset" value="리셋">
            </p>
        </form>
    </body>
</html>
```
![Desktop View](/assets/img/2021-10-16/7.PNG){: width="60%" }

---

### h1 태그
heading태그 중 하나 입니다. 
시작태그 `<h1>`과 종료태그 `</h1>`이 있습니다.
`head`태그와 `heading`태그는 전혀 다릅니다.

heading태그는 총 6개로, 주로 머리말이나 제목을 표현하기위해 사용됩니다.
- h1 : heading태그 중 글자 크기가 가장 큽니다.
- h2
- h3
- h4
- h5
- h6 : heading태그 중 글자 크기가 가장 작습니다.

h1~6까지만 heading태그로 지원되며, h7~는 heading태그로 지원되지 않고 일반 텍스트로 표현됩니다.

---

### form 태그
웹 페이지에서 하나의 입력 양식을 만드는 태그입니다. 이 form태그 안에 다양한 input태그가 존재하며, form태그 안에는 submit타입 버튼을 꼭 포함하고 있습니다.
작성 후 submit버튼을 클릭하면, 해당 submit버튼을 포함하는 form태그의 작성 내용들이 한꺼번에 서버로 전송됩니다.
시작태그 `<form>`과 종료태그 `</form>`이 있습니다.

form태그 속성으로는 5개가 있습니다.
 - action : form양식을 submit버튼으로 제출하게되면 form을 서버 측으로 전송하게 되며 action속성을 이용해 서버 측 어떤 파일로 전송될지 지정합니다.
 - name : form을 식별하기 위한 이름
 - accept-charset : form을 전송할 때 사용할 문자 인코딩
 - target : action으로 지정한 파일이 현재 창이 아닌 다른 위치에 열도록 지정합니다.
 - method : form을 서버 측으로 전송할때 사용하는 http메소드를 지정(get 또는 post)

 ```html
 <!DOCTYPE html>
<html>
    <body>
        <form  action="/main.html" method="get" accept-charset="utf-8" name="loginform">
            <p>
                아이디
                <input type="text" name="name">
            </p>
            <p>
                비밀번호
                <input type="password" name="password">
            </p>
            <p>
                <input type="submit" value="로그인">
            </p>
        </form>
    </body>
</html>
 ```

---

### h3 태그
heading태그 중 하나 입니다. 
시작태그 `<h3>`과 종료태그 `</h3>`이 있습니다.
`head`태그와 `heading`태그는 전혀 다릅니다.

heading태그는 총 6개로, 주로 머리말이나 제목을 표현하기위해 사용됩니다.
- h1 : heading태그 중 글자 크기가 가장 큽니다.
- h2
- h3
- h4
- h5
- h6 : heading태그 중 글자 크기가 가장 작습니다.

h1~6까지만 heading태그로 지원되며, h7~는 heading태그로 지원되지 않고 일반 텍스트로 표현됩니다.

---

### nav 태그
navigation links의 약자로, 현재 페이지 또는 다른 페이지와 연결하는 링크를 뜻합니다.
보통 메뉴, 목차, 인덱스 등이 있습니다. 그래서 보통 nav태그 안에 목록 태그인 ul 또는 ol태그와 li태그를 사용합니다.
시작태그 `<nav>`와 종료태그 `</nav>`가 있습니다.

```html
 <!DOCTYPE html>
<html>
    <body>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Categories</a></li>
                <li><a href="#">Tags</a></li>
                <li><a href="#">Archives</a></li>
                <li><a href="#">About</a></li>
            </ul>
        </nav>
    </body>
</html>
```

---

### footer 태그
말 그대로, 문서의 가장 하단부 요소를 뜻합니다. 해당 문서에 관한 정보(글쓴이, 저작권, 연락처 정보 등)들을 담고 있어야 합니다.
시작태그 `<footer>`와 종료태그 `</footer>`가 있습니다.

단어 느낌 적으로 한 문서당 하나만 있어야 할 것 같지만, 사실 한 문서에 여러개의 footer 태그를 사용할 수 있습니다.

---

### header 태그
head태그와 heading태그와는 또 다른 태그입니다. 
header태그는 해당 문서나 특정 섹션의 도입부에 해당되는 요소입니다. 하나의 문서에서 여러번 사용할 수 있습니다.
시작태그 `<header>`와 종료태그 `</header>`가 있습니다.

Naver의 header부분은 다음과 같습니다.

![Desktop View](/assets/img/2021-10-16/8.PNG){: width="100%" }

---

### iframe 태그
Inline Frame의 약자로, 웹 페이지 안에 또 다른 웹 페이지를 삽입할 때 사용됩니다.
시작태그 `<iframe>`과 종료태그 `</iframe>`이 있습니다.

지도, 영상 등 여러 페이지를 삽입 할 수 있으며, 아래는 iframe태그를 이용해  구글지도를 삽입한 모습입니다.

구글 지도 > 주소 검색 > 공유 > 지도퍼가기 > HTML복사

![Desktop View](/assets/img/2021-10-16/9.PNG){: width="100%" }

```html
 <!DOCTYPE html>
<html>
    <body>
        <p>구글 지도 - N서울타워</p>
       <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d12652.661205783037!2d126.97949329075564!3d37.551169078392675!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x357ca257a88e6aa9%3A0x5cf8577c2e7982a5!2zTuyEnOyauO2DgOybjA!5e0!3m2!1sko!2skr!4v1635071066687!5m2!1sko!2skr" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
    </body>
</html>
```
![Desktop View](/assets/img/2021-10-16/11.PNG){: width="100%" }



---

### button 태그
form 요소 중 하나로, input태그의 type속성을 이용해서 사용 할 수도 있습니다.`<input type="button">`과 같이 사용됩니다.
시작태그 `<button>`과 종료태그 `</button>`이 있습니다.

button태그의 속성은
- submit : form 제출
- reset : form 리셋
- (none) : type을 설정하지 않는 경우 버튼의 모양만 만들어지며, 동작 수행을 위해서는 따로 이벤트처리를 해줘야 합니다.

---

### strong 태그
중요내용 강조 태그 입니다. 해당 태그 안의 글자가 진하게 보여집니다.
쉽게 말하면 "굵게"표시 입니다. 동일하게 "굵음"표시를 하는 b태그가 있습니다만 조금 사용방법이 다릅니다.
시작태그 `<strong>`과 종료태그 `</strong>`이 있습니다.

- b 태그 : 단순히 텍스트를 진하게 표시
- strong 태그 : 페이지 내의 중요한 부분을 진하게 표시 -> 브라우저에 지원되는 웹 접근성에 기여

```html
<!DOCTYPE html>
<html>
    <body>
       <p>이것은 그저 <b>텍스트를 굵게</b> 만듭니다.</p>
       <p>이것은 현재 문서 안에서 <strong>중요도가 높은 텍스트를 굵게</strong> 만듭니다 </p>
    </body>
</html>
```

---

### i 태그
italic의 약자로, 해당 태그 안의 글자가 기울어져 보입니다.
동일하게 "기울임"표시를 하는 em태그가 있지만, 이 또한 사용처가 다릅니다.
시작태그 `<i>`와 종료태그 `</i>`가 있습니다.

- i 태그 : 단순히 텍스트를 기울임
- em 태그 : 페이지 내의 중요한 부분을 기울여 표시 -> 브라우저에 지원되는 웹 접근성에 기여

```html
<!DOCTYPE html>
<html>
    <body>
       <p>이것은 그저 <i>텍스트를 기울입니다</i> </p>
       <p>이것은 현재 문서 안에서 <em>중요도가 높은 텍스트를 기울입니다</em></p>
    </body>
</html>
```

---

## 시맨틱 태그
시맨틱(Semantic) 이란 "의미의, 의미론적인"이라는 뜻을 가진 영단어 인데요.

HTML5에 도입된 시맨틱 태그는, 태그의 이름만 보고도 해당 태그가 어떤 역할인지 바로 알 수 있는 태그를 말합니다.

`div태그`는 이름만 보고 어떤 내용이 들어있는지 알 수 없습니다.
하지만 `header태그`, `footer태그`, `nav태그`, `aside태그`의 경우 태그 이름만 보고도 어떤 내용이 들어가는지 대략적으로 가늠할 수 있습니다.

header, footer, article, aside, section, time태그 등이 시맨틱 태그에 속합니다.

![Desktop View](/assets/img/2021-10-16/10.PNG){: width="100%" }

위 그림처럼 시맨틱 태그를 사용하여 레이아웃을 이해 및 구성할 수 있습니다. 구조는 설계자에 따라 달라지나 대부분 위와 같은 구조를 기본으로 합니다.

---

## 마무리
---
세상에! 포스팅이 또 너무 길어졌습니다..ㅠ 호흡 조절이 필요한 부분에서 잘 조절하지 못한것같습니다.

html은 우선은 이정도만 작성하도록 하고, CSS로 넘어가보자 합니다!

읽어주신 분들 모두에게 감사드립니다!
