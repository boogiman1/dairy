# 5일차, color 종류/ lettet-spacing 자간 간격 / word-spacing 단어 간격/ text-decoration 밑줄속성 / text-transform 대소문자 속성 / text-shadow 그림자 속성 / text-align 문단 수평 정렬 속성 / vertical-align 문단 수직 정렬 / text-indent 들여쓰기 / 텍스트 줄바꿈 word-break / 텍스트 줄 바꿈 white-space / text-overflow / line-height / display : table-cell / display : none; / visibility : hidden;

꿀 팁 표시: ❤ 노랑 배경글
상태: CSS
작성일시: 2022년 7월 11일 오후 9:06

# **color**

- ❤ background-color: #9999ff; 와 같은 핵사코드를 많이 쓴다.
- ❤ background-color:#9999ffca;는 핵사코드에 a(알파체널)을 추가해서 불투명도를 조절해 준다.
- ❤ background-color: rgb(204, 105, 105); 와 같은 rgb 코드를 많이 쓴다.
- ❤ background-color: rgba(180, 255, 255, 0.5);는 rgb 코드에 a(알파체널)를 추가해서 불투명도를 조절해 준다.
- background-color: red; 와 같은 관용색 명은 잘 사용하지 않는다.
- background-color: hsl(180, 50%, 50%); 는 hsl(각도, 체도퍼센트, 명도 퍼센트)
- background-color: hsla(180, 50%, 50%, .8); 는 hsl코드에 a(알파체널)을 추가해서 불투명도를 조절해준다.
- ❤ a(알파체널)은 0.5 이렇게 하는데 앞에 0 생략 가능

---

# letter-spacing / word-spacing 자간, 단어 간격

- ❤ letter-spacing : 자간 간격 + - 양수 음수 사용 가능
- ❤ word-spacing : 단어 간격 + - 양수 음수 사용 가능

---

# text-decoration

- ❤ **밑줄 속성**
- ❤ **none** : 줄 없앰
- ❤ **underline** : 아래에 줄 생김
- ❤ **overline** : 위에 줄 생김
- ❤ **line-through** : 글자 중간에 선 생김

---

# text-transform

- ❤ **대소문자 속성**
- ❤ **lowercase** : 단어 모든걸 소문자로 바꿈
- ❤ **uppercase** : 단어 모든걸 대문자로 바꿈
- ❤ **capitalize** : 단어의 앞 부분만 대문자로 바꿔줌

---

# text-shadow 그림자 속성

❤ **text-shadow: -4px -4px 4px rgba(100, 100, 0, .6);**

❤ **text-shadow: X축, Y축, 번짐, 색상 으로 표기**한다.

**❤ shadow 속성은 연달아 사용 가능하다. 이걸로 3D처럼 구현 가능하다**

```html
text-shadow: 2px 2px #246, 3px 3px #357, 4px 4px #468, 5px 5px #579, 6px 6px #68a, 7px 7px #79b, 8px 8px #8ac;
            /* 속성값, 속성값, 하면 여러번 적용 시킬 수 있따. 
            익스 9 버전 이하에서는 적용 x*/
```

![Untitled](Untitled%20222.png)

---

# text-align 문단 수평 정렬 속성

- ❤ **text-align : block안에 inline 요소만 해당 된다.**
- ❤ text-align: left; 좌측정렬 기본값
- ❤ text-align: right 우측
- ❤ text-align : center 중앙정렬
- ❤ text-align : justify : 양쪽 정렬

---

# vertical-align 문단 수직 정렬

- ❤💥 **인라인 요소나 table-cell box에서만 사용 가능하다.**💥❤
- table-cell 은 태그를 td태그로 바꿔주는 속성이다.
- vertical-align : middle ; 중앙 정렬

---

# text-indent 들여쓰기

- 첫 문단이 들여쓰기가 된다.
- **❤ 부모 block요소에 사용하면 자식 inlne속성에 적용 된다.**
- **❤ 로고로 쓰는 창에 로고 옆에 inline 태그로 로고 이름을 작성하고 -9999999999px로 화면에서 없앤다**

---

# 텍스트 줄 바꿈 word-break / word-wrap

❤ **word-break 는 아시아, 비아시아 언어 다 줄바꿈이 되기 때문에 이것만 사용한다**. **문자 사이에 공백이 없을 때 사용**

❤ **word-break** : **break-all**; 는 **글자 기준**으로 줄 바꿈

❤ **word-break**: **keep-all**; 는 **단어 기준**으로 줄 바꿈

normal : CJK 문자는 글자 기준, 비 CJK 문자는 단어 기준으로 줄 바꿈

**word-wrap**: bread-word; 비아시아 언어만 줄바꿈이 된다. 영어는 띄어쓰기가 없으면 자동 줄바꿈이 안된다. 이건 **비아시아 언어만 되기 때문에 안쓴다. word-break를 사용한다**

---

# 텍스트 줄 바꿈 white-space

❤ white-space 는 띄어쓰기 공백이 있을 때 사용 가능

❤ **white-space: nowrap;** → 줄 바꿈 **안한다**

❤ **white-space: pre;** → 작성 한대로 그대로 표시된다.

❤ **white-space: pre-wrap;** → **공백 없는 묶음 자동 줄 바꿈**

❤ **white-space: pre-line;** → **스페이스바는 인식 못하고 엔터는 인식한다.**

---

# text-overflow

❤ **블럭에 적용 / 블럭 아래 인라인에 적용된다. 하위 속성 필요 / 인라인 일때 안되는 이유는 인라인은 알아서 영역 만큼만 생기고 크기 조절이 안되기 때문**

❤ 아래를 세트로 쓴다. 

width
overflow:hidden;
white-space:nowrap;
text-overflow:ellipsis;

❤ overflow:hidden; → **overflow가 컨텐츠가 너비보다 클때 어떻게 해라 라는 속성**

여기선 숨기라는 뜻

❤ white-space: nowrap; → 줄바꿈 하지 못하게 한다.

❤  **text-overflow : ellipsis; → 뒤에 짤리는 글자를 … 으로 만들어줌**

---

# line-height

❤ **높이 값과 같이 line-height 를 사용 하면 중앙 정렬 된다. / 자식한테 상속된다 / 2줄 이상이면 적용 되지 않는다.**

---

# display : table-cell

display : table-cell 하면 **td요소로** 바뀐다. td style도 적용된다.

display : table-cell;
vertical-align : middle; 하면 중앙 정렬 되나 td가 inline 요소라 옆으로 찬다.. 완벽하지 않음

---

# display : none; / visibility : hidden;

❤ **display:none; 는 완전 흔적도 없이 사라진다. 공간도 삭제**

❤ 

**strong.hdd2** {
color: red;
visibility: hidden;
/* visibility: hidden; 없애주지만 공간은 남는다. */
/* opacity:0; */
/* color: rgba(255, 0, 0, 0); */
}
**div.box:nth-child(3):hover .hdd2** {
visibility: visible;
/* visibility: visible; 다시 나온다. */
/* opacity:1; */
/* opacity:1; 는 opacity로 안보이게 한 것은 opacity로 해야 된다. */
/* color: rgba(255, 0, 0, 1); */
/* **rgba 처럼 핵사 코드로 들어가는 a를 활용하여도 할 수 있으나 이건 상속이 되기 때문에 opacity와 visibility는 상속이 안된다. 자식이 있을때는 opacity나 visibility 사용** */
}

❤ 삭제된 공간을 다시 보이게 하려면 삭제하게 한 태그로 보이는 값을 hover에 적어줘야 한다. 위에 보면 **visibility** 는 **visibility**로 **opacity**는 **opacity**로 **color**는 **color**로