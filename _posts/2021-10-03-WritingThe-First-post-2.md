---
title: 첫 포스팅 작성하기
author: Dodev 하다
date: 2021-10-03 20:10:00 GMT+0900
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

## 이전 포스팅
[첫 포스팅 작성하기 - 마크다운(Markdown)](https://wlqmffl0102.github.io/posts/WritingThe-First-post-1-Markdown-Grammar1/)
<br>
<br>

## 첫 포스팅 작성하기
---
이전 포스팅에서 이야기 하였듯, 네이버나 티스토리 등 여러 플랫폼의 블로그와는 글쓰기 방법이 조금 다릅니다.
특정 위치에 md(markdown)파일을 생성하면, 깃헙에서 해당 md파일을 이용해 html페이지로 변환해줍니다.
그렇게 포스팅이 작성되어 갑니다.

그렇기 때문에 이전 포스팅에서 markdown 문서 작성방법에 관해 포스팅을 진행했습니다.

자, 이제는 포스트를 게시할것인데요, 일반적으로 지킬의 구조는 아래와 같습니다.
```
    .
    ├── _config.yml
    ├── _data
    │   └── members.yml
    ├── _drafts
    │   ├── begin-with-the-crazy-ideas.md
    │   └── on-simplicity-in-technology.md
    ├── _includes
    │   ├── footer.html
    │   └── header.html
    ├── _layouts
    │   ├── default.html
    │   └── post.html
    ├── _posts
    │   ├── 2007-10-29-why-every-programmer-should-play-nethack.md
    │   └── 2009-04-26-barcamp-boston-4-roundup.md
    ├── _sass
    │   ├── _base.scss
    │   └── _layout.scss
    ├── _site
    ├── .jekyll-metadata
    └── index.html # 올바른 머리말을 가진 'index.md' 도 가능
```

여기에서 눈 여겨 보아야 하는 부분은 `_posts`입니다. 말 그대로 포스트가 올라가는 공간입니다.
지킬테마를 사용하는 모든 깃헙 페이지에는 _posts라는 폴더가 있습니다. 그곳에 md파일을 생성 하는 것이 포스팅의 시작입니다.

_posts폴더 안에, 디폴트로 여러가지 문서가 있을 수 있습니다.
_posts폴더 안의 md파일의 이름은 **YYYY-MM-DD-TITLE.md**와 같은 형식을 가집니다. 

그렇다면 파일을 하나 생성해볼까요? 필자의 현재일자,일시를 기준으로 `2021-10-03-WritingThe-First-post-2.md`파일을 하나 만듭니다.
새 파일이기 때문에 안에는 어떠한 내용도 들어있지 않습니다.

해당 md파일이 블로그의 "포스트"임을 알리기 위한 내용이 처음으로 들어가야 합니다.
바로  YAML타입 머리글 인데요, 기본적으로 아래와 같이 쓰이며, 여러가지 옵션들이 있습니다.

```yaml
---
layout: post
title: 첫 포스팅 작성하기
---
```

제가 사용하는 테마는 jekyll-theme-chirpy테마는 기본적으로 아래와 같은 포맷을 사용한다고 나와있기에, 해당 가이드 라인에 따라 작성하고 있습니다. 테마마다 옵션들이 다르기 때문에, 테마의 제작자 Repository에 방문하거나 디폴트 문서 중 나와있는 가이드라인을 참고하시면 됩니다. 가장 맨 처음에 해당 내용을 기입 후, 그 아래에 포스팅 내용을 작성하시면 됩니다.
```yaml
---
title: TITLE
date: YYYY-MM-DD HH:MM:SS +/-TTTT
categories: [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [TAG]     # TAG names should always be lowercase
---
```

참, date항목에  "YYYY-MM-DD HH:MM:SS +/-TTTT"으로 나와있는데, 이중 `+/-TTTT`이라는게 붙어 있습니다. 타임존 오프셋이라고 하는데, 별 것 없다. 대한민국은 보통 +09:00으로 작성합니다. 더 알고 싶다면 [이 블로그 포스팅](https://ratseno.tistory.com/11)에서 자세하게 알아 볼 수 있습니다.
<br>
<br>

## 마크다운 문서 편집기(Markdown Editor)
---
본격적으로 markdown언어를 이용하여 게시글을 작성하려고 하나, 아직 막막하신 분들이 많으실겁니다.
그래서 여러가지 에디터를 소개하고자 합니다.

1. [Typora](https://typora.io/)  :
    마크다운 에디터를 처음 접하게 된 프로그램입니다. 설치형이고, 깔끔하고 많은 사람들이 편하게 사용하고 있습니다.
    그렇지만 저는 설치형보다 웹형의 에디터가 조금 더 편해서, Typora는 초반에 잠깐 사용하였습니다.

2. [StackEdit](https://stackedit.io/app#) :
    Typora 다음으로 접하게 된 스택 에딧입니다. 웹 형이고, 보통 저는 스택에딧을 참고하곤 합니다.

3. [DILLINGER](https://dillinger.io/)

이정도 소개하도록 하겠습니다. 이외에도 엄청나게 많은 에디터 및 마크다운 문서 변환 프로그램/사이트가 존재합니다.
찾아보시다가 편하신 것을 선택해서 사용하시면 될 것 같습니다.
다만, 유의해야 하는점은 Markdown은 표준이 없기 때문에 에디터에서 작성한 모습 그대로 블로그에 표현되지 않을 가능성도 존재합니다. 꼭 유의하시길 바랍니다.
<br>
<br>

## local로 확인해보기
---
포스팅을 작성하였다면 생각했던데로 포스팅이 잘 나오는지, 문제가 되는점은 없는지 등 확인을 해야 합니다.
확인하지 않고 그대로 깃헙에 커밋, 푸시를 하게 되면 어떤 문제가 발생하는지 알 수 없고, 커밋, 푸시 후 또 수정, 다시 커밋, 수정 ... 귀찮습니다! 그래서 우선 로컬로 띄워보겠습니다. 어렵지는 않고, 이전에도 해봤던 과정이기 때문에 크게 문제될 것 없습니다.

`Start Command Prompt with Ruby`를 실행합니다.
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

정상적으로 확인된다면 <http://127.0.0.1:4000/> 또는 <http://localhost:4000/>으로 접속하여 포스팅에 문제가 없는지 확인합니다.

jekyll-theme-chirpy기준으로, 포스팅 파일 제목이 한글로 작성 된 경우, local에서 home화면에서는 게시글 목록이 확인되나, 해당 게시글을 보려고 하면 404에러가 떨어집니다. 인코딩과정을 거쳐 md파일에 한글이 있는 경우에도 정상적으로 작동할 수 있도록 하는 방법은 분명히 있을겁니다. 저는 귀찮아서 그냥 md파일 이름을 모두 영어로 작성하였습니다.

포스팅확인이 정상적으로 된다! 내가 생각했던데로 나온다! 하시면 커밋, 푸시를 하시고, 생각했던데로 나오지 않는 점들을 하나씩 수정하여 정상적인 포스팅으로 수정작업을 진행해줍니다.

포스팅의 내용만 변경 할 경우에는 local jekyll 서버를 재시작 하지 않아도 괜찮습니다만, _config,yml 등의 설정파일을 변경하는 경우에는 local jekyll 서버를 꼭 재시작해주셔야 합니다.
local jekyll server가 실행중인 Ruby Prompt에서 `Ctrl+C`를 눌러 서버를 중지했다가, 다시 `bundle exec jekyll serve`명령어를 입력하여 재시작 가능합니다.

참고로 `bundle exec jekyll serve`명령어를 나눠서 사용도 가능합니다.

local server에서 _site파일 생성 (사이트 구축)
```
 jekyll build
```
<br>

소스 파일이 변경될 때마다 사이트를 빌드하고 로컬에서 제공
```
 jekyll serve
```


<br>
<br>

## 깃헙에 업로드하기
---
정상적으로 로컬서버에서 확인이 된다면, 깃헙에 업로드 하여 본인의 실제 깃헙 블로그에 포스팅을 업로드해야 합니다.

Github Desktop에서, 좌측 하단부에 commit 내용을 작성 후 commit to main이라는 버튼을 클릭한 뒤, Push origin버튼을 눌러주시면 됩니다.

![Desktop View](/assets/img/2021-09-28/5.PNG){: width="30%" } 
![Desktop View](/assets/img/2021-09-27/4.PNG){: width="90%" } 

5~10분 뒤 깃헙 블로그에 정상적으로 포스팅이 보인다면 끝입니다!