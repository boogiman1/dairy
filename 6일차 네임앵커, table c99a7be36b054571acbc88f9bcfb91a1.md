# 6일차 네임앵커, table

꿀 팁 표시: ❤ 노랑 배경글
목차: 네임 앵커, table
상태: HTML
작성일시: 2022년 6월 24일 오후 11:40

# 네임 앵커

네임앵커란 페이지 안에 있는 페이지를 이동할 때 **href 에 #을 붙인다**.

그리고 usemap 처럼 **#임의로 지정한 이름을쓴다.**

❤ex) <a href=”#model1”></a>

그리고 이동하고 싶은 속성에 id를 부여하여 같이 작성하여 준다.

**id에는 # 제거한 이름 작성**

❤ex) <h2 id=”model1”>이동하고 싶은곳</h2>

![Untitled](Untitled%2038.png)

![Untitled](Untitled%2039.png)

---

# Table

- ❤**tr 안에는 td 요소가 들어간다**
- **tr** 은 가로 **행**, **td**는 **한 칸**을 의미한다.
- ❤**thead 안에**는 td 대신 **th가 온다**. th는 중앙 정렬, 굵은 글씨
- thead, tbody, tfoot으로 감싸면 table 태그 안에 위치가 바뀌어도 자기 자리로 간다.
- ❤css : border-collapse : collapse; → 테이블 테두리를 한줄로 병합
- col은 행, row는 열을 의미
- ❤css : border:dashed; 는 점선

---

# Table에 속한 태그

- ❤table 안에 caption 태그는 테이블의 제목을 의미한다 테이블 밖에 그냥 사용하면 문단으로 인식
- ❤colgroup 태그 안에 <col/> 단일 태그를 사용, 작성만 하면 col 방향으로 그룹핑이 된다. 열이 개면 col 3번 사용
- ❤col의 영역을 늘리려면 span 속성 사용

![Untitled](Untitled%2040.png)

![Untitled](Untitled%2041.png)

---

# 표 병합

- ❤colspan : 가로 행 병합
- ❤rowspan : 세로 열 병합

![Untitled](Untitled%2042.png)

![Untitled](Untitled%2043.png)