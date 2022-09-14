# 12일차 flex 사용법 / flex-direction(축 방향) / flex-wrap(줄바꿈) / flex-flow / justify-content(축 기준 정렬) / align-items(행간 세로 정렬) / align-self(자식 마다 선언) / align-content (세로 정렬) / flex 반응형 속성들

꿀 팁 표시: ❤ 노랑 배경글
상태: CSS
작성일시: 2022년 8월 7일 오후 2:42

# flex 사용법

- ❤사용법은 우선 **부모 요소에 flex를 사용한다고 지시**해야한다.
- 부모박스 → flex 컨테이너라고 부른다.
- 자식박스 → flex 아이템이라고 부른다.
- ❤display : flex; 만 사용해도 **가로 방향**으로 된다. **기본 값 : row**

---

# flex-direction(축 방향)

- ❤direction : **방향을 설정**한다. 그 방향대로 **주축이 된다**.
- ❤ **flex-direction: row;** → **기본 값 가로** / **주축 : 가로**
- ❤ **flex-direction: row-reverse; → 가로 반전, 역방향 / 주축 : 가로**
- ❤ **flex-direction: column; → 세로 방향 / 주축 : 세로**
- ❤ **flex-direction: column-reverse; → 세로 방향, 역방향 / 주축 : 세로**

---

# flex-wrap(줄바꿈) / flex-flow

- ❤ flex-wrap : 배치를 하면서 **줄바꿈** 해주는 값
- ❤ **flex-wrap: nowrap;** → **기본 값** 줄바꿈 없음 **한줄로 표시**
- ❤ **flex-wrap: wrap; → 줄바꿈 해준다. 부모 너비에 따라 달라짐**
- ❤ **flex-wrap: wrap-reverse; → 줄바꿈을 반대로 뒤집어서 해준다**
- ❤ **flex-flow: row wrap; → flow 는 direction 과 wrap을 동시에 사용한다.**

---

# justify-content(축 기준 정렬)

- ❤ **justify-content: flex-start; → 축 시작 점 정렬**
- ❤ **justify-content: flex-end; → 축 끝 점 정렬**
- ❤ **justify-content: center; → 중앙 정렬**
- ❤ **justify-content: space-between → 시작과 끝점에 배치된 후 나머지는 같은 간격**
- ❤ **justify-content: space-around → 간격 포함한 자기 영역까지 다 균등**
- ❤ **justify-content: space-evenly → 모든 간격이 균등하게 분배 / 얘는 익스에 적용 x**

![Untitled](Untitled%20173.png)

---

# align-items(행간 세로 정렬)

- ❤ **align-items: flex-start; → 기본 값**
- ❤ **align-items: flex-end; → 아래로 정렬**
- ❤ **align-items: center; → 중앙 정렬**
- ❤ **align-items: baseline; → 글자 선에 맞춰서 배치**
- ❤ **align-items: stretch; → 부모 높이에 맞게** 아이템들을 체운다.
    
    ![Untitled](Untitled%20174.png)
    

---

# align-self(자식 마다 선언)

- ❤ 자식 **개개인 따로 컨트롤 가능** / **자식마다 따로 선언**을 해줘서 가능하다
- ❤ 자식 태그에 선언 → align-self: flex-start;

![Untitled](Untitled%20175.png)

![Untitled](Untitled%20176.png)

---

# align-content (세로 정렬)

- ❤ justify-content가 가로 정렬이면 얜 세로 정렬 / **justify-content 세로 버전**

![Untitled](Untitled%20177.png)

![Untitled](Untitled%20178.png)

---

# flex 반응형 속성들

- ❤ flex-basis → 기본 너비를 지정하는 존재. 계산법이 특이하다. 부모요소에 비례해서 적용된다. 단위를 작성하지 않으면 %
- ❤ flex-grow → 아이템 박스들이 늘어날 때 얼마나 공간을 늘릴지 계산해준다. 소수점 가능, 0은 기본 값
- ❤ flex-shrink → 축소 값, 기본 값 1
- ❤ flex : grow shrink basis; 위에 3개 속성 한 줄로 사용