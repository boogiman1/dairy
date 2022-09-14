# 11일차 미디어쿼리(반응형) 적용 / mostly fluid(기본형) / column drop

꿀 팁 표시: ❤ 노랑 배경글
상태: CSS
작성일시: 2022년 7월 27일 오후 9:20

[반응형.pdf](%25EB%25B0%2598%25EC%259D%2591%25ED%2598%2595.pdf)

# 미디어쿼리 (반응형)

- ❤ 반응형 하려면 viewport 설정과 미디어쿼리가 적용 되어야 한다.
- ❤ 무조건 link 걸때 css 다음에 미디어쿼리가 와야한다. 안그러면 작동x

<aside>
💡 **미디어 쿼리는 화면 크기에 따른 각각의 속성 값을 지정하여, 여러가지 화면을 구성하는 기술을 말합니다.**

`@media only screen and (조건문) {실행문}`

- @media : 미디어 쿼리가 시작됨을 표시합니다
- only : 미디어 쿼리 구문을 해석하라는 명령어입니다.(생략가능)
- all : 미디어 쿼리를 해석해야 할 대상을 나타냅니다.(생략가능)
    - all : 모든 미디어 유형에서 사용할 css를 정의합니다.
    - print : 인쇄장치에서 사용할 css를 정의 합니다.
    - screen : 컴퓨터 스크린에서 사용할 css를 정의 합니다.
- (조건문) : 해당 크기을 설정할 수 있습니다.
- {실행문} : 조건에 따른 실행을 설정합니다.
</aside>

---

# mostly fluid (기본형)

![Untitled](Untitled%20161.png)

960px 이하의 디바이스에서는 aside와 article의 너비를 비율대로 줄어들도록 하고,
480px 이하의 디바이스에서는 aside와 article이 너비를 다 쓰도록 하시오.

**기본형**

- ❤ **가변 퍼센트 계산 : (자기 너비 / 부모 너비)*100**

![Untitled](Untitled%20162.png)

![Untitled](Untitled%20163.png)

![Untitled](Untitled%20164.png)

![Untitled](Untitled%20165.png)

![Untitled](Untitled%20166.png)

- ❤ float:none; 을 안해도 되지만 해야지 완벽하다.

---

# column drop

![Untitled](Untitled%20167.png)

- 비율대로 줄어들다 내려온다 이전과 비슷하나 특정 부분만 아래로 떨어뜨려 새로운 레이아웃을 만드는 방식 
우측의 퀵 네비가 태블릿부터 하단으로 떨어진다

- **481px 이상 960px 이하일때 맨 우측 레이아웃 드랍**

![Untitled](Untitled%20168.png)

![Untitled](Untitled%20169.png)

- **형제 요소에 clear:both; 주면 float 클리어 된다.**

![Untitled](Untitled%20170.png)

- **480px 이하일때 레이아웃 드랍**
    
    ![Untitled](Untitled%20171.png)
    

![Untitled](Untitled%20172.png)