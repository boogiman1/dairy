# 10일차 audio, video, track, iframe 태그 (마지막)

꿀 팁 표시: ❤ 노랑 배경글
목차: audio, video, iframe 태그
상태: HTML
작성일시: 2022년 7월 4일 오후 10:49

# audio 태그

```html
<audio>
    <source src="media/applause.wav">
  </audio>
```

❤ 그냥 작성 하면 소리도 나지 않고 화면에 나타나지 않는다. audio 태그 안에 controls 가 없어서 그렇다. (video 태그도 controls 없으면 재생이 안된다)

```html
<audio src="media/applause.wav" controls autoplay muted loop>
    
  </audio>
```

![Untitled](Untitled%2096.png)

이렇게 보인다.

<속성>

❤ autoplay : 자동 재생기능 / 사용해도 자동재생이 안되는게 정상이다. 웹 접근성에 위배되기 때문 / 시각 장애인 분들이 놀래기 때문에 muted 음소거 기능이 없는 이상 재생 안되게 해놨다.

❤ muted : 음소거 기능

❤ loop : 반복재생 기능

---

# video 태그

```html
<video width="800" controls autoplay muted loop poster="src/images/prince/pic3.JPG">
    </video>
```

audio 태그와 속성은 같다

❤ poster : 동영상의 썸네일

```html
<video width="800" controls autoplay muted loop poster="src/images/prince/pic3.JPG">
    </video>
```

![Untitled](Untitled%2097.png)

**track 태그**

❤ track : 동영상의 자막을 넣는 기능 / track 태그는 자동으로 생성 되지 않는다. vs code enn(앤잇)에 등록 되어 있지 않기 때문 / 자막 확장자는 vtt / 

**track 태그 속성**

❤ srclang : 자막 언어

❤ lable : 제목

❤ kind : 종류

```html
<video src="media/mango.mp4" controls muted autoplay poster="src/images/prince/pic3.JPG">
        <track  src="media/subtitle_ko.vtt" srclang="ko" lable="korean" kind="subtitles"/>
        <track  src="media/subtitle_en.vtt" srclang="en" lable="english" kind="subtitles"/>
    </video>
```

![Untitled](Untitled%2098.png)

---

# iframe 태그

**웹 접근성에서 iframe 사용하는 것을 권장하지 않는다**. 검색앤진 최적화에도 안좋다. html 문서는 하나만 인정하는데 html 문서 안에 html이 들어오는 격이기 때문에 검색앤진에 검색이 안된다. 그래서 기계가 인식을 못하기 때문

```html
<iframe src="ex1-39-1.html" frameborder="0" width="500" height="500">
    </iframe>
    <iframe src="table_q1.html" frameborder="0" height="500"></iframe>
    <iframe src="http://icoxpublish.com/" frameborder="0"></iframe>
    <iframe src="https://www.melon.com/" frameborder="0"></iframe>
```

![Untitled](Untitled%2099.png)

속성

frameborder : 아이프레임 보더를 넣는 속성

**iframe 네임엥커**

a 태그 target 속성에 임시 네이밍 작성 후 iframe 태그 안에 name 속성에 같이 적어준다.

```html
<nav>
        <ul>
            <li><a href="ex1-18-2.html" target="mainframe">네임엥커</a></li>
            <li><a href="ex1-34.html" target="mainframe">ㅁㄴㅇㄹ</a></li>
            <li><a href="ex1-24.html" target="mainframe">네임엥커</a></li>
            <li><a href="form_test.html" target="mainframe">폼 테스트</a></li>
        </ul>
    </nav>
    <hr>
    <iframe src="ex1-18-2.html" frameborder="0" width="800" height="500" name="mainframe">
    <iframe src="ex1-34.html" frameborder="0" width="800" height="500" name="mainframe">
    <iframe src="ex1-24.html" frameborder="0" width="800" height="500" name="mainframe">
    <iframe src="form_test.html" frameborder="0" width="800" height="500" name="mainframe">
```

![Untitled](Untitled%20100.png)