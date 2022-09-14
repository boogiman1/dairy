# 1일차 식별자의 종류 / const, var, let / const / document.write(''); → 문서 자료형 선언하기 / alert() 팝업창 / console 개발자모드 console창에 기록을 보여준다. / 숫자 자료형 / 논리자료형(bool, boolean) /  논리합, 논리곱 연산자 / prompt() → 입력 팝업창 출력 / 기본값으로 ,“글자” 를 입력한다.

꿀 팁 표시: ❤ 노랑 배경글
상태: JAVA Script
작성일시: 2022년 8월 8일 오후 7:11

# 식별자의 종류

![Untitled](Untitled%20184.png)

- ❤ **document.write(result)** → **write : 메소드** / **result : 변수 // 식별자 뒤 괄호 있고 다른 식별자와 사용 = 메소드 write // 식별자 뒤 괄호 없고 단독으로 사용 = result 변수**
- ❤ **var age = prompt() → prompt : 함수 // 식별자 뒤 괄호 있고 단독으로 사용 = 함수 prompt()**
- ❤ **console.log('망고 엉덩이'.length); → length : 속성 // 식별자 뒤에 괄호 없고, 다른 식별자와 사용 = length 속성 // 식별자 뒤에 괄호 있고, 다른 식별자와 사용 = log() 메소드**
- 메소드도 함수이지만 누군가에게 종속 될 수 있는 함수, 메소드는 함수가 될 수 있지만 함수는 메소드가 될 수 없다. (함수 > 메소드)
- ❤ **함수는 그냥 행동, 메소드는 지정한 놈이 행동**

---

# const, var, let

- ❤ const, var, let → 어떠한 값을 저장하는 변수
- ❤ const : 상수
- ❤ var, let : 변수
- const, let은 6버전에 추가되어서 익스에서 안됨 / 리엑트나 다른 프로그램에서 사용하기 때문에 알아야한다.

---

# const

- ❤ const : 상수 = 항상 같은 수
- ❤ 예시) **const pi=3.141592** → **/ const 이름정하기=우항 /**→ 좌항에(**정한 이름**에) **우항을 넣다** → **이름 정한것 =우항**
- ❤ 예시) **console.log(pi); → 개발자 모드 console 에 pi 값을 나타낸다.**
    - **console.log() → 개발자 모드에 나타나는 값**

![Untitled](Untitled%20185.png)

![Untitled](Untitled%20186.png)

- ❤  예시) **console.log(’pi’); → 작은 따옴표를 사용하면 pi라는 글자가 입력된다.**

![Untitled](Untitled%20187.png)

![Untitled](Untitled%20188.png)

- ❤ 예시) **console.log(pi*5); → 사칙연산이 가능하다.**

![Untitled](Untitled%20189.png)

![Untitled](Untitled%20190.png)

- ❤ **const name="김망고";**
     **const name="이종민";** / 상수는 항상 변하지 않는 수 이기 때문에 **중복 값 x** / **바뀔 수 없다**
- ❤ const mango="mango는 예쁘다";
     mango="그리고 귀엽다"  로 ***중간에 변경 할 수 없다!!!!!!!!!!!***
- ❤ **바꿀려면 let을 사용**해야한다. ***변수 let***
let mango="mango는 예쁘다";
mango="그리고 귀엽다"

---

# document.write(''); → 문서 자료형 선언하기 → 문서 자료형 선언하기

- ❤ document.write(''); → 문서 자료형 선언하기
    - .write(); → 문서로 보여준다.
    - document : html문서 body를의미
    - **document.write(''); → html 문서. 명령어(’소괄호’) → 소괄호 안에 있는 글자를 써준다. 큰 따옴표 작은 따옴표 구분 없다.**
    - **document.write('망고야');**
    - document.write("공가져와");
    
    ![Untitled](Untitled%20191.png)
    
- ❤ document.write(공가져와); -> **애러가 뜬다 / 괄호 안에 따옴표 없이 작성 가능한건 변수와 숫자 뿐이다.**
- ❤ **document.write(" \"공 \" 가져와"); → 따움표 안에 따움표는 출력용이다 \ 를 사용하지 않으면 애러가 뜬다. 큰따움표 안에 작은 따움표는 되지만 큰따움표 안에 큰 따움표는 못들어가기 때문에 \ 사용해야한다.**

---

# alert() 팝업창 띄어준다.

- ❤ const hip='김망고\n'+'귀염둥이'+'공주’ → 으로 지정해준다. 여기서 \n 은 new line 줄바꿈 / +는 옆으로 온다.
- ❤ alert(hip);

![Untitled](Untitled%20192.png)

---

# console 개발자모드 console창에 기록을 보여준다.

- ❤ **console.log(); → log탭이 단축키 / 개발자모드 콘솔창에 기록을 보여준다.**
- ❤ console.log(’망고 엉덩이’.length); → **length -> 속성**이라고 불린다 / 어떠한 문자 뒤에 .length 를 하면 **글자수 표현해준다**. **띄어쓰기 인식**
- ❤ console.log(’망고 엉덩이’[0]); → **글자 맨 앞 글자만 찍고 싶을 때 [0]을 사용**한다.
    - [0] : index 번호는 0부터 / 글자 하나당 고유 번호가 붙는데 그걸 **index 번호라고 부른다.**

![Untitled](Untitled%20193.png)

![Untitled](Untitled%20194.png)

---

# 숫자 자료형

![Untitled](Untitled%20195.png)

---

# 논리자료형(bool, boolean)

- ❤ 참, 거짓을 나타내는 자료형 비교연산자 / 연산자와 같이 써야 확인 가능
- 예시)

<aside>
💡 let a=52;
let b=273;
let c='52'

</aside>

로 변수를 준다. **c는 숫자가 아닌 문자라는것을 의미 ‘’ 안에 사용했음**

❤ document.write(a>b); → 화면에 false 표시

![Untitled](Untitled%20196.png)

![Untitled](Untitled%20197.png)

❤ document.write(a<b); → > 화면에 true 출력

![Untitled](Untitled%20198.png)

![Untitled](Untitled%20199.png)

❤ document.write(**`**<br /> 52 > 273 은 **${a>b}** <br/>**`**); → **${a>b}**는 문자자료와 숫자를 같이 출력 하려면 **``(백틱)으로 안에 함수를 감싸야한다.** 그 후 변수를 **${}** 안에 사용한다.

![Untitled](Untitled%20200.png)

![Untitled](Untitled%20201.png)

❤ document.write(a**==**b); → false로 화면에 출력 / 보통 **= 한개는 변수를 줄때 좌항에 우항을 넣다란 뜻**이지만 **== 2개를 써야 우리가 아는 a와 b는 같다?라는 뜻**이다.

![Untitled](Untitled%20202.png)

![Untitled](Untitled%20203.png)

❤ document.write(a===b); → === 3개는 자료형 까지 구분해준다 / 자료형은 문자인지 숫자인지까지

❤ **document.write(a==c);** → true 가 나오는 이유는 **형 상관 없이 값이 같으면 같다 한다.**

![Untitled](Untitled%20204.png)

![Untitled](Untitled%20205.png)

❤ document.write(a**===**c); → false가 출력된다. **=== 3개는 자료형 까지 봐주기 때문**

![Untitled](Untitled%20206.png)

![Untitled](Untitled%20207.png)

❤ **document.write(a!=b); → true로 출력 된다.**  **프로그램에서 ! 는 부정을 표시**한다. 즉 **반대값 출력**

![Untitled](Untitled%20208.png)

![Untitled](Untitled%20209.png)

❤ **document.write(a!==c); → true 로 출력된다.  !== 은 자료의 형태까지 비교 / 형태가 달라서 false이나 ! 때문에 true가 된다.**

![Untitled](Untitled%20210.png)

![Untitled](Untitled%20211.png)

---

# 논리합, 논리곱 연산자

- ❤ **A && B -> and 연산자 / A, B 모두 true 면 true**
- ❤ **A || B -> or 연산자 / A 나 B 중 하나만 true 면 true**
- 예시) **const x = (7>6)&&(1>8);**
    - document.write(x); → false로 출력, 왜냐하면 **1개가 틀리기 때문**이다.

![Untitled](Untitled%20212.png)

![Untitled](Untitled%20213.png)

- 예시) **const y = (7>6) || (1>8);**
    - document.write(y); → true 로 출력, 왜냐하면 **1개라도 맞기 때문**
    
    ![Untitled](Untitled%20214.png)
    

![Untitled](Untitled%20215.png)

- 예시) **const z=!(7>6);**
    - document.write(z); → false로 출력, 원래는 true 이나 **! 때문에 false로 나온다**
    
    ![Untitled](Untitled%20216.png)
    

![Untitled](Untitled%20217.png)

![Untitled](Untitled%20218.png)

![Untitled](Untitled%20219.png)

---

# prompt() → 입력 팝업창 출력 / 기본값으로 ,“글자” 를 입력한다.

- ❤ 예시) **var gender = prompt(”당신의 성별은”,”여성”)**
- ❤          변수 / gender라는 이름 정함 / = 팝업창에 “당신의 성별은” 이란 질문에 답변 “여성”이 기본 값으로 나온다.

![Untitled](Untitled%20220.png)

![Untitled](Untitled%20221.png)