---
title: 블로그 커스터마이징 하기
author: Dodev 하다
date: 2021-10-04 10:37:00 +0900
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

## 포스팅 작성하기 시리즈
[첫 포스팅 작성하기 - 마크다운(Markdown)](https://wlqmffl0102.github.io/posts/WritingThe-First-post-1-Markdown-Grammar1/)

[첫 포스팅 작성하기](https://wlqmffl0102.github.io/posts/WritingThe-First-post-2/)
<br>
<br>

## 두서
---
깃허브 블로그도 어느정도 블로그에 모습을 갖췄습니다. 제작자가 만들어둔 테마 그 자체만으로도 예쁩니다만, 그래도 그 테마를 그대로 쓰자니 내 마음에 들게 예쁘게 꾸미고 싶기도 한데 이걸 어떻게 또 해야하나.. 그러면 뭘해야하나.. html? css? js? jquery? 아웅 왜이렇게 힘든게 많아... 아우 귀찮아.. 

사실 간단하다면 간단하고, 어렵다면 어려울 수도 있습니다. 
구조를 완벽히 파악하고, 원하는 코드라인이 무엇인지, 어디에 해당 코드가 있는지 모두 안다면 쉽겠지요. 하지만 저는 내가 뭘 바꾸고싶은지만 알고 있는 분들을 위해 작성하도록 하겠습니다. 뭘 바꾸고싶은지도 모른다면 적어도 "이 버튼 색깔을 바꾸고 싶어", "여기는 이렇게 나오면 좋을것같아"와 같이 희망사항을 대충 생각해오시면 될 것 같습니다.

주먹구구식으로 보이겠지만 이렇게라도 본인의 마음에 쏙 드는 페이지를 만들 수 있다면 좋겠습니다. 입문자에게 깃헙 블로그의 문턱을 낮춰드리고싶습니다.

참고로 jekyll-theme-chirpy테마를 기준으로 작성합니다. 테마마다 구조나, 코드가 모두 다르기 때문에 유의 부탁드립니다.
나는 이 옵션이 있는데 왜 이 블로그에서는 다뤄주지 않지? 나는 이 옵션이 없는데 도대체 뭘 말하는 거지?라고 생각하실 수 있습니다.
블로그에 적혀있지 않으나 본인이 가지고 있는 옵션의 경우에는 테마 제작자 repository의 README.md 참고하여 수정해주시고, 블로그에는 적혀있지만 본인이 가지고 있지 않는 옵션의 경우에는 스킵하시거나 테마 제작자 repository의 README.md 참고하여 수정해주시면 됩니다.
<br>
<br>

## 바꾸고자 하는 곳을 명확하게 짚는다.
---
앞서 말했던 것 처럼 제가 현재 사용중인 jekyll-theme-chirpy테마를 기준으로 작성합니다.

우선 본인이 사용중인 테마의 데모 페이지가 있을것입니다. 그 데모 페이지를 거의 그대로 현재 쓰고 계실건데요. 제가 사용중인 테마의 데모 페이지는  [jekyll-theme-chirpy Demo Page](https://chirpy.cotes.info/)입니다.

![Desktop View](/assets/img/2021-10-04/1.PNG){: width="90%" } 
![Desktop View](/assets/img/2021-10-04/2.PNG){: width="90%" } 

위 사진과 같이 제가 쓰는 테마는 두 가지 모드를 지원합니다. light모드, dark모드. 어느 모드 할 것 없이 군더더기 없이 깔끔하고 컬러도 예쁩니다.
하지만 저는 여기서 **프로필 사진, 블로그 소개말, favicon, 좌측 사이드 바의 컬러, 모드별 하이라이트 컬러** 정도를 변경하고 싶었습니다.

하다가 보면 추가되거나, 변경, 삭제 되는 흐름이 있을겁니다. 그치만 저는 처음부터 "이걸부터 해야만 한다!"보다는 처음에는 "어디가 어떤 모양이면 좋겠어" 혹은 "이건 다른 색 / 이미지라면 좋겠어"와 같은 명확한 생각이 필요하다고 생각합니다.

그렇지 않다면 어딜 어떻게 바꿔야 하는지 조차 알 수 없기 때문이죠. 본인의 테마에서 변경하고 싶은 점이 어느정도 나왔다면 시작할 수 있습니다!
<br>
<br>

## 프로필 사진과 블로그 소개말 변경
---
사실 이 부분은 [이전 포스팅](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-3/)에서 다뤘던 부분입니다.
대부분의 지킬 테마는 _config.yml파일안에 title, tagline, avatar라고 하는 옵션들이 있습니다.

이때 title은 블로그 제목,  tagline은 서브타이틀(블로그 소개말), avatar는 프로필 사진 옵션입니다.
작성시 특수문자가 들어가면 오류가 발생하는 경우도 있습니다. 제목 및 소개말을 작성하였는데 깨지거나, 정상적으로 보이지 않는 경우에는 특수문자를 빼고 작성해보시길 바랍니다.
avatar 이미지가 제대로 보이지 않는 경우에는 이미지의 경로가 올바른지 확인하시면 됩니다.
<br>
<br>

## favicon
---
파비콘 또는 패비콘입니다. 웹 브라우저 상단에 사이트 제목과 함께 아이콘이 뜨지요. 그 아이콘을 favicon이라고 합니다.
![Desktop View](/assets/img/2021-10-04/3.PNG){: width="90%" }

[Real Favicon Generator](https://realfavicongenerator.net/)로 접속합니다. `Select your Favicon image`버튼을 클릭 후 favicon으로 사용하고자 하는 이미지를 업로드 합니다.
잠시 기다리면 여러가지 옵션을 변경 할 수 있는데, 필요한 옵션들을 선택/변경 후 스크롤을 하단으로 쭉 내리시면 `Generate your Favicons and HTML code` 버튼을 눌러줍니다.
다음으로 `Favicon package`버튼을 누르시면 .zip파일이 다운로드 됩니다.

해당 압축파일을 푼 다음, 그 안에서 
- browserconfig.xml
- site.webmanifest

위 두 개의 파일을 삭제 합니다.

나머지 파일들은 assets/img/favicons/ 경로안에 넣어줍니다.
넣어준 뒤 보면 아까 삭제했던 browserconfig.xml과 site.webmanifest가 보이는데요. 이것은 디폴트 파일이라 아까 삭제한것과는 다른 파일입니다. 보여야 정상입니다!

![Desktop View](/assets/img/2021-10-04/4.PNG){: width="40%" }

그 다음, `/_includes/favicons.html`파일을 열어줍니다. 들어가시면 이전에 설정되어있는 favicons정보들이 있습니다. 내용을 변경해야 하기 때문에, 다음과 같이, assets/img/favicons/ 경로에 있는 파일을 추가해주시면 됩니다.
사이즈와 파일명은 다를 수 있기 때문에, 잘 확인하시길 바랍니다.
![Desktop View](/assets/img/2021-10-04/5.PNG){: width="90%" }

![Desktop View](/assets/img/2021-10-04/5-1.PNG){: width="90%" }
<br>
<br>

## 좌측 사이드 바의 컬러 변경
---
[jekyll-theme-chirpy Demo Page](https://chirpy.cotes.info/)에서 좌측에는 사이드바(sidebar)가 존재합니다. 프로필이미지, 소개글, 메뉴 등이 있는 좌측 부분을 말하지요.
![Desktop View](/assets/img/2021-10-04/6.PNG){: width="90%" }

해당 부분의 컬러는 light mode일때에는 베이지색, dark mode일 경우 검정에가까운 회색을 띕니다. 저는 우주컨셉이 좋아서, 색을 교체하기보다는 이 부분을 이미지로 넣고 싶었습니다. 이 부분이 도대체 어디에 있는지 어떻게 찾을까요?

요리조리 연결되어있는 부분을 소스로 찾아내어서 변경 할 수도 있습니다만, 그냥 직관적으로 찾고싶다면 브라우저의 **개발자 모드**를 이용해서 쉽게 찾을 수 있습니다. 개발자 모드는 현재 사용하시는 브라우저에서 `F12`버튼을 눌러 바로 띄울 수 있습니다.

사용중인 테마의 Demo페이지 말고, 본인의 깃헙블로그페이지로 들어간 뒤, F12버튼을 눌러 개발자 모드(DevTools)를 띄워줍니다.
아래와 같이 나오실텐데, 그 중 우측 상단 `>>`버튼을 눌러 Dock style을 변경 할 수 있습니다.

![Desktop View](/assets/img/2021-10-04/7.PNG){: width="90%" }

개발자 모드(DevTools) 중 상단에 요소(Elements)를 선택하시면 `<html>`태그로 시작되는 부분을 보실 수 있습니다. 각각의 요소에 마우스를 올리면 해당 태그가 어디부분을 구성하고 있는지 보실 수 있는데요. 마우스를 한줄 한줄 내려가면서 수정하고싶은 부분을 찾아봅니다. 

저는 `<body>`태그 안의 `<div id="sidear" ...`부분이 해당됩니다. 해당 부분을 더블 클릭하면 태그가 열립니다.
요소를 찾았다면, 그 태그를 클릭해보면 우측에 스타일(style)부분을 찾으실 수 있는데, 여기에서 보시면 `#sidebar{... background: var(--sidebar-bg); ...}`을 찾을 수 있습니다.
![Desktop View](/assets/img/2021-10-04/8.PNG){: width="90%" }

css파일에서 해당부분을 찾아야 하는데, #sidebar는 sidebar를 id로 가지는 요소의 css를 정의해 둔 것입니다. `background: var(--sidebar-bg);`를 그대로 복사하여서 VSCode에서 검색해보면, 아래와 같이 찾을 수 있습니다.
저는 이미 sidebar 배경색을 이미지로 변경하였기 때문에 저렇게 뜨는데, 더 많거나 혹은 다르게 보여질 수 있습니다.

![Desktop View](/assets/img/2021-10-04/9.PNG){: width="50%" }

해당 파일을 열어보면, background속성이 색깔이 아닌 `--sidebar-bg`라고 적혀있습니다. 색을 변수로 담아두었습니다. 다시한번 동일하게 --sidebar-bg를 검색해보시면, dark-typography.scss와 light-typography.scss에서 --sidebar-bg가 rgb로 설정되어 있는 것을 확인 할 수 있습니다.

컬러만 바꾸고싶으시다면 `dark-typography.scss`와 `light-typography.scss`에서 각각의 rgb색을 변경하여 입력해줍니다.

단순 컬러가 아닌 그라데이션을 사용하고 싶으시다면 [CSS Gradient](https://cssgradient.io/)과 같은 사이트를 참고하여 사용할 수 있습니다.

저는 컬러나 그라데이션 말고 이미지를 넣고 싶었기 때문에, dark-typography.scss와 light-typography.scss에 정의되어있는 --sidebar-bg부분을 지우고(주석처리하고) 아래와 같이 변경해주었습니다.
참고로 `/*___*/`형식으로 적어주시면 주석처리 됩니다.
```css
  /*background: var(--sidebar-bg);*/
  background-image: url('/assets/img/sidebar-bg-img.jpg'); /*사용하고 싶은 이미지 경로*/
  background-size: cover;  /*이미지의 size가 보여질 부분의 사이즈와 다른 경우에는 이미지 크기를 꽉차게 만든다 */
  background-repeat: no-repeat; /*이미지의 size가 보여질 부분의 사이즈와 다른 경우 이미지가 반복하여 나오는데, 반복하지 않겠다*/
```

<br>
<br>

## 모드별 하이라이트 컬러 변경
---
개발자 모드에서 변경이 필요한 요소를 찾고, VSCode에서 검색하여 수정하는 방법이 감이 잡혔다면 모드별 하이라이트 컬러를 변경하는것도 매우 쉽습니다!

페이지에 있는 글자들이 모두 검정색 글자는 아닙니다. 링크가 걸려있거나, 어떠한 구역 혹은 글자는 색깔을 가지고 있습니다. 그것이 바로 하이라이트 컬러입니다.

테마 고유의 색도 예쁘긴 합니다만, 저는 우주!컨셉이 좋아서, 색깔들을 보라색으로 변경하려고 합니다. light mode일때에는 그냥 그대로 두고, dark mode일 때 하이라이팅 컬러를 바꾸려고 해요. 

동일하게 본인의 깃헙블로그페이지로 들어간 뒤, F12버튼을 눌러 개발자 모드(DevTools)를 띄워줍니다. 하이라이트 컬러는 큰 요소가 아니기 때문에, sidebar부분을 찾는 것 처럼 하면 되게 오래 걸립니다.
그렇기 때문에 텍스트를 이용해서 검색하도록 하겠습니다.
저는 다크모드의 하이라이트 컬러를 바꿀거라 다크모드에서 개발자 모드로 진입했습니다.
화면에 보시면 "Getting Started", "Enable Google Page Views", "Customize the Favicon"과 같이 포스팅 제목에 색이 들어가 있습니다. 
![Desktop View](/assets/img/2021-10-04/10.PNG){: width="90%" }

해당 부분을 변경하려고 하기 때문에, 개발자 모드쪽에서 Ctrl+f를 눌러 포스팅 제목 중 하나를 검색합니다.
저는 `Getting Started`라고 검색하도록 하겠습니다.
검색하게 되면 해당부분의 요소가 맞는지 확인 후, style을 확인합니다.
![Desktop View](/assets/img/2021-10-04/11.png){: width="90%" }

```css
#search-results a, .post-content 
a:not(.img-link), .post-meta a, a{
    color: var(--link-color);
}
```

라고 확인되는데요, `color: var(--link-color);`를 VSCode에서 검색해봅시다.

![Desktop View](/assets/img/2021-10-04/12.PNG){: width="40%" }

확인은 되지만, sidebar부분과 같이 color가 rgb 등 색 지정이 되어있지 않고 변수로 지정되어 있습니다.
그렇기 때문에 다시 `--link-color`를 재검색 해봅니다. 그러면 아래와 같이 해당 변수명이 어떤 컬러인지 확인이 가능한데요, 저는 다크모드쪽만 변경할거라 다크모드쪽 link-color를 수정하여 저장합니다.

![Desktop View](/assets/img/2021-10-04/13.PNG){: width="40%" }

<br>
<br>

## local로 확인해보기
---
포스팅 작성과 마찬가지로, local에서 먼저 오류나 에러가 없는지, 원하는데로 수정이 잘 되었는지 등을 확인합니다.

Start Command Prompt with Ruby를 실행합니다.
![Desktop View](/assets/img/2021-09-28/2.PNG){: width="100%" } 
<br>

아래는 저의 경로로 예를 든것이며, 본인의 git Clone경로(폴더)로 이동합니다.
```
 cd C:\Users\wlqmf\Documents\GitHub\wlqmffl0102.github.io
```
<br>

Ruby Prompt에서 명령어를 입력
```
 bundle exec jekyll serve
```
<br>

정상적으로 확인된다면 <http://127.0.0.1:4000/> 또는 <http://localhost:4000/>으로 접속하여 변경사항들을 확인합니다.
<br>
<br>

## 깃헙에 업로드하기
---
정상적으로 로컬서버에서 확인이 된다면, 깃헙에 업로드 하여 본인의 실제 깃헙 블로그에 변경사항을 적용해야 합니다.

Github Desktop에서, 좌측 하단부에 commit 내용을 작성 후 commit to main이라는 버튼을 클릭한 뒤, Push origin버튼을 눌러주시면 됩니다.

![Desktop View](/assets/img/2021-09-28/5.PNG){: width="30%" } 
![Desktop View](/assets/img/2021-09-27/4.PNG){: width="90%" } 

5~10분 뒤 깃헙 블로그에 정상적으로 변경사항이 확인된다면 끝입니다!
<br>
<br>

## 마무리
---
블로그 커스텀에 관한 포스팅을 작성하였는데요, 사실 html이나 css 심지어는 javascript까지도 알아야 커스텀을 자유롭게 할 수 있습니다. 초보자들에게는 꽤 어려울 수도 있고, 주먹구구식으로 해야 할 수도 있습니다.
그래서 html이나 css등 여러가지 이야기를 풀어나가면 좋겠다는 생각이 드는데, 제 역량으로는 엄청나게 멋지고, 대단한 포스팅을 적을수는 없다고 생각합니다.
다만 제 바램은 초보자들도 쉽게 문턱을 넘어 자신만의 Github Blog를 만들었으면 하는 것 입니다.

포스팅은 계속 됩니다!