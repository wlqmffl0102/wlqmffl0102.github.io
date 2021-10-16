---
title: Git 용어 정리
author: Dodev 하다
date: 2021-09-28 15:40:00 +0900
categories: [Git]
tags: [Git, Study]
---


## Git
---
여담으로 끼워넣겠습니다. 전혀 모르고 하다보면 어느순간 이해하게 됩니다만, 그렇지만 간단한것은 한번씩 짚고 넘어가려고 합니다.
깃 블로그 만들기에는 꼭 필요한 내용은 아닙니다. 넘어가셔도 무관합니다.
<br>

Github 사용법은 몸에 익숙해지면 여러가지 편리함으로 업무에 효율을 높여줍니다.
그렇지만 사용법을 잘 알지 못하면 사용법을 익히기 전까지는 조금 귀찮을 수 있습니다.
<br>

어떤 가게에서 물건을 살 때, 그냥 현금을 주고 사면 복잡할 것이 없습니다. 체크카드를 사용하면 더 편하게, 더 여러가지 일들을 할 수 있습니다. 그렇지만 체크카드를 사용하기 위해서는 은행에서 계좌를 개설하고, 계좌에 돈을 넣은 다음에 정해진 만큼의 돈 만 사용 할 수 있죠. 어플을 사용하지 않는다면, 체크카드 혹은 계좌에 돈이 얼마나 남아있는지 확인하기 위해서는 은행이나, ATM기까지 가야 합니다.
<br>

모든 일들은 저렇다고 생각합니다. 사용에 익숙해지면 편리한점들만 보이는데, 첫 사용이라면 궁금증도, 불편함도 있다고 생각합니다. 그래서 어렵게 이야기 하기보단 조금씩 접근성을 늘려갔으면 합니다!
<br>

여담은 그만하고, 이번에는 여태까지 나온 Repository, Clone, Commit, Push, Pull에 관해 이야기 하려고 합니다.
<br>
<br>

## Github
---
Github는 `Git을 호스팅해주는 웹 페이지`를 말합니다. 그렇다면 Git은 무엇이냐, 보통 "형상관리 툴"이라고 이야기 합니다.
즉, Github와 Git은 엄연히 다른것 입니다. Git은 tool이고, Github는 Service입니다.
<br>

간단하게 이야기 하자면, 
프로그램은 엄청나게 많은 코드를 포함합니다. 그 코드는 혼자서 작성하는것이 아니지요. 여러 사람과 협업을 하며 코드를 수정하고, 추가하고, 삭제하며 프로그램은 만들어집니다.
그런데 만약, 그 기록을 남겨놓지 않는다면? 추후에 문제가 발생하여도 빠른 대응이 어려울 것입니다.
그래서 누가, 언제, 무슨코드를 어떻게 했느냐 하는 기록을 남기는(흔히 형상관리라고 하지요.) 도구를 "Git"이라고 부르고,
그것을 웹페이지에서 볼 수 있도록 도와주는 녀석이 "Github"입니다.

참고로, Github이외에도 여러가지 서비스가 존재합니다. ex) GitHub, GitLab, BitBucket

## Repository
---
말 그대로 '저장소'입니다. 파일이나 폴더를 저장해 두는 곳입니다. 
 - Local Repository : Local. 즉 현재 사용하는 PC, 노트북 등의 장치에 존재하는 저장소입니다. 
	PC에서 어떤 프로그램을 다운로드 받게 되면 하드디스크의 용량을 차지하게 됩니다.
	물론 폴더도 그렇습니다. 폴더 안에 사진들만 저장해 둔다면 "사진첩", 동영상만 저장해둔다면 "동영상"이라고 폴더 이름을 적어 나눠 둘 것 같습니다. 
	사진이나, 동영상이 아니라 어떠한 프로젝트를 위한 폴더를 만들고, 그곳에 관련 파일들을 저장해둔다면, 그 폴더 이름은 "xx project" 등과 같을 수 있습니다. 이때, xx project라고 불리는 폴더가 Local Repository입니다.
   
 - Remote Repository : Local에 위치하지 않는 저장소입니다. 간단히 말하자면 현재 PC 등에서 파일을 저장하는 폴더 등은 Local 저장소이고, 본인이 PC에 직접 가지고 있지 않고, 다른 곳에 저장되어있는 각종 파일과 폴더 등은 원격지(Remote) 저장소(Repository)에 저장되어 있다라고 생각하시면 될 것 같습니다.
  저희는 Github(웹 사이트)에 Repository를 만들었지요. 그것이 바로 Remote 저장소(줄여서 원격지)라고 생각하시면 될 것 같습니다.
<br>
<br>

## Clone / Fork
---
우선 `Clone`부터 확인하겠습니다. Clone또한, 말 그대로 복제입니다.
원격지에 저장되어 있는 모든 데이터를 로컬로 복사해오는 기능입니다. 
![Desktop View](/assets/img/2021-09-29/0.PNG){: width="90%" } 

원격지(Github)로부터 데이터를 Local로 Clone해 오는 방법은 여러가지 입니다.
- 명령 프롬프트(cmd)를 이용하는 방법
- git bash를 이용하는 방법
- Github Desktop을 이용하는 방법
- 원격지 데이터를 .zip파일로 다운로드 받아 Local에 압축을 해제하는 방법
등 여러가지 방법이 있습니다.

Clone이 진행된다면, local Repository와 Remote Repository가 연결됩니다.
![Desktop View](/assets/img/2021-09-29/4.PNG){: width="90%" }

그 중, 제 포스팅은 [Github Desktop](https://desktop.github.com/, "Github-Desktop")을 이용하고 있는데요. 초보자들이 사용하기 가장 좋은 방법이라고 생각합니다. UI지원으로 명령어를 직접 사용하지 않고, 버튼만 몇가지 눌러 git을 사용할 수 있습니다.

[Github Bash](https://git-scm.com/, "Github-Bash")는 OS에 상관없이 리눅스체제의 명령어를 입력하여 사용 할 수 있습니다. Windows와 Linux 그리고 mac은 사용하는 명령어가 모두 다릅니다. windows는 cmd(명령 프롬프트), Linux와 mac은 terminal을 사용합니다. windows에서 Linux명령어를 사용 할 수 있어서, git과 linux명령어를 함께 배우고싶거나, 모두 사용할 줄 아신다면 git bash는 매우 유용합니다.
<br>
<br>

다음으로 `Fork`입니다.
fork는 본인의 Repository가 아닌, **다른사람의 Repository를 본인의 Repository로 복제하는것**입니다. 

제 블로그에서는 아직까지 fork에 관해 다루지 않았습니다. 

fork하게 되면 fork한 다른 사람의 Repository와 연결됩니다. 연결되어 있기 때문에, 원격지 Repository에서 수정, 삭제, 추가 등의 행위가 발생한다면 fetch, pull의 과정이 필요합니다.
또한 본인이 상대방의 Repository에 관해 어떠한 부분을 수정거나, 추가하는 등 추가적인 작업을 진행 후 pull request를 진행합니다.
request가 상대방으로부터 승인된다면 본인이 수정한 내용이 상대방의 Repository에 기록됩니다.(commit, merge 진행) 
![Desktop View](/assets/img/2021-09-29/5.PNG){: width="90%" }

다른 사람의 Repository에 접속 후 우측 상단의 fork버튼을 누르면 동일한 이름의 Repository가 본인의 github에 생성됩니다.
![Desktop View](/assets/img/2021-09-29/6.PNG){: width="90%" }
위 예는 제가 사용했던 깃헙 블로그 테마인 [jekyll-theme-chirpy](https://github.com/cotes2020/jekyll-theme-chirpy, "jekyll-theme-chirpy")의 Repository입니다.

Fork는 추후에 필요시 포스팅을 작성하도록 하겠습니다.
<br>
<br>

## Commit
---
`Commit`이란, [이전 포스팅(초보자를 위한 GitHub Blog 만들기 - 1)](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-1/, "이전 포스팅")에서 

"그래서 누가, 언제, 무슨코드를 어떻게 했느냐 하는 기록을 남기는(흔히 형상관리라고 합니다.) 도구를 "Git"이라고 부르고,
그것을 웹페이지에서 볼 수 있도록 도와주는 서비스 중 하나가 "Github"입니다." 라고 했는데,

이때, 기록을 남기는 수단입니다.
파일의 추가 / 수정 / 삭제시에 남기는 메모로, 변경 이력을 남깁니다.
Commmit의 이름(내용)을 통해 각각의 commit을 구분합니다.

Github Desktop을 사용할시, 좌측 하단에 사용자 이미지 바로 옆 부분에 Commit 이름(내용)을 작성 후 하단의 "Commit to main"버튼을 눌러 commit을 진행합니다.

이때, main은 브런치 명입니다. branch(브런치) 관련 내용은 추후 작성하도록 하겠습니다.
![Desktop View](/assets/img/2021-09-28/5.PNG){: width="50%" }
<br>
<br>

## Push
---
`Push`란 로컬 Repository의 데이터를 원격지 Repository로 업로드 하는것을 뜻합니다.
![Desktop View](/assets/img/2021-09-29/2.PNG){: width="50%" }

commit후 push가 진행되며, 여러가지 변경들이 commit 이름에 따라 구분뒤어 업로드 됩니다.

push가 완료 되면 로컬과 원격지의 데이터 내용이 동일해집니다.
<br>
<br>

## Pull
---
`Pull`이란, 반대로 원격지 Repository를 로컬 Repository로 내려 받는것을 뜻합니다.
![Desktop View](/assets/img/2021-09-29/3.PNG){: width="50%" }

혼자서 사용하는 Repository보다는, 여러사람이 함께쓰는 Repository의 내용을 로컬로 받아오는 경우가 많습니다.
여러명이 쓰는 Repository에서 누군가 commit, push를 진행하게되면,
push를 진행한 사람은 로컬과 원격지의 데이터가 동일해지지만, 나머지 사람들은 로컬과 원격지 Repository간의 차이가 발생하기 때문에, pull을 진행해야만 합니다.

pull을 진행하면 원격지와 로컬의 데이터 내용이 동일해집니다.
<br>
<br>

git에 관해서도 찬찬히 작성하도록 하겠습니다.
git을 좀 더 쉽게 접근할 수 있는 사이트가 몇몇 있습니다.

저는 그 중 게임 형식으로 git의 사용법을 알 수 있는 [Learn Git Branching](https://learngitbranching.js.org/?locale=ko, "Learn Git Branching")을 추천드립니다!

git 관련 글도 계속해서 적어나가겠습니다!