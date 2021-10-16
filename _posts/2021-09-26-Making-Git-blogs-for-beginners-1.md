---
title: 초보자를 위한 GitHub Blog 만들기 - 1
author: Dodev 하다
date: 2021-09-26 20:28:00 +0900
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

## 두서
---
가장 처음으로 작성하고자 마음먹은 것이 깃 블로그에 관한 것이였습니다.
개발을 전혀 모르시는 분이시라면 어렵고, 구조를 잘 몰라도 은근 헷갈립니다.
<br>

인터넷이 참 잘 되어 있어서 몇 번 검색만으로도 방대한 자료를 찾아 볼 수 있습니다.
그치만 제게 딱 맞는 글을 찾기란 어렵지요.
<br>

그래서 적어도 그냥 따라하기만 하면 깃블로그를 만들 수 있는 포스팅을 적고 싶었습니다.
그런 고로, 시작하겠습니다.
**해당 포스팅은 Window, 64bit 기준으로 작성되었습니다**
<br>
<br>

## Step 0. Github Blog(깃허브 블로그)란?
---
**Github** 라고 불리는 웹 페이지가 있습니다. 
Github는 **Git**을 호스팅해주는 웹 페이지를 말합니다. 그렇다면 Git은 무엇이냐, 보통 "형상관리 툴"이라고 이야기 합니다.
<br>

간단하게 이야기 하자면, 
프로그램은 엄청나게 많은 코드를 포함합니다. 그 코드는 혼자서 작성하는것이 아니지요. 여러 사람과 협업을 하며 코드를 수정하고, 추가하고, 삭제하며 프로그램은 만들어집니다.
그런데 만약, 그 기록을 남겨놓지 않는다면? 추후에 문제가 발생하여도 빠른 대응이 어려울 것입니다.
그래서 누가, 언제, 무슨코드를 어떻게 했느냐 하는 기록을 남기는(흔히 형상관리라고 합니다.) 도구를 "Git"이라고 부르고,
그것을 웹페이지에서 볼 수 있도록 도와주는 서비스 중 하나가 "Github"입니다.
참고로, Github이외에도 여러가지 서비스가 존재합니다. ex) GitHub, GitLab, BitBucket
<br>

자 그렇다면 **Github Blog**는 무엇인가?
Github에는 여러가지 파일이 업로드,저장이 이루어집니다. 그 중, 저장된 html파일 같은 웹 문서들을 Github에서 무료로 호스팅을 제공해주는 서비스가 존재합니다. 바로 [**Github Page**](https://pages.github.com, "github-page")입니다.
이 Github Page를 이용하여 Blog를 만든것이 Github Blog(깃허브 블로그, 깃블로그)입니다.

그렇기 때문에, 깃 블로그를 만들기 위해서는 Github 계정이 필요합니다.
Github 계정이 없으신 분들은 [**Github**](https://github.com/, "github")으로 접속하여 계정생성(회원가입)을 먼저 진행해주시길 바랍니다.
계정 생성은 어렵지 않기 때문에, 생략하도록 하겠습니다. 추후 필요시 내용 추가 하도록 하겠습니다.
<br>
<br>

## Step 1. Github Page 생성
---
### Step 1-1. 우선 본인의 Github계정(https://github.com/{username})으로 접속 후, 새로운 repository를 생성합니다.
---
![Desktop View](/assets/img/2021-09-27/1.PNG){: width="90%" }
 <br>
<br>

### Step 1-2. repository생성
---
Github Page는 `사용자 페이지(단 1개)` 와 `프로젝트 페이지(여러개 가능)` 으로 구성됩니다. 		
<br>

`사용자 페이지`는 https://username.github.io 와 같은 주소형식을 가집니다.
`프로젝트 페이지`는 https://username.github.io/project_name 과 같은 주소 형식을 가집니다.

위 두 가지는 비슷해 보이더라도, 차이가 아주 큽니다.

저희는 사용자 페이지 주소형식을 사용할것입니다!
고로 **Owner는 변경하지 마시고, Repository name항목은 "username.github.io"를 입력합니다.**
<br>

저는 username이 wlqmffl0102이기 때문에
Owner는 wlqmffl0102 / Repository name은 wlqmffl0102.github.io 으로 작성합니다.
<br>

이후 선택지는 Public, Add a README file만 체크 후 나머지는 그대로 두시고 Create repository를 클릭합니다.
![Desktop View](/assets/img/2021-09-27/2.PNG){: width="90%" }
<br>
<br>

### Step 1-3. GitHub Page생성
---
생성한 리포지토리로 이동 한 뒤, 상단 Settings를 클릭합니다.
Settings 좌측 하단부에서 Page설정을 찾을 수 있습니다.
![Desktop View](/assets/img/2021-09-27/add1.PNG){: width="90%" }
<br>

Source항목을 아래 사진과 동일하게 맞춰주신 후 Save버튼을 누르면
상단의 Your site is published at...이라는 초록색 부분을 볼 수 있습니다.
![Desktop View](/assets/img/2021-09-27/add2.PNG){: width="90%" }
<br>

해당 주소가 바로 GitHub Page입니다!
접속이 되지 않는다면 5~10분정도 기다린 후 접속해보시면 접속이 될 것입니다.
<br>

이 주소가 본인의 깃헙블로그 주소가 될 것입니다!
사진과 같이 <https://wlqmffl0102.github.io/>로 보여지지 않고,
<https://wlqmffl0102.github.io/(Projectname)>으로 보여진다면,
사용자이름과 리포지토리명이 달라서 그렇습니다. 사용자 페이지가 아닌 프로젝트 페이지가 생성 된 것입니다. [Step 1-2. repository생성](#step-1-2-repository생성)에서 다시 확인하시길 바랍니다.
<br>
<br>

### Step 1-4. [**Github Desktop**](https://desktop.github.com/, "github-desktop")과 [**VSCode**](https://code.visualstudio.com/, "vscode") 설치
---
Github Desktop과 VSCode를 설치합니다.
<br>

사실 Github는 "Git을 다루는 능력" 또한 중요합니다. Git은 여러가지 명령어가 있고, 구조가 존재합니다. Github Page를 만들고는 싶은데, Git을 잘 사용할 줄 모르시는 분이시라면, commend line을 이용하기 보다는 Github Desktop을 추천해드립니다. 초보자도 쉽게 조작이 가능하기 때문이지요!
<br>

그리고 VSCode란, Visual Studio Code의 약자로, MS사가 개발한 소스 코드 편집기 입니다.
네. 각종 파일들을 편집하기 쉽도록 해주는 툴이지요.
<br>

자, 이제 Github Desktop과 VSCode 설치를 완료했다면, 원격지에 있는 Github repository를 로컬과 Clone해줄것입니다!
무슨 말이냐 하면, 인터넷 웹페이지에 어떠한 저장공간을 만들었어요(Repository). 그 저장공간에 있는 파일을 로컬(본인의 PC)로 가져오는것입니다!
아직 잘 이해가 안 되실 수 있지만 시작해보겠습니다.
<br>

우선, Github Desktop을 실행하여 Sign in to GitHub.com 버튼을 클릭 후, GitHub에 가입한 계정명(유저이름), 이메일을 작성 후 Continue -> Finish버튼을 순서대로 눌러줍니다.
<br>

로그인이 정상적으로 되었다면, 이전 단계에서 생성한 "username.github.io" Repository가 화면에 보이실겁니다. 선택 후 하단 Clone.. 버튼을 클릭하여 진행하시면됩니다.
이때, 보여지는 "Local path"라는 항목이 보이실건데요, 해당 경로의 폴더가 인터넷에 있는 repository와 연동되는 것 입니다.
<br>

로그인이 정상적으로 되지 않으셨다면, 좌측상단의 File -> Options -> Accounts -> GitHub.com에서 Sign in버튼을 눌러 로그인을 진행가능합니다.
<br>

또, Clone할 리포지토리가 제대로 보여지지 않거나 선택을 하지 못하였을 경우, 좌측상단의 File -> Clone a repository -> GitHub.com -> Your repositories에서 해당하는 repository 를 선택 후, 클론 해주시면 됩니다.
<br>
<br>

### Step 1-5. Github Desktop과 VSCode를 이용 해 보기
---
자, 다 되어 갑니다!
정상적으로 Github Desktop을 설치 후, repository clone을 하였다면, 아래와 같은 이미지를 확인 할 수 있습니다.
여기서 Current repository에 "username.github.io"로 보이는지, Current branch에 "main"으로 보이는지 확인 후, 맞다면 Open the repository in your external editor항목의 Open in Visual Studio Code버튼을 누릅니다.
![Desktop View](/assets/img/2021-09-27/3.PNG){: width="90%" }
<br>

그렇다면  Github Desktop이 실행 중인 채로 쨘 하고 VSCode가 실행되어 보이실텐데 Github Desktop은 그대로 두시고, VSCode의 좌측 탐색기 부분을 잘 봅시다.
아마 "열려 있는 편집기"와 "username.github.io"가 보이실거예요.
아무것도 파일을 작성한 것이 없어서, 아무런 파일이 보이지 않아야 정상이지만, 사실 저희가 repository를 만들때 하나의 파일을 생성했어요! 바로 "README.md"입니다! 
잘 확인 되신다면 순조로워요~~
<br>

자, 이제 여기에 홈페이지에 띄울 파일을 하나 작성해보도록 할게요.
"username.github.io"에 마우스를 올리시면 파일을 추가 할 수 있습니다.
index.html이라는 이름의 파일을 하나 생성해주시고, 내용은
```html
<html>
	<body>
		Hello! This is the first page!
	</body>
</html>
```
으로 작성 후 저장해주세요!
<br>

그런 다음에, Github Desktop을 다시 열어 보시면, 좌측에 changes에 index.html파일이 보이고, 하단에는 Commit to main이라는 버튼이 활성화 되어 보일겁니다.
그대로 버튼을 눌러주시면 아래와 같이 확인이 가능할것입니다!
Push origin버튼을 눌러주시면, 완료된겁니다. 
![Desktop View](/assets/img/2021-09-27/4.PNG){: width="90%" }
<br>
<br>

### (보너스) Github Desktop 사용방법
---
Girhub Desktop의 사용법은 위와 같이 동일합니다.
1. 좌측 상단 'Current repository'가 현재 사용하려고 하는 repository와 같은 이름인지 확인

2. 바로 옆 'Current branch'또한 (대개)main이 맞는지 확인합니다.(브런치가 다르다면 브런치를 확인합니다!)

3. 좌측부분에서 file들의 변경사항이 있다면 추가(초록), 수정(노랑), 삭제(빨강)로 확인이 가능합니다.

4. file변경사항을 원격지 repository로 올리고 싶을때에는 수정사항이 올바른지 확인 후, 좌측 하단 Summary에서 Commit message를를 적은 뒤 'Commit to main'버튼을 누릅니다.(브런치가 다르다면 Commit to (브런치명)으로 확인됩니다.)

5. Commit이 완료되었다면 화면 가운데 혹은 화면 상단에서 Push origin버튼을 눌러줍니다.

6. 5~10분 뒤 github page로 생성된 주소로 들어가서 확인합니다.

<br>
<br>

### Step 1-6. Push확인 및 index.html접속해보기
---
Github Desktop에서 push 후, Github홈페이지 -> "username.github.io" repository로 들어가 보시면,
화면에는 README.md파일과, index.html파일이 확인된다면 정상적으로 Push가 완료된 것입니다.
<br>

자, 이제 확인해봅시다.
웹 브라우저 주소창에 http://username.github.io 를 기입하여 접속 해봅시다.
화면에 "Hello! This is the first page!"라고 보인다면 완료되신것입니다.
페이지가 정상적으로 보이지 않는다면 5~10분 후 재접속 해보시길 바랍니다.
<br>
<br>

## 마무리
---
어떠셨나요? 너무 어렵지는 않으셨으면 합니다.
사담이 너무 많이 끼여서~ 게시글이 너무 길어진것 같아요! 정보전달을 더 깔끔하게 할 수 있도록 노력해보겠습니다.
아직 재미있는 것들이 잔뜩 남았는데, 한 페이지로 다 보여드리지 못해서 죄송합니다.
그치만 꾸준히 작성하겠습니다. 부디 도움이 되었으면 합니다.
<br>

처음에도 말씀드렸지만 아직 미흡한 부분이 많습니다.
미흡한 부분은 지적해주시고, 에러가 난다면 함께 고민 할 수 있으면 합니다.
다들 끝까지 봐주셨으면 하는 바램이 있습니다. 그러니까 저도 끝까지 게시글을 쓰려고 합니다.
<br>

포스팅은 계속됩니다. 감사합니다!
<br>
<br>

## 다음 포스팅
---
[초보자를 위한 GitHub Blog 만들기 - 1](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-1/)

[초보자를 위한 GitHub Blog 만들기 - 2](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-2/)

[초보자를 위한 GitHub Blog 만들기 - 3](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-3/)

[초보자를 위한 GitHub Blog 만들기 - 4](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-4/)
