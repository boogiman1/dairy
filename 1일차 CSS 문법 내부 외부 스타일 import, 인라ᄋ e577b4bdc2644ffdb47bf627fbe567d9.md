# 1일차 CSS 문법 / 내부 외부 스타일 import, 인라인 스타일 / 선택자

꿀 팁 표시: ❤ 노랑 배경글
목차: CSS 문법 / 내부 외부 스타일 import, 인라인 스타일 / 선택자
상태: CSS
작성일시: 2022년 7월 5일 오후 9:28

# CSS 문법

- 선택자 {선언문} 구조
- 선택자(selector) {선언문(declaration)}
- 선언문 : {preperty(선언부분) : value;}

ex. h1 {color : red;}

---

# 내부 외부 스타일

- 내부스타일 : head 태그 사이에 있는 title 태그 아래에 style 태그를 넣어 그 안에 작성한다. 대부분 사용 x
- **외부스타일** : head 태그 사이에 있는 title 태그 아래에 link 태그를 이용한다. link 탭 하면 자동 생성 후 href 에 css 확장자를 가진 파일명을 작성하고 ctrl 클릭하면 생성 가능. / 원래는 css 확장자를 가진 파일을 먼저 생성 후 경로로 연결 해준다.
**이게 웹 표준**
- @import : CSS 안에 CSS / url을 통해 연결해준다.

![Untitled](Untitled%20113.png)

내부 스타일 import

![Untitled](Untitled%20114.png)

외부 스타일 import

- 인라인 스타일 : html 태그 안에 style : color=”red”; 와 같이 style 속성으로 추가한다.

---

# 선택자

- 태그 선택자 : 태그{ }

- ❤**아이디 선택자** : html : <div id=”mycssdiv”> → css : div#mycssdiv {  } / #아이디 이름 형태로 정의**반드시 영문으로 시작해야 하며 _ - 이외의 특수문자, 띄어쓰기 사용 X. 주민등록번호 처럼 중복 불가능**

![Untitled](Untitled%20115.png)

![Untitled](Untitled%20116.png)

- ❤**클래스 선택자** : html : <div class=”mycssdiv”> → css : div.mycssdiv {  } / 사용자 정의 선택자라고 하며 , **영어나 - _ 특수 문자만 이용해서 만든다. 아이디 처럼 무조건 영어로 시작 X  
ex. <p class=”happy t_center>와 같은 띄어쓰기로 여러개 사용 가능**

![Untitled](Untitled%20117.png)

![Untitled](Untitled%20118.png)

- 전체 선택자 : * {  } /  * : 전체란 의미를 가진다

- ❤**하위 선택자 : 부모태그  자식태그{  } : 부모 태그 아래 모든 자식, 자손 태그 다 포함한다. 모든 자식 자손이 중요!!! / ex. div p{   } div 안에 있는 모든 html 의 p 태그 전체를 뜻한다.**

![Untitled](Untitled%20119.png)

![Untitled](Untitled%20120.png)

- ❤**자식 선택자 : 부모태그 > 자식태그{  } : 부모태그 바로 아래에 있는 모든 자식 태그들만 선택 된다. 자손이 선택 안되는것 / ex. div > p : div 의 자식인 p 태그들만 선택된다.**

![Untitled](Untitled%20121.png)

![Untitled](Untitled%20122.png)

- ❤**인접 선택자** : 형제1 태그 + 형제2 태그 {   }   :   형제1 태그 옆에 있는 형제2 태그 **하나가 선택이 된다** / + : 옆 이라는 뜻

![Untitled](Untitled%20123.png)

![Untitled](Untitled%20124.png)

- ❤**형제 선택자** : 형제1 태그 ~ 형제2 태그 {    }   :   **형제 1 태그 옆 모든 형제 2 태그**들이 선택 된다.

![Untitled](Untitled%20125.png)

![Untitled](Untitled%20126.png)

- 그룹 선택자 : 태그, 태그 {   } : 여러 태그에 같은 css 적용