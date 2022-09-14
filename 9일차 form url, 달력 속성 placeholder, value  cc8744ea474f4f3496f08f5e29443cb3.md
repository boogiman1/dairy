# 9일차 form url, 달력 / 속성 placeholder, value 차이 autocomplete, pattern, multiple, disabled, readonly /   웹 사이트 구조요소 header, section, fooer

꿀 팁 표시: ❤ 노랑 배경글
목차: url, 달력 / 속성 placeholder, value 차이 autocomplete, pattern, multiple, disabled, readonly /   웹 사이트 구조요소 header, section, fooer
상태: HTML
작성일시: 2022년 6월 29일 오후 9:07

# form input 마무리

url : email 처럼 url 형식과 일치하는지 검사한다. http:// 까지 사용해야 한다.

![Untitled](Untitled%20101.png)

![Untitled](Untitled%20102.png)

---

# 달력

달력 type은 디자인 변경이 어렵기 때문에 잘 사용하지 않는다.

![Untitled](Untitled%20103.png)

![Untitled](Untitled%20104.png)

---

# form 속성

❤ autocomplete : 자동완성 기능 **name을 꼭 작성해야 가능**하다.

❤**비밀번호에 꼭 autocomplete=”off” 속성 추가해준다. 자동완성 속성 / 사용 안하면 기본 속성이 autocomplete=”on”이기 때문에 자동완성이 되기 때문**

❤ placeholder : 사용자가 클릭하면 글자 사라짐

❤ value : 사용자가 직접 클릭 해야만 사라짐

❤ placeholder, value 둘의 차이는 placeholder가 value 이후에생김 그래서 placeholder는 익스9 전버전에선 사용이 안된다. value는 값이 서버에 저장되지만 placeholder는 아니다.

[caniuse.com](http://caniuse.com) 에서 사이트 호환성 확인 가능.

![Untitled](Untitled%20105.png)

![Untitled](Untitled%20106.png)

❤ pattern : 정규 표현식이라고 한다.

pattern="\d{6}-\d{7}" 앞자리 6자리 뒷자리 7자리 형식을 하라고 한다.
d:숫자, {}:자릿수 // 주민등록번호 양식에 맞게 사용 가능

![Untitled](Untitled%20107.png)

![Untitled](Untitled%20108.png)

❤ multiple : file 타입에 첨부파일 여러개 올릴 수 있다.

![Untitled](Untitled%20109.png)

![Untitled](Untitled%20110.png)

❤ disabled : 비활성화 속성. 예를들면 시리얼 번호가 정품이면 다음 버튼이 되게 활성화 하게한다.

❤ readonly : 읽기전용, 사용자가 변경하지 못하게 할때 사용 input 중 text에만 사용가능, 사용자가 value 수정 불가능

![Untitled](Untitled%20111.png)

![Untitled](Untitled%20112.png)

---

# 웹사이트 구조

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>구조요소</title>
    <link rel="stylesheet" href="style.css">
    <!-- link 탭 href 에 css확장차 넣기
        이렇게 하는게 웹 표준
        ctrl 누른 상태에서 href 눌러서 파일 만들고 시작
        rel : 걸리는 링크와 html의 관계를 묻는것
        href : 파일 경로 -->
</head>
<body>
    <div id="wrap">
        <header>
            <h1><a href="#">반응형웹</a></h1>
            <nav>
                <ul>
                    <li><a href="#">menu1</a></li>
                    <li><a href="#">menu2</a></li>
                    <li><a href="#">menu3</a></li>
                    <li><a href="#">menu4</a></li>
                    <li><a href="#">menu5</a></li>
                </ul>
            </nav>
            <!-- nav는 보통 header 하위에 드렁간다 -->
        </header>
        <div id="container">
            <section>
                <h2>컨텐츠 그룹 1</h2>
            </section>
            <section>
                <h2>컨텐츠 그룹 2</h2>
            </section>
            <div>
                <article>
                    <h2>주요기사</h2>
                    <!-- article 독립적으로 배포가 가능한 기사나 블로그 처럼 주요 컨텐츠가 아니라 웹 사이트에서 독립적으로 베포할 수 있는 마크업 -->
                </article>
                <aside>
                    광고
                    <!-- 광고 영역을 보통 aside 태그로 만든다 -->
                </aside>
            </div>
        </div>
        <footer>
            <address>회사주소 경기도 부천시</address>
            <p>copyright all right reserved.</p>
        </footer>
    </div>
</body>
</html>
```

div로 그루핑 해준다

❤header : 헤더 영역 / 제목 네비게이션 검색 등

❤ nav는 보통 header 하위에 들어간다.

❤section : 맥락이 같은 요소를 주제별로 그룹핑 / 섹션주제에 대한 제목 <h2>~<h6>를 작성하는것이 좋다

❤ article 독립적으로 배포가 가능한 기사나 블로그 처럼 주요 컨텐츠가 아니라 웹 사이트에서 독립적으로 베포할 수 있는 마크업

❤ 광고 영역을 보통 aside 태그로 만든다