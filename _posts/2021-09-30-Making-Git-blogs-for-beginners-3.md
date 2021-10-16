---
title: 초보자를 위한 GitHub Blog 만들기 - 3
author: Dodev 하다
date: 2021-09-30 20:28:00 +0900
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

## Step 3.  블로그 기본 설정하기
---
본인의 블로그 주소로, 원하는 테마 업로드를 완료하였다면, 기본 설정 몇가지가 더 필요합니다.
이번 포스팅에서는 기본 설정에 관해 이야기하도록 하겠습니다.
<br>
<br>

### Step 3-1. _config.yml파일 확인하기
---
본인 로컬 폴더, VSCode 탐색기를 보시면, `_config.yml`파일이 존재합니다. 해당 파일은 테마마다 다르기 때문에, 설정에 관해서라면 다운로드하였던 테마 `제작자의 README.md 등을 참고`하여 확인하시면 훨씬 편하게 설정 할 수 있습니다.
저는 jekyll-theme-chirpy테마를 다운로드 받았기에, 다른 테마를 사용하신다면 _config.yml파일의 내용이 상이할 수 있습니다.

```yml
theme: jekyll-theme-chirpy  # import하는 테마 명입니다. 디폴트로 사용중인 테마 명이 들어가 있으므로, 수정은 하지 않습니다.

baseurl: ''     # 사용자 페이지를 만들었을 경우, 빈칸으로 둡니다. 프로젝트 페이지를 만든 경우 프로젝트 명을 적어줍니다.
                # 사용자 페이지와 프로젝트 페이지를 모르신다면, [초보자를 위한 GitHub Blog 만들기 - 1](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-1/)에서 Step 1-2. repository생성을 참고하시길 바랍니다.
=
lang: ko-KR     # 사용하는 언어 설정을 진행합니다. http://www.lingoes.net/en/translator/langcode.htm 로 접속하여 확인가능합니다.

timezone: Asia/Seoul    #timezone설정입니다. http://www.timezoneconverter.com/cgi-bin/findzone/findzone 에서 확인가능합니다.

# jekyll-seo-tag settings › https://github.com/jekyll/jekyll-seo-tag/blob/master/docs/usage.md
# ↓ --------------------------

title: Dodev                          # 블로그 이름입니다. 설정하면 브라우저 상단에 설정된 이름이 확인가능합니다.

tagline: Dodev 하다   # 서브 타이틀 입니다. 설정하면 블로그 첫 페이지 좌측에서 확인 가능합니다.

description: >-                        # "used by seo meta and the atom feed"라고 나옵니다. 저는 설정을 그대로 두었습니다.
  A minimal, portfolio, sidebar,
  bootstrap Jekyll theme with responsive web design
  and focuses on text presentation.

url: 'https://wlqmffl0102.github.io'    # 'https://username.github.io'와 같이 설정합니다. 설정이 잘 못 되면 곤란합니다. 
                                        # 잘 적어넣도록 합니다.

github:
  username: wlqmffl0102             # 본인의 github username을 적습니다.

#twitter:
#  username: twitter_username            # 본인의 twitter username을 적습니다. 저는 트위터는 사용하지 않아 주석 처리 해 두었습니다.

social:
  # Change to your full name.
  # It will be displayed as the default author of the posts and the copyright owner in the Footer
  name: Dodev-하다
  email: wlqmffl0102@naver.com             # change to your email address
  links:
    # The first element serves as the copyright owner's link
    #- https://twitter.com/username      # change to your twitter homepage
    - https://github.com/wlqmffl0102       # change to your github homepage
    # Uncomment below to add more social links
    # - https://www.facebook.com/username
    # - https://www.linkedin.com/in/username

    # 상단은 social관련 내용입니다. 본인의 이름, 이메일, 링크 등을 작성합니다. 저는 깃허브만 올려두었습니다.

google_site_verification: 000 # Google Search Console관련 내용입니다. 이후 포스팅에서 다루겠습니다.

# ↑ --------------------------


google_analytics:
  id: '000'              # Google Analytics ID입니다. 이 또한 이후 포스팅에서 다루겠습니다.
  pv:           
    proxy_endpoint:   
    cache_path:       

theme_mode:   # chirpy테마는 [light|dark]테마를 지원합니다. 비워두시면 사용자의 디폴트 값이 설정되고, light 또는 dark로 입력해두시면 페이지의 기본 테마가 설정됩니다.

img_cdn: ''  #cdn 이미지 설정입니다. 저는 따로 진행하지 않았으나 진행하시려면 url을 작성해주시면 됩니다.

avatar: /assets/img/profile.png     # 대표이미지 라고 생각하시면 됩니다. /assets/img경로에 사진을 넣은 뒤 작성하시면 됩니다.

toc: true       # toc(Table of contents)입니다. 블로그 보시다 보면 포스팅 옆에서 스크롤을 따라오는 목차같은 녀석이 있습니다.
                # 사용하시려면 true, 아니라면 false를 적으시면 됩니다.

disqus:
  comments: true  # disqus라는 덧글기능을 하는 녀석입니다. 사용하시려면 true, 아니라면 false를 적으시면 됩니다.
  shortname: 'Dodev-HADA'    # 사용하신다면 https://disqus.com/ 에 가입 후, shortname을 넣어줍니다.

paginate: 10        

# ------------ 아래로는 크게 손 볼 것 없어서 생략합니다. ------------------

```

위에도 이야기 했듯, 해당 파일은 테마마다 다르기 때문에, 설정에 관해서라면 다운로드하였던 테마 제작자의 repository에서 참고하시길 바랍니다.
저는 jekyll-theme-chirpy테마를 다운로드 받았기에, <https://github.com/cotes2020/jekyll-theme-chirpy> 으로 접속하시면 다양한 내용을 찾아 볼 수 있습니다.
<br>
<br>

### Step 3-2. 파일 삭제 및 추가작업
---
jekyll-theme-chirpy의 제작자의 안내에 따라 추가 작업을 진행하겠습니다.

1. `.travis.yml`파일 삭제
2. `_posts 폴더` 안의 파일 삭제 -> 이것은 참고할만한 포스팅이 몇가지 있기 때문에, 보시고 불필요한것만 먼저 삭제하시고,
                                나머지는 참고하셨다가 추후에 삭제하시는 편이 좋다고 생각합니다.
3. `docs폴더` 삭제
4. `.github폴더` 안에서, workflows폴더를 제외한 나머지 폴더, 파일 삭제(ISSUE_TEMPLATE폴더, CODE_OF_CONDUCT.md파일, CONTRIBUTING.md파일, FUNDING.yml파일, PULL_REQUEST_TEMPLATE.md파일, stale.yml파일 총 6개)
5. .github폴더 > workflows폴더에서 ci.yml파일, issue-pr-interceptor.yml파일 2개 삭제
6. **중요!!!** `.github>workflows>pages-deploy.yml.hook`파일이 있을텐데, 해당 파일에서 마지막 `.hook`부분을 지워서. `.github>workflows>pages-deploy.yml`파일로 만들어 줍니다.
7. 이후에, 해당 파일을 열어보면 가장 상단 branches를 수정합니다.
   ```yml
   name: 'Automatic build'
    on:
    push:
        branches:
        - main          # 이 부분을 꼭 master에서 main으로 수정해줍니다.
        paths-ignore:
        - .gitignore
        - README.md
        - LICENSE
   ```
<br>
<br>

### Step 3-3. 배포관련 추가내용
---
jekyll-theme-chirpy는 github에 push(배포)시에 main브런치 이외에 gh-pages브런치를 생성합니다.
여기서 머리아픈 이야기들이 나오는데, 본인 github repository로 이동하여 확인가능합니다.
![Desktop View](/assets/img/2021-09-30/1.PNG){: width="90%" }

내용을 주욱 이야기 하자면, 머리 아프기 때문에 간단하게 말하자면.
main브런치로 사용하는것을 `pages-deploy.yml`파일에서 명명해주었으나, 자동으로 chirpy테마는 ci / cd구성이 구축되어 있어 main으로 배포하더라도 자동으로 gh-pages브런치가 생성된다. 정도만 아시면 될 것 같습니다.

gh-pages브런치를 이용하여 페이지 설정 하는 부분도 있으나, main브런치를 이용해 페이지를 사용하고 있지만 문제가 되는 점은 하나도 없기에 알고만 계시면 될 것 같습니다.
<br>
<br>

### Step 3-4. 로컬서버에서 페이지 확인해보기
---
여러가지 수정사항이 정상적으로 반영되는지 우선 로컬 서버에서 확인해보겠습니다.
변경사항들을 모두 저장 후, `Start Command Prompt with Ruby`를 실행합니다.
![Desktop View](/assets/img/2021-09-28/2.PNG){: width="100%" } 
<br>
본인의 git Clone경로(폴더)로 이동합니다.(아래는 제 경로입니다)
```
 cd C:\Users\wlqmf\Documents\GitHub\wlqmffl0102.github.io
```
<br>
jekyll 서버 동작
```
 bundle exec jekyll serve
```

<http://127.0.0.1:4000/> 또는 <http://localhost:4000/>으로 접속하여 변경사항을 정상적으로 확인했다면, github desktop을 이용해 commit, push진행을 해줍니다.

5~10분 뒤, 본인의 Github Page 주소 즉, 저에게는 <https://wlqmffl0102.github.io/> 으로 접속하여 정상적으로 페이지가 보인다면 끝입니다!
<br>
<br>

## 마무리
---
깃 블로그 만들기 포스팅은 계속됩니다!

## 다음포스팅
---
[초보자를 위한 GitHub Blog 만들기 - 1](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-1/)

[초보자를 위한 GitHub Blog 만들기 - 2](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-2/)

[초보자를 위한 GitHub Blog 만들기 - 3](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-3/)

[초보자를 위한 GitHub Blog 만들기 - 4](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-4/)
<br>
<br>