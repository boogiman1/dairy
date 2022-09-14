# 8일차 animation / position / column / float / clear

꿀 팁 표시: ❤ 노랑 배경글
목차: animation, position
상태: CSS
작성일시: 2022년 7월 14일 오후 5:46

# animation

- 사용하고자 하는 태그에 animation 을 넣고 name을 정해 준 다음 @keyframes name{} 안에 원하는 애니매이션 작동 효과들을 담는다.
    - ex. p{animation-name : me;
            animation-duration : 4s;
            animation-play-state : running;  /  p:hover{에 paused; 값 주면 마우스 올리면 멈춘다.
            animation-delay : 1s;}
    - @keyframes me{
                                0% {background-color: violet;
                                       width: 150px;
                                       transform: translate(0, 0)}
                                10% {background-color: bisque;
                                         width: 50px;
                                         transform: translate(200px, 100px)}
                                40% {}
                                50% {}
                                100% {} 이런 식으로 작동 효과 넣음
- ❤ animation-**name**: ; 이름이 꼭 있어야 한다 필수 속성
- ❤ animation-**duration**: ; 애니메이션 지속 속성 / 초 단위(s) 또는 밀리 초 단위(ms)로 지정한다
- ❤ animation-fill-mode: ; 애니메이션이 어디서 끝날 지 설정         forwards -> 시작점에서 끝남
- ❤ animation-iteration-count: ; 재생 횟수 지정 */
     animation-iteration-count: infinite; 무한 재생
- ❤  animation-direction:  ; 애니메이션이 끝난 후 반복될 때 진행 할 방향 선택
animation-direction: alternate; 애니메이션 종료 후 역방향
- ❤ animation-play-state: ; 애니메이션 진행 상황
animation-play-state: paused; 일시 정지
animation-play-state: running; 움직임
hover랑 같이 사용 가능

![Untitled](Untitled%20144.png)

- ❤ animation-delay: 1s; 몇 초 뒤에 시작한다
- ❤ animation-timing-function: cubic-bezier(); 속도 조절
- ❤ animation: name duration timing-function delay iteration-count direction fill-mode; -> **축약 속성**
- ❤ keyframes name{ } 안에 들어가는 값은 숫자만 사용한다. / 색은 예외 색은 16진법으로 변환 해주기 때문

---

# position

- ❤ 부모요소 : position: relative;
- ❤ 자식요소 : position: absolute; 로 하면 자식 요소의 위치가 부모 요소로 바뀐다.

---

# column

- ❤ 글씨를 여러단으로 출력 해주는 속성
- ❤ column-**count**: 3; 문단 3개로 바꿔줌
- ❤ column-**gap**: 30px; 컬럼 사이 여백
- ❤ column-**rule**: 2px dashed chocolate; 컬럼 사이 **선** 생성
- column-span: all;  /  값은 all, none 2개 있다

![Untitled](Untitled%20145.png)

![Untitled](Untitled%20146.png)

![Untitled](Untitled%20147.png)

---

# float

- ❤ float : 공중으로 뜬다 라는 뜻 먼저 작성된 html 요소 한테는 먹지 않는다.
- ❤ float: left; → 공중으로 떠서 : 화면 왼쪽으로간다; -> 라는 뜻
- ❤ **너비가 없으면 작동하지 않는다.** margin:0 auto; 와 원리가 같음

---

# clear

- ❤ float 자체가 띄워서 좌, 우로 정렬 해주는 기능이기 때문에 float효과를 못 받은 형제 요소나 float 보다 크기가 작은 부모 요소가 있을 경우 정렬이 제대로 안되고 겹쳐진다. 그때 사용하는 요소
- ❤ 부모와 자식 관계중 자식에만 float이 되면 부모가 높이를 가지지 못한다.
- ❤ clear : left;
- ❤ clear : right;
- ❤ clear : both;
- 해결방법
    - ❤ 부모 요소에 높이 너비를 준다. 자식이 부모 보다 크면 안된다. 자식을 감싸도록 부모가 커야한다. -> 단점 가변적으로 변화가 안됨(자식이 커지면 부모가 커져야 하는데 안됨) -> 사용 안하는게 조음
    - ❤ float 된 자식요소 마지막에 형제 요소로 빈 div를 넣고 clear: 속성 준다.
    - ❤ ::after를 이용해서 한다. -> 자식으로 가니까 p.coffee 아래로 간다. 2번 div랑 같음 / display : block 까지 해줘야 한다. 인라인 요소 이기 때문
    
    ```html
    div.mydrink::after{
              content: '';
              clear: both;
              display: block;
            }
    ```
    
    - ❤ class 명 통일한다.(cf, clear fix 등으로 통일 해서 class에 다 붙인다.) 제일 많이 씀
    
    <aside>
    💡 .cf::after{
    content: '';
    clear: both;
    display: block;
    }
    
    </aside>
    
    - ❤ 부모 요소에 overflow를 준다. -> 단점 : 스크롤 주거나, 이용 약관 등 을 줄 때는 못쓴다. 그때는 4번 방식을 사용
    스크롤을 overflow-y : scroll;
    
    ```jsx
    .mydrink{
    overflow: auto; 이나
    overflow: hidden;
    }
    ```