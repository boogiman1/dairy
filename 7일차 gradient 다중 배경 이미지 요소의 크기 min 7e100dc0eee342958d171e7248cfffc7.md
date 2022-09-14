# 7일차 gradient / 다중 배경 이미지 / 요소의 크기 min-height : 최소 높이 지정 / padding / margin / outline 테두리 외곽에 아우트라인 처리하기 / border-radius 둥근 테두리 / border-image 테두리 이미지 / box-sizing / float: left; / box-shadow / transform 변이 / transition 전이

꿀 팁 표시: ❤ 노랑 배경글
상태: CSS
작성일시: 2022년 7월 13일 오후 8:39

# gradient

- ❤ background-**image 속성 안에 적용** 해야한다.
- ❤ **기본 :** background : linear-gradient( 색, 색, 색) → 색을 계속 추가 할 수 있다.
- ❤ **방향 조절 :** background : linear-gradient( **to 방향**, 색, 색, 색) → **방향 조절 : 색상 앞에 작성**한다. (**방향 : top, bottom, right, left** 2개 같이 쓸 수도 있다.)
- ❤ **각도 조절 :** background : linear-gradient(**30deg**, 색, 색, 색) → **방향 각도 조절** : deg 단위를 사용한다. 양수 음수 가능
- ❤ **투명도** : background : linear-gradient(**rgba(), rgba()**); → **투명도 조절은 rgba를 통해서 가능**하다.
- ❤ **영역 퍼센트** : background : linear-gradient(색상 **%**, 색상 **%**, 색상 **%**) → **%를 사용하여 영역을 지정**한 수 있다.
- ❤ **반복** : background : **repeating**-linear-gradient(색상, 색상%, 색상%) → **2개 이상 %가 들어가야 하며 repeating을 사용**한다.
- ❤ **중앙부터 시작** : background : **radial**-gradient(색상, 색상, 색상) → 중간 부터 시작한다.
- ❤ **동그라미로 생김** : background : radial-gradient(**circle**, 색상, 색상, 색상) → 중간 부터 시작을 원으로 보이게 한다
- ❤ **중앙 시작 반복** : background : **repeating**-radial-gradient(색상%, 색상%, 색상%)
- ❤ colorzilla 사용 시

![Untitled](Untitled%20223.png)

번외

그라디언트 중심점 이동 교재 p.188
- closest-corner 끝 모앙이 그레디언트 중앙에서 가장 가까운 모서리로 흐려짐.
- closest-side 끝 모양이 그레디언트 중앙에서 가장 가까운 변으로 흐려짐.
- farthest-corner 기본값. 그레디언트 중앙에서 가장 먼 모서리로 흐려짐
- farthest-side 그레디언트 중앙에서 가장 먼 변으로 흐려짐

---

# 다중 배경이미지

- ❤ background-image : url(), url() ; → **url 을 여러번 사용 하면서 가능**하다. **앞에 작성한 이미지가 맨 위로 온다**
- ❤ 그리고 속성을 적용 하고 싶으면 순서에 맞게 적용시켜준다.
gradient 는 image 속성에 넣어야 적용된다

![Untitled](Untitled%20224.png)

---

# 요소의 크기

- ❤ **min-height : 최소 높이 지정**
- ❤ height 는 고정 값이기 때문에 컨텐츠가 넘치면 박스를 넘어 버리지만 **min-height 는 박스가 늘어나고 최소 값 보단 안작아진다.**

---

# padding 요소의 안 여백

- ❤ **padding도 박스 크기에 영향을 미친다.**
- padding 은 위부터 시계 방향으로 4방향 크기를 줄 수 있다. 기본적으로 무조건 위부터 시계방향으로 적용 된다고 보면 됨
- padding : 위 오른쪽 아래 왼쪽
- padding : 값을 1개 쓰면 자동으로 4방향이 같은 값으로 적용된다.
- padding : 값을 2개 쓰면 자동으로 4방향이 되면 위=아래 오른쪽=왼쪽 값이 된다.
- padding : 값을 3개 쓰면 위 오른쪽 아래 왼쪽(=오른쪽)

---

# margin 요소의 바깥 여백

- margin: 200px; 위 아래 방향 마진은 겹친다. 병합 현상이 있다. 상하 마진을 적용 할 때는 위, 아래 한쪽 방향으로만 코딩 좌우는 겹치지 않아서 400px 만큼 벌어진다.
- ❤ 이렇게 하나를 줘도 합쳐질 때 큰 값으로 합쳐진다. 200으로 적용
    
    margin: 200px;
    margin-top: 50px;
    
- ❤ margin : 0 auto; → 중앙 정렬 가능 / 단 마진으론 **수평 정렬만 가능** 그리고 **꼭 너비가 있어야 한다**💥💥💥 / **inline 요소에는 사용 불가**

---

# outline 테두리 외곽에 아우트라인 처리하기

- ❤ outline-style : 박스 밖 테두리 스타일
- ❤ outline-width : 외각선 두깨
- ❤ outline-color : 외각선 색
- ❤ **outline-offset : 외각선이 얼마나 떨어져 생길지 작성**

---

# border-radius 둥근 테두리

- ❤ border-radius : 왼쪽 상단 모서리부터 4방향이 둥글게 먹는다. 자기 크기만큼 주면 중심점 기준으로 원이 된다.(border-radius: 100px;)
- ❤ border-radius: 100px 100px 0 0; -> 왼쪽 모서리 부터 둥글게 먹으니까 위 두개만 둥글게 된다.
- ❤ 1개 2개 3개 4개 적용 하는 방향 및 **시스템은 padding, margin과 같다**. **면**에서 **꼭지점**으로 바뀔 뿐
    
    ![Untitled](Untitled%20225.png)
    
- border-radius: 15px / 70px; 꼭지점 기준으로 원의 반지름이 가로 방향(x축)으로 15px 세로 방향(y축)으로 70px만큼 생긴다

![Untitled](Untitled%20226.png)

![Untitled](Untitled%20227.png)

---

# border-image 테두리 이미지

- border : 1px solid transparent → **transparent 사용 하면 테두리가 투명이 된다**
- ❤ border-image : url(); → 4개의 꼭지점에 이미지가 생긴다.
- ❤ border-image: url(img/border.png) 20; → 각 꼭지점을 20만큼 늘려준다.
- ❤ border-image: linear-gradient(red,blue) 27; → 그라데이션 추가
- ❤ border-image: url(img/border.png) 20 repeat; → 반복

---

# box-sizing

- ❤ box-sizing: border-box; **width, height 안에 border 영역까지 딱 들어가게 해주는것** / **width, height 가 없으면 컨텐츠 영역 안으로 들어간다**.
- box-sizing : border-box 는padding + border + content-box가 안에 다 들어간다
- box-sizing : content-box 는padding + border + content-box가 다 각각 따로 더해진다

---

# float: left;

- ❤ **float: left; -> 옆으로 나열 시켜주는 속성 / 줘도 옆으로 안생기면 공간이 부족해서 그렇다 -> 여기선 그래서 부모 너비 늘려줌**

---

# box-shadow

- p.shadow{box-shadow : 8px 15px 8px rgba(255, 255, 0, .5);}
p.shadow{box-shadow : x축 y축 블러값(번짐) 색상;}
- p.shadow4{box-shadow:8px 15px 8px 7px rgba(0, 0, 50, .4);}
p.shadow1{box-shadow:x 축 y 축 블러값(번짐), 스프레드(강함) 색상;}
- p.shadow5{box-shadow:8px 15px 10px inset rgba(0, 0, 50, .4);}
inset : 컨텐츠를 들여박은거 처럼 보여줌 / 안쪽 그림자 느낌
- p.shadow6{box-shadow:5px 5px 5px 8px darkblue, -5px -5px 5px 8px violet;}
그림자 2개 적용 가능

---

# transform 변이

- ❤ 속성으로 요소에 회전, 크기 조절, 기울이기, 이동 효과를 부여할 수 있습니다.
- ❤ 형태 → **transform : 효과 속성 (  ) ;**
- ❤ translate : x축, y축; → **위치를 옮기는 속성**
- ❤ rotate : 숫자 deg ; → **deg각도 만큼 회전** 시켜줌
- ❤ scale : x축, y축 → 만큼 **크기 조절**
    - 💕 **scale(2) → 2배 커짐**
- ❤ skew : deg, deg → deg 만큼 **뒤틀리게** 해줌
- 💕 **origin** : **중심점 이동** → **origin(x축 y축)**

---

# transition 전이

- ❤ 바뀌는 중간 과정을 보여주는 요소
- ❤ transition은 hover한테 주는게 아니라 원래 속성에 준다. hover에 주면 마우스를 때자마자 끊기는 현상 발생
- ❤ transition을 사용 하려면 hover에 같은 속성이 들어가야 한다.
- transition : all 1s; → 모든 반응 속도 1초로 해준다.
- transition-property : 트랜지션의 대상이 되는 css를 정해준다. 기본 값 : all
- transition-duration : 트랜지션이 일어나는 시간 설정
- transition-timing-function : 트랜지션 효과를 위한 수치 함수를 지정한다.
- transition-delay **:** 프로퍼티가 변화한 시점과 트랜지션이 실제로 시작하는 사이에 대기하는 시간을 초 단위(s) 또는 밀리 초 단위(ms)로 지정한다

![Untitled](Untitled%20228.png)