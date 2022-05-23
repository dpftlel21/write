<H1>form과 유효성 검사</h1>

<h2>1. form 이란?</h2>
<hr>
폼, 입력 폼은 웹 프로그래밍의 기술의 하나이다. 클라이언트가 정보를 입력 · 선택하고, 웹 서버 등의 폼을 처리하는 에이전트로 제출하기 위한 기구이다. 즉, 사용자와 웹 사이트 또는 어플리케이션이 서로 상호 작용하기 위한 기술 중 하나이다.
폼은 사용자가 웹 사이트에 데이터를 전송할 수 있게 한다. 일반적으로 웹 서버로 데이터를 전송하지만, 웹 페이지 내 필요한 데이터를 위해 전송할 수도 있다.

```html
<body>
    <form action="", method="", enctype="">
        <input type="text" name="test">
        <input type="submit> 
    </form>
</body> 
```
- Html의 form 태그는 input 태그를 감싸는 형태로 이루어 져 있다.
- ```<form></form>``` 태그 사이에는 다른 form 태그가 삽입이 안된다.
- ```<form>``` 이름 속성은 한 페이지에서 중복하여 사용하면 안된다.
- css를 통해 폰트를 적용할 때 ```<form>``` 태그는 폰트가 적용되지 않으므로 따로 font를 적용해야 한다. 
<hr>

<h2>2. form 태그의 속성</h2>
<hr>
<b>㉠ method</b> : 양식을 제출할 때 사용할 HTTP 메서드<br>
    - post : post메서드, 양식 데이터를 요청 본문으로 전송<br>
    - get : get메서드, 양식 데이터를 action URL과 ? 구분자 뒤에 이어 붙여서 전송 <br>
<b>㉡ name</b> : form의 이름, 서버로 보내질 때 이름의 값으로 데이터 전송 Html4부터 중단, id 사용 <br>
<b>㉢ action</b> : form을 전송할 서버쪽의 script 파일을 지정하고, 전송되는 서버 url 또는 링크를 의미<br>
<b>㉣ target</b> : action에서 지정한 script 파일을 현재 창이 아닌 다른 위치에 열도록 지정<br>
<b>㉤ autocomplete</b> : 자동완성, on으로 설정하면 form 전체에 자동 완성 허용<br><hr>

<h2>3. form 내부의 태그와 속성</h2><hr>
<h2>ⓐ input이란?</h2>
웹 기반 양식에서 사용자의 데이터를 받을 수 있는 대화형 컨트롤을 생성한다. 사용자 에이전트에 따라서 다양한 종류의 입력 데이터 유형과 컨트롤 위젯이 존재한다. 입력 유형과 특성의 다양한 조합 가능성으로 인해, input 요소는 HTML에서 제일 강력하고 복잡한 요소 중 하나이다.<hr>
<h2>ⓑ input 속성(Html 유효성 검사 기능)</h2>
<b>㉠ readonly </b> : 읽기전용 필드로 만들기<br>
<b>㉡ placeholder </b> : 힌트표시(필드클릭시 내용 사라짐)<br>
<b>㉢ maxlength </b> : 텍스트 필드에 최대로 입력할 수 있는 문자의 개수 지정<br>
<b>㉣ required </b>: input 태그의 required 속성을 입력해 주면 submit 버튼을 누르기 전에 어떤 데이터가 입력되어 있어야 한다.<br>
<img src="https://postfiles.pstatic.net/MjAyMjA1MjNfMjE1/MDAxNjUzMzA5OTM5NDc4.HruaE4M9tCKfsezb1GTFpCdrdgy7G9mBT5ng_VaoYlkg.frC0UCRii58ye_WD5IMEPzaWZWD3frgmoOzI3LUfuocg.PNG.dkdnmju/4.png?type=w773">
- 데이터를 입력하지 않고 제출 버튼을 누르게 되면 이러한 결과가 도출된다.<br>
<b>㉤ pattern </b>: 입력받을 데이터가 준수해야 할 정규 표현식을 설정한다.<br>
- 이 외에  <b>autofocus, autocomplete, max/min, step 등</b>이 있다.
<hr>

<h2>ⓒ input의 type 속성</h2>
<b>㉠ button </b> : 한 줄로 된 input을 정의한다. <br>
<b>㉡ email </b> :<br> 
- <b>input 태그</b>의 type 속성값을 “email"로 설정하면, input 요소는 사용자가 email 주소를 입력할 수 있도록 해준다.<br>
- 브라우저 지원 여부에 따라 전송할 때 입력한 email 주소가 유효한 email 주소인지 자동으로 검사한다. <br>
<b>㉢ number </b> : <br>
- <b>input 태그</b>의 type 속성값을 “number"로 설정하면, input 요소는 사용자가 숫자를 입력할 수 있도록 해준다.<br>
- number 타입이 일반 text 타입과 다른 점은 입력 필드 우측에 숫자의 크기를 조절할 수 있는 상하 버튼이 생기는 점이다.<br>
- 브라우저의 지원 여부에 따라 min 속성과 max 속성을 이용하여 숫자 선택에 제한값을 설정할 수도 있다.
<br>
<b>㉣ password </b> : 패스워드를 입력받을 수 있도록, 입력값이 화면에 보여지지 않도록 한다.<br>
<b>㉦ radio </b> : 사용자가 선택지 중에서 한가지를 선택할 수 있도록 한다.<br>
<b>㉧ submit </b> : form데이터를 서버로 submit 해주는 역할을 한다.<br>
<b>㉨ text </b> : 한 줄로 된 input을 정의한다. <br>
<b>㉩ URL 주소 입력 </b> : <br>
- <B>input 태그</B>의 type 속성값을 "url"로 설정하면, input 요소는 사용자가 - URL 주소를 입력할 수 있도록 해준다.<br>
<img src="https://postfiles.pstatic.net/MjAyMjA1MjNfMjY5/MDAxNjUzMzA4ODc3MzUy.ede8-mmTmN5vnmyIzw8zqO6kdyVOhRIe9RZg_PmtOQEg.bykHx2f6wTnSSySx59JPWRTZkDSE0-WjH-fkp9l6_1Eg.PNG.dkdnmju/3.png?type=w773"> <hr>


