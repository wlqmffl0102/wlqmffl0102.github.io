---
title: 첫 포스팅 작성하기 - 마크다운(Markdown)
author: Dodev 하다
date: 2021-10-02 11:07:00 +0900
categories: [GitHub Blog]
tags: [GitHub Blog, How to, Study]
---
## 초보자를 위한 GitHub Blog 만들기 시리즈
[초보자를 위한 GitHub Blog 만들기 - 1](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-1/)

[초보자를 위한 GitHub Blog 만들기 - 2](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-2/)

[초보자를 위한 GitHub Blog 만들기 - 3](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-3/)

[초보자를 위한 GitHub Blog 만들기 - 4](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-4/)
<br>
<br>

## 두서
---
힘들었던 블로그 생성을 다 마치고 나서도 끝은 아닙니다. 블로그가 생겼으니 블로그를 운영해야 하지요.
지킬테마+깃헙페이지 를 이용해 만든 깃 블로그는 md파일을 사용하여 블로그 포스팅을 작성, 업로드 할 수 있습니다.

네이버 블로그, 티스토리, 브런치 등등.. 여러 플랫폼에는 블로그 자체에 "새글쓰기" 혹은 "새 게시물 작성"등의 버튼이 있고,
포스팅을 위한 에디터가 나와, 블로그 자체에서 글을 씁니다.

하지만 깃헙페이지는 그런식으로 운영되지는 않습니다. markdown문서를 작성하여 새 포스팅을 작성 할 수 있는데, 이번 것도 차근차근 시작하겠습니다!
<br>
<br>

## 마크다운(Markdown(.md / .markdown)) 이란?
---
> Markdown은 텍스트 기반의 마크업언어로 2004년 존 그루버에 의해 만들어졌으며 쉽게 쓰고 읽을 수 있으며 HTML로 변환이 가능하다. 특수기호와 문자를 이용한 매우 간단한 구조의 문법을 사용하여 웹에서도 보다 빠르게 컨텐츠를 작성하고 보다 직관적으로 인식할 수 있다. 마크다운이 최근 각광받기 시작한 이유는 깃헙(https://github.com) 덕분이다. 깃헙의 저장소(Repository)에 관한 정보를 기록하는 README.md는 깃헙을 사용하는 사람이라면 누구나 가장 먼저 접하게 되는 마크다운 문서였다. 마크다운을 통해서 설치방법, 소스코드 설명, 이슈 등을 간단하게 기록하고 가독성을 높일 수 있다는 강점이 부각되면서 점점 여러 곳으로 퍼져가게 된다.

웹을 이루는 가장 기초적인 구성 요소인 HTML이라고 하는 녀석이 있습니다. HTML은 Hyper Text **Markup** language의 약자 입니다.
여러가지 많은 설명들이 있습니다만, 간단히 이야기 하자면 Markup은 텍스트를 이용해 구조를 만드는 것 입니다. 일반 plain text와 태그를 이용하여 정의를 하는 것 입니다.
그런데, 이 마크업(markup)문서는 작성하는법이 귀찮고 까다롭습니다. 그렇기 때문에 더 쉽게 페이지를 작성 할 수 있는 문법이 나오게 되었는데, 그것이 바로 마크다운(Markdown) 입니다.

**Markdown**이란, plain text와 몇가지 특수기호를 이용해서 서식이 있는 문서를 만드는 것 입니다.

간단한 사용, html로 변환가능, 버전 관리 용이 등의 이점이 있습니다.
그러나 표준이 없어 어떤 에디터를 사용하느냐에 따라 다른 결과물이 나올 수 있습니다.
<br>
<br>

아직까지도 잘 이해가 안 갈 수 있습니다.
다만, 중요한점은 Markup과 Markdown은 서로 상충하는것이 아니라는 점입니다.
Markup과 Markdown은 동일한 행위를 다른 방식으로 진행하는 것 뿐이지요.

아래의 설명을 보시면 더 편하게 이해가실 것 입니다.

Markup(HTML)에서는, 어떠한 문장 또는 단어를 "굵게"처리하기 위해서는
```html
안녕하세요. 저는 <b>Dodev-하다</b> 입니다.
```
와 같은 형식으로 사용해야 합니다. <b></b>태그 사이에 있는 것은 굵게 표시 한다. 라는 뜻이예요.

하지만 Markdown에서는
```markdown
안녕하세요. 저는 **Dodev-하다** 입니다.
```
와 같은 형식으로 사용합니다. ** 사이에 있는 것은 굵게 표시한다. 라는 뜻입니다.

똑같은 행위를 그저 다른 방식으로 진행합니다. markup은 태그를 이용해서, markdown은 일반텍스트와 몇가지 특수 기호를 이용해서요.

Markup과 Markdown은 나름데로 복잡합니다. 다만 markdown쪽이 아무래도 조금 더 쉽습니다. 그렇지만 나름데로의 문법이 존재하기 때문에, 처음 접하신다면 익숙하지 않으실 수 있습니다.

하지만 누구나 자주 보셨을 법한 Markdown문법이 있습니다. 바로 인스타, 페이스북 등 각종 SNS에서 사용하는것인데요.
SNS상에서 누군가를 태그하고 싶다면 "@"를 앞에 붙입니다. @wlqmffl0102 이런식으로 말이죠.
이때, **@**가 바로 일반인들이 자주보는 markdown언어 중 하나입니다.
![Desktop View](/assets/img/2021-10-02/1.jpg){: width="50%" } 

여러가지 Markdown문법에 관해 알아보도록 하겠습니다.
<br>
<br>

## 마크다운(Markdown) 기본문법
---
- 헤더(Header) : 제목
    ```markdown
    # 제목 1단계
    ## 제목 2단계  
    ### 제목 3단계
    #### 제목 4단계
    ##### 제목 5단계
    ###### 제목 6단계 
    ```

# 제목 1단계
<h2 data-toc-skip>제목 2단계</h2>

<h3 data-toc-skip>제목 3단계</h3>

#### 제목 4단계
##### 제목 5단계
###### 제목 6단계 
<br>
<br>

현재 필자가 사용중인 jekyll-theme-chirpy에서는 3단계까지만 toc메뉴에 걸립니다.

1~3단계를 사용하는 중, toc메뉴에 걸리지 않도록 하고 싶다면 아래와 같이 작성합니다.
```html
<h2 data-toc-skip>H2 - heading</h2>

<h3 data-toc-skip>H3 - heading</h3>
```

참고* jekyll-theme-chirpy에서는 1~3단계 제목 수준을 지키더라도 제목 글이 숫자로 시작되면 toc메뉴에서 제외됨.

---
- 수평선 : 게시글의 명시적 구분
    ```markdown
    ---
    ```
---
---

- 줄바꿈(개행) : 글 라인을 바꾸고 싶을 때.
    ```markdown
    단어 / 문장 사이에  띄워쓰기를 2번 하면 개행 됨.
    ```
단어 / 문장 사이에  띄워쓰기를 2번 하면 개행 됨.

참고* jekyll-theme-chirpy에서는 해당 방법으로 개행되지 않음

---

- 강조 : 문장 또는 단어 꾸밈
  ```markdown
  __볼드(굵게)__ 또는 **볼드(굵게)**   
  _이탤릭체(기울임)_    
  ~~취소선~~  
  <u>밑줄(태그를 이용한 쓰임)</u> 

  **여러가지 강조를 _중복하여서_ 사용도 가능하다**
  ```
__볼드(굵게)__ 또는 **볼드(굵게)**   
_이탤릭체(기울임)_    
~~취소선~~  
<u>밑줄(태그를 이용한 쓰임)</u>

**여러가지 강조를 _중복하여서_ 사용도 가능하다**

---

- 리스트
  - Ordered list(순서가 있는 리스트)

  ```markdown
  1. Firstly
  2. Secondly
  3. Thirdly
  ```

  1. Firstly
  2. Secondly
  3. Thirdly

  - Unordered list(순서가 없는 리스트) : 글머리 기호 __*__, __+__, **-** 지원

  ```markdown
  - Chapter
  - Section
    - Paragraph
  ```

  - Chapter
  - Section
    - Paragraph
<br>

  - Task list

  ```markdown
  - [ ] TODO
    - [x] Completed
    - [ ] Defeat COVID-19
      - [x] Vaccine production
      - [ ] Economic recovery
      - [ ] People smile again
  ```

  - [ ] TODO
  - [x] Completed
  - [ ] Defeat COVID-19
    - [x] Vaccine production
    - [ ] Economic recovery
    - [ ] People smile again

  - Description list

  ```markdown
  Sun
    : the star around which the earth orbits

  Moon
    : the natural satellite of the earth, visible by reflected light from the sun
  ```

Sun
  : the star around which the earth orbits

Moon
  : the natural satellite of the earth, visible by reflected light from the sun

---


- 인용구 : 중복 사용 가능
  ```markdown
  > "흑백 사진에 글쓰면 명언같다"
  >> 주말의 띵화 (침착맨)
  >>> 침착맨
  ``` 

> "흑백 사진에 글쓰면 명언같다"
>> 주말의 띵화
>>> 침착맨

---

- 링크(Link) : 하이퍼 링크, 클릭시 해당 페이지로 이동
  ```markdown
  깃허브 홈페이지: <https://github.com>

  [Github](https://github.com)
  [Github](https://github.com "마우스 오버시 링크에 대한 설명문 추가 가능")

  [현재 페이지 안에서의 이동(클릭시 "## 두서" 부분으로 이동)](#두서)
  ```

깃허브 홈페이지: <https://github.com>

[Github](https://github.com)

[Github](https://github.com "마우스 오버시 링크에 대한 설명문 추가 가능")

[현재 페이지 안에서의 이동(클릭시 "## 두서" 부분으로 이동)](#두서)
<br>
<br>
현재 페이지 안에서의 이동부분은 조금 특이해서 추가 한다.
> 1. header를 링크로 잡고 특수문자를 지운다.
> 2. 가장 앞 부분에 #을 하나만 넣는다
> 3. 스페이스 바 부분은 모두 "-"으로 바꾼다
> 4. 영어 대문자는 모두 소문자로 바꾼다
> 예) "## 마크다운(Markdown) 기본문법" -> "#마크다운markdown-기본문법"

---

- 이미지 : local에 이미지를 넣는 경우에는 상대경로를 적어줘야 합니다. 보통 이미지는 assets/img폴더 안에 들어갑니다.
  ```markdown 
  ![대체텍스트](https://cdn.jsdelivr.net/gh/cotes2020/chirpy-images/posts/20190808/mockup.png)

  ![대체텍스트](https://cdn.jsdelivr.net/gh/cotes2020/chirpy-images/posts/20190808/mockup.png "마우스 오버시 이미지에 대한 설명문 추가 가능")

  사이즈를 조절하고 싶은 경우 html 태그를 이용하여 처리  
  <img src="https://cdn.jsdelivr.net/gh/cotes2020/chirpy-images/posts/20190808/mockup.png" width="300" height="200"> 

  ```
![대체텍스트](https://cdn.jsdelivr.net/gh/cotes2020/chirpy-images/posts/20190808/mockup.png)

![대체텍스트](https://cdn.jsdelivr.net/gh/cotes2020/chirpy-images/posts/20190808/mockup.png "마우스 오버시 이미지에 대한 설명문 추가 가능")

사이즈를 조절하고 싶은 경우 html 태그를 이용하여 처리  
<img src="https://cdn.jsdelivr.net/gh/cotes2020/chirpy-images/posts/20190808/mockup.png" width="300" height="200"> 
---
<br>
<br>

- 코드 블럭

```markdown
 `Code`입니다. 
 * 이때 사용되는 기호는 '(작은따옴표)가 아니라 `(백틱)이다. 
 특수문자는 자판 숫자 1 바로 앞에 있다. 쉬프트를 누르면 물결(~)표시가 되는 녀석이다.

 이 백틱(`)을 3개씩 위아래로 쓴 다음 그 사이에 코드를 넣어주면 코드 블럭이 된다.

```html
<h1>Hello world!</h1>

처럼 위쪽 백틱 끝에 해당 코드블럭이 어떤언어인지 명시해두면 코드 하이라이팅이 가능하다.
```

 `Code`입니다.

```html
<h1>Hello world!</h1>
```

## 마무리
---
이번에는 markdown 문법 기초에 관해서 알아보았습니다. 
다음 포스팅은 드디어 첫 포스팅을 작성하는 방법과 markdown문서 편집기(에디터)에 관해 다루겠습니다!
<br>
<br>
