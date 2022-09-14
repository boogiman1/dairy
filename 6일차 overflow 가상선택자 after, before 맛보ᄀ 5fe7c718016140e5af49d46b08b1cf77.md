# 6일차 overflow / 가상선택자 after, before 맛보기 / opacity : 불투명도 / 배경 이미지 background-image / repeat / position / attachment / size / origin / clip

꿀 팁 표시: ❤ 노랑 배경글
상태: CSS
작성일시: 2022년 7월 12일 오후 8:20

# overflow

❤ 컨텐츠가 박스보다 넘칠 때 사용, block 요소만 사용 가능, inline 요소는 크기를 가질 수 없기 때문에 사용 불가능하다.

속성 값

- ❤ **overflow : visible;** → 기본값, 넘친 상태로 보여준다.
- ❤ **overflow : auto;** → 자동으로 스크롤 생김
- ❤ **overflow : hidden;** → 넘치면 넘친 부분이 안보이게 해준다.
- ❤ **overflow : scroll;** → x축, y축에 스크롤이 생기게 해준다.
- ❤🌹**초기화 코드로 사용 : overflow-y : scroll; → 미리 우측 스크롤 바 생성해준다.** 안하면 다른 메뉴 갈때마다. 생성되고 해서 시각적 불편함을 격는다🌹❤

---

# 가상선택자 after, before 맛보기

- ❤ **태그::after / 태그::before** → 실제로 html에 생기지 않는 **가상선택자**라고 한다. 선택된 태그 뒤, 앞에 문서를 만들어 주며 **inline 요소**이다. **content:’’; 안에 작성된 문서가 생기며 그 위 css 적용 가능하다.**
- 웹 아이콘 가상선택자로 사용 link head에 작성하고 혹은 @import은 style에 작성하고 content:’’;안에 이름 작성 후 font-family로 폰트명 작성해준다.

![Untitled](Untitled%20270.png)

![Untitled](Untitled%20271.png)

- 웹 이미지 등록 방법 / content:’’; 는 택스트로 들어가기 때문에 비워두고 background 사용

![Untitled](Untitled%20272.png)

![Untitled](Untitled%20273.png)

---

# opacity : 불투명도

- ❤ 불투명도를 조절하는 css
- ❤ 불투명도 조절을 rgba의 a(알파체널)을 통해서도 할 수 있다. opacity와의 차이는 **opacity는 상속**되고 **rgba는 상속되지 않는다.** 즉 배경만 불투명 하게 할 때는 알파체널을 사용한다

![Untitled](Untitled%20274.png)

![Untitled](Untitled%20275.png)

---

# 배경 이미지 background-image / background-repeat:no-repeat;

- background-image: url();
- ❤ 자동으로 모든 공간을 채우려고 반복된다. 반복하지 않으려면 background-repeat : no-repeat; 사용
- background-repeat : repeat → 기본 값, 반복한다
- background-repeat : repeat-y → y축 (세로) 만 반복한다.
- background-repeat : repeat-x → x축 (가로) 만 반복한다.
- ❤ **여러장 넣기 → background-image: url(../img/interior_con_img.jpg), url(../img/interior_con_img2.jpg), url(../img/interior_con_img3.jpg), url(../img/interior_con_img4.jpg);**

---

# 배경 이미지 위치 background-position

- ❤ background-position : x축 y축 으로 위치를 맞춘다.
- background-position: center left; 좌측 상단 정렬
- background-position: bottom; 태그 아래에 생기게함
- ❤ **여러장 위치 조절 → background-position: 10% 20%, 20% 50%, 40% 90%, 75% 30%;**
    
    ![Untitled](Untitled%20276.png)
    

![Untitled](Untitled%20277.png)

---

# 배경 이미지 고정 background-attachment : fixed;

- ❤**background-attachment: fixed;** 를 통하여 백 그라운드를 고정 시킬 수 있다.

---

# 배경 이미지 크기 background-size

- ❤ background-size : width height ; → 너비 높이
- ❤ background-size : 50px → 이렇게 하나만 써도 width만 적용되고 height는 자동 적용된다.
- ❤ background-size : auto; → 자동 기본값
- ❤ background-size : 80% → 상대값 가능
- ❤ background-size : cover; → 비율로 맞춰준다. 공간 없이 전체 꽉 차게(짤릴 수 있음)
- ❤ background-size : contain; → 이미지 비율 그대로

---

# 배경 이미지 원점 background-origin

- ❤ **이미지의 시작점을 정하는 속성**
- ❤ **background-origin : border-box;** → border 있는 곳 부터 시작한다.
- ❤ **background-origin : padding-box;** → padding 있는 곳 부터 시작한다.
- ❤ **background-origin : content-box;** → 글자가 있는 곳 부터 시작한다.

---

# 배경 이미지 영역 background-clip

- ❤ **background-clip : border-box;** → border 안에 영역
- ❤ **background-clip : padding-box;** → padding 안에 영역
- ❤ **background-clip : content-box;** → 컨텐츠 영역

---