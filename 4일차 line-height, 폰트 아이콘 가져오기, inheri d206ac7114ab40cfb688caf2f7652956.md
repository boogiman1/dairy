# 4일차 line-height, 폰트 아이콘 가져오기, inherit(상속 속성)

꿀 팁 표시: ❤ 노랑 배경글
상태: CSS
작성일시: 2022년 7월 10일 오후 3:41

# line-height

line-height : **행간**, **단위 사용 안하면 배수** / 포토샵 일러스트는 행간 시작을 글자 맨 아래부터 하지만 HTML은 글자 중간부터 한다.

❤ **line-height : 높이와 같은 px 하면 중앙 정렬 된다**

---

# 폰트, 아이콘 가져오기

한글	[https://noonnu.cc/](https://noonnu.cc/)
구글	[https://fonts.google.com/?subset=korean](https://fonts.google.com/?subset=korean)
영문	[https://www.lipsum.com/](https://www.lipsum.com/)

웹 폰트 가져오기
**link를 head 사이에 넣고 css를 style에 넣는다**

```
    폰트 추가 시 link는 전부 다시 복붙 하고 기존꺼 지우고
    css는 따로 추가

```

**@import url 로 된 경우 style에 작성하고 ctrl 클릭 후 폰트 이름 알아 낸 후사용하고 싶은 태그 안제 적용 / font-face뒤에 있으면 충돌 나서 사용 안된다**.

**font-face도 @impot url과 같다.**

아이콘도 방법은 같으나 text로 취급 되기 때문에 text 속성을 사용한다.

---

# inherit(상속 속성)

부모 요소에 css효과를 주면 자식, 자손에게 전부 효과가 적용된다. 이걸 상속이라 한다.

상속 속성

**initial; → 원래 있던 값으로 적용하며 상속 값 없앤다.**

**inherit → 상속값을 받게 한다.**