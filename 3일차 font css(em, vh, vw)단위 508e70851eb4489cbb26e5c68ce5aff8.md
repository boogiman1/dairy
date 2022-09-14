# 3일차 font / css(em, vh, vw)단위

꿀 팁 표시: ❤ 노랑 배경글
상태: CSS
작성일시: 2022년 7월 6일 오후 9:29

# **font**

❤ font-family : 글꼴 지정 속성

❤ sans-serif : 앞에 선언된 글꼴이 없으면 시스템 기본 글꼴 중 고딕체 아무거나 들어간다.

❤ serif : 명조체 아무거나

font-size : 폰트 사이즈 설정

font-weight : 폰트 굵기 설정

font-style : 폰트 스타일 변경

font-style : italic; 기울여진 체

❤ font-variant : small-caps → 영문에만 적용 된다. 전부 대문자인데 소문자 크기로 보인다.

축약 속성 : font : [ font-weight, font-style, font-variant ] [ font-size/line-heignt ] [ font-family ]

**축약 속성 사용 시 순서가 중요하다**

---

# web font (웹 폰트) 불러오기

- ❤ **@import url 은 style 안에 작성 후 ctrl 클릭 후에 폰트 이름 알아낸 후 사용하기 싶은 태그 안에 적용 / @import 가 @font-face뒤에 있으면 충돌나서 안됨**
    
    ![Untitled](Untitled%20282.png)
    
- ❤ **@font-face로 있는건 style 에 작성 후 사용하고 싶은 태그 안에 font-family 복붙**

![Untitled](Untitled%20283.png)

- ❤ **웹 폰트 가져오기 : link를 head 사이에 넣고 css를 style에 넣는다 / 폰트 추가 시 link는 전부 다시 복붙 하고 기존꺼 지우고 css는 따로 추가**

![Untitled](Untitled%20284.png)

**폰트 추가시 마지막 링크만 바꾼다.**

---

# css 단위

**글자단위**

기본 웹 폰트 사이즈 : 16px

❤**em** : 상대 단위, 상위(**부모**) 요소의 폰트 **크기에 비교**된다.

ex. font-size : 1.5em → 부모 크기 * 1.5

❤rem : rootem이란 뜻 / 제일 높은 놈*rem / 제일 높은 놈은 html이라 **항상 기준은 html 이다**.

root(html) 기준 : root 는 최상위 란 뜻

ex. font-size : 1.5rem → html 크기 *1.5

❤

```
html {
  font-size: 62.5%;
}
를 쓰면 font-size가 10px 이기 때문에 rem을 쓰면 *10으로 계산하면 된다.
```

**vh, vw, % 비교**

❤ **vh** : viewportHeight **화면의 높이 기준**으로 크기가 달라진다, 너비에는 반응하지 않는다.

❤ **vw** : viesportWidht **화면의 너비 기준**으로 크기가 달라진다. 높이에는 반응하지 않는다.

❤ **%** : **부모 기준**으로 % 만큼 커진다.!!!💥💥

![Untitled](Untitled%20285.png)

![Untitled](Untitled%20286.png)

![Untitled](Untitled%20287.png)