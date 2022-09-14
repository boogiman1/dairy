# 9일차 position

꿀 팁 표시: ❤ 노랑 배경글
상태: CSS
작성일시: 2022년 7월 19일 오후 9:26

# position

- ❤ position을 사용하면 top, left, bottom, right 값으로 속성을 추가하여 위치 조절을 좌표값으로 할 수 있다.
- ❤ 그리고 위치를 조절하면 다른 태그를 밀어내지 않고 겹쳐진다. **공중에 붕 뜬다고 생각** float과 다르다 float은 밀어낸다.
- 반응형 시 큰 애들은 float을 잡고 작은 애들을 position 잡는다.
- ❤ **static** : position의 **기본 값** → 아무 영향도 주지 않는다.
- ❤ **relative** : position의 상대 좌표, 상대 좌표 값이 내 위치에서 시작한다.

<aside>
💡 `❤ .red { background: crimson; position: relative; right: 50px;}`

내 위치에서 오른쪽 50px 만큼 이동

</aside>

![Untitled](Untitled%20148.png)

- ❤ **absolute** : position의 절대 좌표 / 부모를 벗어나 브라우저의 기준 값**(즉, 부모가 부라우저로 바뀐다고 생각)** absolute는 컨텐츠 끼리 겹치는게 가능하다. 애니메이션시 많이 사용,

<aside>
💡 .red { background: crimson; position: absolute; right: 50px;}

브라우저 기준 우측에서 50px 만큼 이동

</aside>

![Untitled](Untitled%20149.png)

- ❤ **z-index** : absolute는 컨텐츠 끼리 겹치는게 가능하다. 애니메이션시 많이 사용 / 그때 z-index로 앞으로 나오는 순위 가능. **position을 사용 할 때만 사용된다. -1 이하로는 떨어지지 않음**
- ❤ **자식에 전부 absolute를 주면 부모가 사라진다.** 그때 **부모에 너비와 높이를 주고 position : relative를 주면** **부모 기준으로 포지션 잡히면서 부모가 나온다**

![Untitled](Untitled%20150.png)

![Untitled](Untitled%20151.png)

![Untitled](Untitled%20152.png)

![Untitled](Untitled%20153.png)

- ❤ **fixed** : position을 고정 시키는 값
- ❤ **sticky** : position을 **스크롤로 고정**시키는 값 (새로 나와서 호환성이 낮다)

<aside>
💡 .box-2{background-color: cornflowerblue; position: sticky; top:30px;}

스크롤 내리면 top: 30px 만큼 내려와서 고정 된다.

</aside>

![Untitled](Untitled%20154.png)

<aside>
💡 수평 중앙 정렬

1. 요소의 너비를 준다.
2. position을 준다.
3. left:50% 이동시킨다.
4. 너비의 반 만큼 margin-left로 이동시킨다.

position : relative를 줬을 때 margin:auto; 로도 가능하나 position을 absolute를 줬을 때는 margin:auto;는 안된다. 웹 브라우저 기준으로 좌측 상단에 정렬 됐기 때문

</aside>