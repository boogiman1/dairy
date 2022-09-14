# 5일차 list, figure, 이미지맵, usemap, map, area, header, section

꿀 팁 표시: ❤ 노랑 배경글
목차: list, dl, figure, header, section, 이미지 맵, usemap, map, area
상태: HTML
작성일시: 2022년 6월 24일 오후 11:40

# list, ol, ul, li, dl

ol : orderlist란 뜻으로 숫자를 세김

ul : unorderlist란 뜻으로 숫자를 세지 않음

둘의 자식 요소로는 li 밖에 오지 못한다.

❤그러나 li 안에는 ol, ul, div, p 등 올 수 있다. ol, ul 자식으로만 li만 가능

ol의 속성은

❤ reversed : 숫자 뒤 바꿔 세기기

❤ start=”숫자” : 숫자부터 시작숫자 세기

❤ type : 표시 타입 / 'a'는 소문자 알파벳, 'A'는 대문자 알파벳, 'i'는 소문자 로마 숫자, 'I'는 대문자 로마 숫자, '1' 는 숫자(기본값)을 나타냅니다.

❤ 한번에 만들기 : ul>li*5, ol>li*5

![Untitled](Untitled%2058.png)

![Untitled](Untitled%2059.png)

❤ ul>li>a+(ul>li>a) / > : 오른쪽 요소에 왼쪽 요소를 포함한다. / + : 옆에 둔다.

![Untitled](Untitled%2060.png)

![Untitled](Untitled%2061.png)

---

# dl, dt, dd

dl은 반드시 **하나 이상의 <dt>-<dd>** **짝을 담고 있어야 한다.**

dt와 dd는 **dl 밖에서 사용하지 못한다**

단, **dt-dd가** 반드시 **하나의 짝**으로 지어져야 하는건 **아니다.**

dt는 하나 이상의 dd를 형제 요소로 가질 수 있기 때문이다. (예: `dt-dd-dd`)

그래서 하나 이상의 dt가 연속으로 나올 수 있다.(예: `dt-dt-dd`)

![Untitled](Untitled%2062.png)

![Untitled](Untitled%2063.png)

---

# figure + header, section

그림과 설명글이 한 세트로 묶을 때 사용
그림과 글이 하나의 삽화로 있을 때 사용

**❤figure 태그 안에 img 태그 와 그를 설명하는 figcaption 태그를 같이 사용한다.**

![Untitled](Untitled%2064.png)

alt는 사진 설명을 읽어주지만 figure를 사용해서 사진을 설명 해주면 굳이 적지 않는다.

시작 장애인들에게 오해를 주기 때문

❤ header는 h1과 다르다 컨텐츠는 section안에 적는다.

❤ 이미지의 크기를 바꿀때는 width나 height중 하나만 변경 한다. 화질이 깨지기 때문 그리고 px 고정 단위라 단위를 적지 않는다.

❤ img는 몇 없는 inline-block요소이다.

inline 요소는 너비 높이를 같이 못한다.
block 요소는 가질 수 있다.
inline-block은 인라인 속성을 가지면서 너비 높이를 가질 수 있다.

![Untitled](Untitled%2065.png)

---

# 이미지 맵, usemap, map, area

img 태그 안에 usemap 속성 기입

ex) usemap=”#임의로 지정한 이름” #은 링크를 의미

map 태그 작성 **name은 usemap과 동일하게 작성**하여 링크를 연결 시켜 준다.

ex) <map name=”임의로 지정한 이름”>

map 태그 **하위로 area 태그 작성**

ex) <area shape="rect" coords="0,0 100,100" href="[http://boowon1.dothome.co.kr/](http://boowon1.dothome.co.kr/)" alt="" target="_blank">

속성 설명

shape : 모양

coords : 좌표값 x,y x,y ex : coords="0,0 100,100" coords="x축,y축 x축,y축”

![Untitled](Untitled%2066.png)

![Untitled](Untitled%2067.png)