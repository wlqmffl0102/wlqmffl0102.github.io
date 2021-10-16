---
title: 초보자를 위한 GitHub Blog 만들기 - 2
author: Dodev 하다
date: 2021-09-27 20:28:00 +0900
categories: [GitHub Blog]
tags: [GitHub Blog, How to, Study]
---

## 초보자를 위한 GitHub Blog 만들기 시리즈
---
[초보자를 위한 GitHub Blog 만들기 - 1](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-1/)

[초보자를 위한 GitHub Blog 만들기 - 2](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-2/)

[초보자를 위한 GitHub Blog 만들기 - 3](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-3/)

[초보자를 위한 GitHub Blog 만들기 - 4](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-4/)
<br>
<br>

## Step 2.  Jekyll과 Ruby 설치
---
### Step 2-1. Jekyll Theme선택
---
나만의 깃헙 페이지 주소가 생성되었다면, 드디어 그 페이지를 블로그처럼 꾸미는 일을 시작해보겠습니다.
<br>

Github 블로그는 Github Page, Jekyll(지킬), Ruby(루비)가 필수입니다! 셋 중 하나는 완료했고, 나머지는 쉽게 설치가 가능합니다.
<br>

Jekyll과 ruby를 다운로드 하기 전, 마음에 드는 테마를 고르려고 합니다.
-   [http://jekyllthemes.org/](http://jekyllthemes.org/)
-   [https://jekyllthemes.io/free](https://jekyllthemes.io/free)
-   [http://themes.jekyllrc.org/](http://themes.jekyllrc.org/)
-   [https://github.com/topics/jekyll-theme](https://github.com/topics/jekyll-theme)

과 같이 다양한 Jekyll Themes를 지원하는 페이지가 있습니다.
구글 등에 검색하시면 훨씬 많이 나오니, 찬찬히 선택 하시길 바랍니다.
<br>

저는 처음에는 [Type-on-Strap 테마](https://sylhare.github.io/Type-on-Strap/)를 선택하여 다양한 커스텀을 거쳐 사용하다, 불편한 점이 많다고 생각해서 블로그를 다시 만들었습니다.
선택에 여러가지 경우가 많겠지만, 결론적으로 저는 [jekyll-theme-chirpy](https://chirpy.cotes.info/) 테마를 선택했습니다!
<br>

현재 여러분이 보고 계신 제 블로그는 jekyll-theme-chirpy를 사용한 블로그입니다.
제가 필요한 여러가지 기능들이 구현이 되어있고 몇가지만 커스터마이징 후 사용가능하다고 생각되어서 선택하였는데, 다른 테마들과는 조금 다른점이 있더라구요.
그렇지만 어떠한 테마를 사용하여도 큰 틀은 동일합니다! 하지만 디테일은 모두 다르다는 점! 
<br>
<br>

### Step 2-2. Ruby 설치
---
Ruby. 예쁜 이름입니다! 루비는 프로그래밍 언어명입니다. Jekyll이 Ruby로 만들어져 있어서 Jekyll설치 전, 먼저 설치하도록 하겠습니다.
<br>

[Ruby 공식사이트](https://rubyinstaller.org/downloads/)로 접속 후, 아래와 같이 `Ruby+Devkit 2.6.8-1 (x64)`를 선택하여 다운로드 합니다.
이후 다운받은 설치파일을 실행 후, 별 다른 수정 없이 Next만 눌러 디폴트로 설치합니다.
![Desktop View](/assets/img/2021-09-28/1.PNG){: width="90%" } 
<br>

설치 완료 후, 좌측 하단 윈도우 검색창에 "ruby"라고 검색하여 `Start Command Prompt with Ruby`를 실행합니다.
![Desktop View](/assets/img/2021-09-28/2.PNG){: width="100%" } 
<br>

검은색의 명령어창(Prompt)가 열릴것입니다. 여기서 명령어를 사용하려고 합니다. 사용하시는 컴퓨터의 파일명, 경로 등이 모두 영어로 되어있다면 괜찮지만, 대게 한글도 섞여 있을 것입니다. 그렇기 때문에 경로 이동 후 인코딩을 먼저 진행하겠습니다.
<br>

우선, Clone 진행 시 지정했던 위치로 이동합니다.
Clone 위치는 모두 다릅니다. 위치를 알 수 없다면 열려있는 VSCode 좌측 README.md파일을 우클릭 후 "파일 탐색기에 표시"버튼을 누르면 폴더창이 열립니다.
해당 폴더가 바로 Clone했던 local위치입니다.
<br>

아래는 저의 경로로 예를 든것이며, 본인의 git Clone경로(폴더)로 이동합니다.
```
 cd C:\Users\wlqmf\Documents\GitHub\wlqmffl0102.github.io
```
<br>
이동한 뒤, 인코딩을 합니다. 
```
 chcp 65001
```
명령어 입력 후 "Active code page: 650001"이라는 글자가 확인된다면 정상입니다.
<br>
<br>

### Step 2-3. Jekyll 설치
---
jekyll 및 bundle설치 : 두 개의 명령어를 순서대로 입력합니다. 
```
 gem install jekyll bundler
 
 gem install webrick
```
<br>

jekyll생성
```
 jekyll new ./
```
<br>

bundle install
```
 bundle install
```
jekyll 서버 동작
```
 bundle exec jekyll serve
```
<br>

에러가 없이 정상적으로 모두 실행되었다면 웹 브라우저 주소창에 <http://127.0.0.1:4000/> 또는 <http://localhost:4000/>로 접속. 
<br>

"https://wlqmffl0102.github.io/"와 동일한 화면. 즉 화면에 “Hello! This is the first page!”가 나온다면 정상입니다!
<br>
<br>

## Step 3.  Jekyll Theme(지킬 테마) 적용하기
---
### Step 3-1. 테마 다운로드하기
---
드디어 아까 전에 블로그에 테마를 적용하려고 합니다!
지킬과 루비를 다운로드 받기 전, 마음에 드는 테마를 고르셨을텐데요, 아마 데모페이지를 보셨을것입니다.
데모 페이지를 그대로 다운로드 해서 제 블로그에 올려서 확인해보려고 해요.
<br>

어떤 데모이든, "Download" 혹은 "GitHub" 링크가 존재할것입니다. 데모페이지에서 바로 다운받으셔도 상관없습니다.
GitHub 링크만 존재하는 경우, 해당 Github페이지로 이동합니다. 제 경우에는 <https://github.com/cotes2020> 으로 접속합니다.
![Desktop View](/assets/img/2021-09-28/3.PNG){: width="90%" } 
<br>

접속하시면 Repository 이름에 본인이 선택한 테마이름의 Repository가 보이실것입니다. 해당 Repository로 들어가셔서 소스를 다운로드 합니다.
![Desktop View](/assets/img/2021-09-28/4.PNG){: width="90%" } 
<br>

압축파일을 풀고, 폴더 안의 모든 내용을 복사하여, Clone한 local 폴더 안에 붙여넣어줍니다.
파일이 존재한다는 메시지가 뜬다면 덮어쓰기를 진행합니다.
여기서, Clone한 local폴더는 저의 경우 C:\Users\wlqmf\Documents\GitHub\wlqmffl0102.github.io입니다. 모두 다릅니다. 본인의 경로로 들어가서 붙여넣기 하셔야 합니다!
<br>
<br>

### Step 3-2. 테마 적용 로컬 확인
---
Ruby Prompt에서 명령어를 입력
```
 bundle install
```
<br>

지킬 로컬서버 실행
```
bundle exec jekyll serve
```
<br>

정상적으로 명령어 입력 후, <http://127.0.0.1:4000/> 또는 <http://localhost:4000/>으로 접속하시면 Demo화면과 동일하게 보이실것입니다!

와~~ 드디어! 하고 생각하실 수 있지만, 이것은 로컬 확인입니다.
Github page로 생성한 제 홈페이지는 여전히 "Hello! This is the first page!"로만 보여집니다.
<br>
<br>

### Step 3-3. Github로 Push
---
자, 여기에서 설명을 조금 하겠습니다.
Github Page란 설정된 Github Repository에 있는 정적 파일을 이용해서 페이지를 보여주는것입니다.
로컬(Local)이란, 지금 본인이 사용중인 컴퓨터... PC, 노트북 따위를 말합니다.
<br>

조금 전, 저희는 인터넷에서 마음에 드는 테마 소스를 다운로드받아서 local에 있는 폴더 안으로 붙여넣기를 했습니다.
즉, local에는 파일이 엄청나게 많아 졌지만, Github Repository에는 어떠한 파일을 작성, 수정, 삭제 하지 않았습니다.
그래서 local에 있는 여러가지 파일을 Github Repository로 전송해야합니다.
<br>

그렇다면 어떻게 하느냐, 여러가지 방법이 있지만 저희는 쉬운 Github Desktop을 설치했습니다!
Github Desktop은 원격지에 있는 Github Repository와 local 폴더 안에 있는 파일들을 대조하고, 달라진것이 있다면 자동으로 push(local -> repository)하거나, pull( repository -> local)를 할 수 있도록 쉽게 도와줍니다.
<br>

Github Desktop을 열어보시면, 좌측에 local에 붙여넣었던 파일명이 쭉 뜰것입니다.
Github Desktop이 원격지 Repository와 local사이에서, 어떤파일이 추가,수정,삭제됬는지 확인을 해주는 것입니다!
<br>

좌측 하단부에 이전과 같이 commit to main이라는 버튼이 있을텐데, 활성화 되어 있지 않을 것 입니다. 파일이 여러개라서 commit 내용을 직접 적어줘야 합니다.
대충 아무내용을 적으신 다음, commit to main이라는 버튼을 클릭한 뒤, Push origin버튼을 눌러주시면 됩니다.
![Desktop View](/assets/img/2021-09-28/5.PNG){: width="50%" } 
<br>

5~10분 뒤, 본인의 Github Page 주소 즉, 저에게는 https://wlqmffl0102.github.io/ 으로 접속하여 정상적으로 페이지가 보인다면 끝입니다!
<br>
<br>

## 마무리
---
깃 블로그 만들기 포스팅은 계속됩니다!

## 다음 포스팅
---
[초보자를 위한 GitHub Blog 만들기 - 1](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-1/)

[초보자를 위한 GitHub Blog 만들기 - 2](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-2/)

[초보자를 위한 GitHub Blog 만들기 - 3](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-3/)

[초보자를 위한 GitHub Blog 만들기 - 4](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-4/)
