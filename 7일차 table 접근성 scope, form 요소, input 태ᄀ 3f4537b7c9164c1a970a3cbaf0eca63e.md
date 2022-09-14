# 7일차 table 접근성 scope, form 요소, input 태그의 type(text, password, search, email, tel, color, number, range, radio, checkbox), 속성(value, name, id까지)

꿀 팁 표시: ❤ 노랑 배경글
목차: table 접근성 scope, form 요소(action, method), input 태그의 type 속성
상태: HTML
작성일시: 2022년 6월 25일 오전 12:25

# Table 접근성 scope

**table 태그 안에 caption 은 표의 제목을 의미한다**. (자주 까먹으니 주의)💥

❤scope 속성은 스크린리더기에서 읽을 데이터의 방향을 정해준다. 접근성 기법

![Untitled](Untitled%2044.png)

![Untitled](Untitled%2045.png)

화면에 표시되진 않는다.

---

# form 요소 개념

 ex : **<form action="#" method="post"></form>**

**❤ input을 단독으로 사용하지 않고 form 태그안에 꼭 써야하는 이유 : form 태그 안에만 있는 action 속성으로 인해서 서버에 전송 해줘야 하기 때문에 꼭 input 등 요소는 form안에 작성해야한다.💥**

❤action : 데이터가 전송 될 서버의 주소

❤method : 데이터가 전송 되는 방법, 주로 get, post 만 사용한다.

❤post : ID 나 PW를 사용할 때 사용, 보안성 때문에 사용한다. 
이유는 get으로 사용 된 보통 form 들은 검색 하면 주소창에 검색 내용들이 보여지기 때문에 보안상 post를 사용한다.

❤get : 검색하면 주소창에 검색내용이 나온다. 보통 사용

❤fieldset : form 요소를 그룹핑 하는 태그

❤legend : fieldset으로 그룹핑 된 form 태그의 이름을 지어주는 태그

![Untitled](Untitled%2046.png)

![Untitled](Untitled%2047.png)

**input 태그는 inline-block 속성이다!**

---

# input 태그 type 속성

아이디 : <input type="**text**" name="" id="">

비밀번호 : <input type="**password**" name="" id=""> 비밀번호 입력 가능 암호문자로 나옴

❤**비밀번호에 꼭 autocomplete=”off” 속성 추가해준다. 자동완성 속성 / 사용 안하면 기본 속성이 autocomplete=”on”이기 때문에 자동완성이 되기 때문**

검색 : <input type="**search**" name="" id=""> 검색창에 입력하면 지우기 아이콘 생성됨

이메일 : <input type="**email**" name="" id=""> 제출 시 이메일 형식이 아니면 걸러준다

전화번호 : <input type="**tel**" name="" id="">

컬러 : <input type="**color**" name="" id="">

수량 : <input type="**number**" name="" id=""> value로 숫자를 작성하면 그 숫자가 시작 숫자가 된다

만족도 : <input type="**range**" name="" id=""> min, max로 만족도 최소 최대를 지정 가능

![Untitled](Untitled%2048.png)

![Untitled](Untitled%2049.png)

---

# radio 와 checkbox의 차이

❤radio는 중복 선택 X, checkbox는 중복 선택 가능

❤radio : 여러개 중 하나만 선택 가능. 예, 성별, 나이, 연도 등 / name을 같게 해야 적용된다.

❤checkbox : 여러개 중복 선택 가능. name 이름 달라야 한다. 카테고리가 다르기 때문

![Untitled](Untitled%2050.png)

![Untitled](Untitled%2051.png)

---

# value, name, id에 대한 개념

❤value : 데이터 값 (즉 개발자에게 전송 될 데이터 값, 실무에서 개발자의 요청으로 작성 후 전달)

❤name : 백단용 데이터 실벽자 / value 값이 들어갈 이름, 즉 메뉴의 카테고리 라고 생각하자

❤id : 디자인용 식별자 / id는 절대 중복이 되어선 안된다.

---

# label 태그, checked 속성

❤ radio나 checkbox 안에 checked 속성 기입 시 자동으로 선택 되는 기능

![Untitled](Untitled%2052.png)

![Untitled](Untitled%2053.png)

❤label 태그 안에 input 태그 작성 시 input 글씨만 클릭해도 체킹 된다.

![Untitled](Untitled%2054.png)

![Untitled](Untitled%2055.png)

❤떨어져 있는 input 체크를 할 경우 label 태그 안에 for 요소를 작성하고 input에 id와 같은 이름을 작성 

![Untitled](Untitled%2056.png)

![Untitled](Untitled%2057.png)