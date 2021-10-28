---
title: 초보자를 위한 GitHub Blog 만들기 - 4
author: Dodev 하다
date: 2021-10-01 20:28:00 +0900
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

## Step 4. Google Search Console / Google Analytics / Google Adsense
---
블로그 기본 설정이 완료 되었다면, 이제는 이 블로그가 다른 사람에게도 잘 보이는지, 잘 운영되고 있는지, 가능하다면 짤짤이를 벌 수 있는지 확인해보도록 하겠습니다.

아 복잡해! 라고 생각 할 수 있지만, 천천히 따라하시면 금방 할 수 있다고 생각합니다.

자 우선,
> Google Search Console 이란

많은 사람들이 무언가 검색을 한다면 무엇을 이용할까요? 네이버, 다음과 같은 국내 포털사이트도 있지만 Google을 통해서 검색하는 경우도 많을 것 입니다.
Google Search Console은 제 블로그가, 제 블로그의 포스팅이 Google로 검색하면 나오도록 해 주는 녀석입니다.

> Google Analytics 란

말 그대로 Analytics(분석)입니다. 누가, 언제, 어디서, 얼마나 제 블로그에 접속하였는지, 여러가지 요소를 분석해주는 녀석입니다.

> Google Adsense 란

여러 블로그 및 사이트에서 광고가 나오는것을 기억하실텐데요, 이녀석 입니다. 제 블로그 / 사이트에 광고를 띄우는것이죠.
귀찮은 광고를 내 블로그에 띄운다는데, 왜? 라고 생각 할 수 있지만, Google Adsense를 이용해 블로그에 광고를 띄우고, 다른사람이 광고를 통해 어떠한 url로 접속하여 수익이 창출되어, 광고비를 제가 얻을 수 있답니다. 

와 모두 너무 좋은 기능들이예요. 혼자만의 힘으로 하기 어려운 것을 각각의 사이트에 계정생성, url연동 등으로 쉽게 사용가능하답니다.

하나씩 시작하겠습니다.
<br>
<br>

## Step 4-1. Google Search Console
---
우선 [Google Search Console](https://search.google.com/search-console/about?hl=ko&utm_source=wmx&utm_medium=wmx-welcome)로 이동하여, 시작하기 버튼을 클릭합니다.

좌측은 구매한 도메인이 있는 경우, 우측은 일반적인 GitBlog일경우입니다.
저는 도메인 구매 및 추가 설정을 하지 않은 일반적인 Git blog형식으로, 우측을 이용하도록 하겠습니다.
URL에 블로그 전체주소(https://wlqmffl0102.github.io/)를 적어줍니다.
![Desktop View](/assets/img/2021-10-01/1.png){: width="90%" }

해당 url이 본인의 소유인지 확인합니다.
아래에 보이는 googlexxxxxxx~.html파일을 다운로드 한 뒤, <https://wlqmffl0102.github.io/> 페이지에 업로드 하라고 나옵니다.
<https://wlqmffl0102.github.io/> 페이지는 index페이지 인데, VSCode에서 Gemfile이 있는 위치에 index.html이 하나 있습니다.
그곳에 다운로드 한 html파일을 넣습니다.

![Desktop View](/assets/img/2021-10-01/2.png){: width="90%" }

![Desktop View](/assets/img/2021-10-01/3.PNG){: width="70%" }

Github Desktop을 이용해 commit과 push를 진행합니다.

정상적으로 push가 완료 되었다면, 아래의 확인버튼을 눌러 계속해서 진행합니다.
![Desktop View](/assets/img/2021-10-01/2.png){: width="90%" }

소유권이 확인되었다면, 제가 쓴(혹은 쓰게 될) 포스팅 페이지 등 블로그 내에 여러가지 페이지 등을 google에서 읽을 수 있도록(크롤링 할 수 있도록) 추가적인 작업을 진행해야합니다.

Gemfile에 아래 문구를 한 줄 하단에 추가해줍니다.
```
gem 'jekyll-sitemap'
```
![Desktop View](/assets/img/2021-10-01/4.PNG){: width="90%" }

Ruby Prompt에서 명령어를 입력
```
 bundle install
```

입력 후 기다렸다가 확인해보시면 jekyll-sitemap을 install한것이 확인가능합니다.
![Desktop View](/assets/img/2021-10-01/5.PNG){: width="90%" }

```
 jekyll serve
```
명령어 입력 후, 잠시 뒤 <http://localhost:4000/sitemap.xml> 으로 접속 해 봅니다. 
xml로 이루어진 페이지가 보인다면 해당 페이지 전체를 복사하여 Gemfile이 있는 위치에 sitemap.xml파일을 생성 후 붙여넣어줍니다.
sitemap.xml파일이 이미 생성되어 있다면 그대로 두셔도 무관합니다.

해당 방법 말고, sitemap.xml을 생성해주는 사이트도 많이 있습니다.
[https://www.xml-sitemaps.com/](https://www.xml-sitemaps.com/)과 같은 사이트 입니다. 
화면 가운데 Your Website URL을 적어 넣으신 뒤, start버튼을 눌러주시면 자동 생성 됩니다.
생성받은 sitemap.xml파일을 정확한 위치에 넣어주시면 됩니다.

마지막으로 sitemap.xml이 있는 동일한 위치에 robots.txt 파일을 생성하고, 내용을 다음과 같이 적습니다.
```
User-agent: *
Allow: /

Sitemap: https://wlqmffl0102.github.io/sitemap.xml
```
Sitemap의 주소는 본인 블로그 주소를 넣으셔야 합니다.

Github Desktop을 이용해 commit과 push를 진행합니다.

push가 정상적으로 이루어 졌다면, [Google Search Console](https://search.google.com/search-console)의 Sitemap항목으로 들어가 sitemap.xml을 올려줍니다.

![Desktop View](/assets/img/2021-10-01/6.png){: width="90%" }

등록이 완료 된 후 7일 이내로 검색 엔진에 노출됩니다.
<br>
<br>

## Step 4-2. Google Analytics
---
[Google Analytics](https://analytics.google.com/analytics/web)로 이동합니다.

첫 화면에서 파란색 "측정 시작"이라는 버튼을 누르면 진행이 됩니다.

1. 계정 설정 단계에서는 계정 이름만 적어줍니다. 말 그대로 계정 이름으로, 편하신것 아무거나 입력하시면 됩니다. 저는 제 본인 이름을 넣었다가, 그냥 wlqmffl0102_github라고 입력하였습니다.
![Desktop View](/assets/img/2021-10-01/8.PNG){: width="90%" }

체크를 하시거나 체크를 해제하는것 없이 디폴트 값 그대로 두고 다음 버튼 클릭.
![Desktop View](/assets/img/2021-10-01/9.PNG){: width="90%" }

<br>

2. 속성 설정 에서 몇가지 중요한 설정들이 나옵니다.
속성 이름은 본인 블로그 주소를 넣어줍니다. http 혹은 https까지 모두 포함된 주소를 입력하시면 됩니다.
보고 시간대 및 통화는 "대한민국"으로 맞춰주시면 됩니다.
![Desktop View](/assets/img/2021-10-01/11.PNG){: width="90%" }

**여기서 중요!!!** 조금 아래로 내리면 `고급 옵션 열기`라고 하는 버튼이 보이십니다.
이 설정을 꼭 해주셔야만 블로그-애널리틱스 연결이 가능합니다!
고급 옵션을 열면 `유니버설 애널리틱스 속성 만들기`라고 보이실텐데, 우측 버튼을 눌러 활성화 시켜주시고, URL을 입력합니다.
아래 버튼들은 디폴트 값 그대로 두시고 다음 버튼을 클릭합니다.
![Desktop View](/assets/img/2021-10-01/12.PNG){: width="90%" }

<br>

3. 비즈니스 정보는 대충 입력해주시고, 다음 버튼을 클릭합니다.

<br>

4. 이후에 약관이 나올텐데, 약관 언어를 대한민국으로 설정 후 동의 진행해주시면 됩니다.

정상적으로 설정 되셨다면 애널리틱스 홈 화면이 보이실겁니다.
그 중 좌측 하단 "관리"탭으로 들어갑니다.

![Desktop View](/assets/img/2021-10-01/14.PNG){: width="90%" }

속성 설정에서 `유니버설 애널리틱스 속성`을 만드셨다면 다음과 같이 유니버설 애널리틱스 속성화면을 보실 수 있습니다.
그 중, `추적 코드`버튼을 누릅니다.
![Desktop View](/assets/img/2021-10-01/15.PNG){: width="90%" }

그러시면 하단에 추적 ID 및 범용 사이트 태그를 보실 수 있습니다.
jekyll-theme-chirpy는 _config.yml에서 Google Analytics관련 설정을 할 수 있기 때문에, 추적 ID를 복사 후, _config.yml파일을 열어, 해당 부분에 값을 입력해줍니다.

```yml
google_analytics:
  id: 'UA-*********-1'              # 이쪽에 넣어주시면 됩니다.
```

이때, 추적 ID는 꼭 **UA**로 시작합니다. 유니버설 애널리틱스의 추적아이디가 필요로 하기때문에, 헷갈리지 않으시길 바랍니다.

테마 중, _config.yml에서 Google Analytics관련 설정을 지원하지 않는 경우, "범용 사이트 태그(gtag.js)"를 이용하여야 합니다.
_includes폴더 안에 head.html 또는 footer.html에 해당 스크립트를 복사 붙여넣기 해주시면 됩니다.

듣자하니 footer에 넣으면 가장 마지막에 analytics가 로드되면서 사이트 로드가 느려지는것을 방지 할 수 있다고 합니다.
<br>
<br>

## Step 4-2. Google Adsense
---
Google Adsense는 가입 절차는 쉬운편이라 캡쳐없이 글로 적겠습니다.


[Google Adsense](https://www.google.com/adsense/)로 접속하여 시작하기 버튼을 클릭합니다.

Google Adsense 가입이 진행되는데, 웹사이트 URL과 이메일 주소 등 정보를 입력합니다.

국가 또는 지역을 대한민국으로 맞춘 뒤, 약관에 동의합니다.

수익금을 받기 위해 결제 프로필을 등록합니다. 주소 및 연락처 등 개인정보를 입력합니다.

가입이 거의 이루어질 쯤, 구글 애드센스 코드를 웹 사이트에 적용하라고 뜰텐데, 이 부분이 중요합니다.

해당 애드 센스 코드를 복사하여, _includes폴더안 head.html에 붙여넣어 줍니다.저는 head.html <head>태그 안쪽 가장 하단에 넣어줬습니다.
```html
<!--...중략...-->
  <!-- JavaScript -->
  <script src="https://cdn.jsdelivr.net/npm/jquery@3/dist/jquery.min.js"></script>

  <!-- Google Addsence -->
  <script data-ad-client="ca-pub-8857040748920572" async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
  
</head>
  
```

이때, data-ad-client값인 ca-pub-8857040748920572가 본인의 애드센스 id가 됩니다.

우선 넣으셨다면 Github Desktop을 이용해 commit과 push를 진행합니다.
push가 정상적으로 이루어졌다면, 다시 Adsense페이지로 돌아가 "코드를 사이트에 붙여넣었습니다" 부분에 체크 후 완료 버튼을 눌러 줍니다.

코드 확인 완료 창이 뜬 뒤, 1일 이내로 사이트 검토에 들어가며, 승인이 될 때까지 기다립니다. 보통 1~14일 정도 소요됩니다.
코드 확인이 제대로 되지 않은 경우, 잘못된 장소에 코드가 들어갔거나, push가 제대로 이루어지지 않는 등의 경우가 있습니다.


승인이 된 경우 메일이 온다고 합니다.

사실 저도 아직 승인을 기다리고 있는중이라, 해당건에 관해서는 승인 후 추가하도록 하겠습니다!
양질의 게시글이 어느정도 있어야 승인이 된다고 합니다.
아직 저는 신생 블로거라, 한참 남았을거라 생각합니다. 꼭 추후에 승인 이후 과정도 넣고 싶습니다.

자, 이렇게 어느정도 블로그의 모양새가 나왔을거라 생각합니다.
추가적으로 질문을 받게되면 게시글을 계속 추가해나가고 싶습니다.


[ 2021.10.27 추가내용 ]
10월 초에 해당 게시글을 작성하고, 구글 애드센스도 함께 신청하였는데요!

추가하는 내용은 다름아님 승인이 되어 애드센스가 "계정이 활성화되었습니다."라는 화면이 확인되었습니다!!
저는 사실 4번정도 "애드센스 사이트가 다운되었거나 사용할 수 없음"으로 승인 거절을 당한 뒤, sitemap.xml과 robots.txt파일을 수정한 뒤,
3주 쪼오금 더 지나서 오늘 승인이 났습니다~!

관련사항은 내용을 덧붙이지 않고 새로운 포스팅으로 찾아뵙겠습니다
링크를 타고 들어가시면 바로 확인가능하십니다!
<br>
<br>

## 보너스. disqus 덧글 기능 이용하기
---
[disqus](https://disqus.com/)에 접속합니다.

GET STARTED버튼을 눌러 Sign in(회원가입)을 진행합니다. 어렵지 않게 진행가능합니다.

회원가입 후 로그인하게 되면 I want to comment on sites / I want to install Disqus on my site버튼 두개가 보이실 텐데요, 
jekyll-theme-chirpy는 _config.yml에서 Disqus관련 내용이 존재합니다. 따라서 I want to comment on sites버튼을 누르시면 됩니다.
이후에 _config.yml파일에 disqus관련 내용을 적어주시면 됩니다.

```yml
disqus:
  comments: true  # boolean type, the global switch for posts comments.
  shortname: 'Dodev-HADA'    # Fill with your Disqus shortname. › https://help.disqus.com/en/articles/1717111-what-s-a-shortname
```

테마 중, _config.yml에서 disqus관련 설정을 지원하지 않는 경우, 소스 코드를 수정해야 할 수도 있습니다. 다만 제가 알기론 거의 대부분의 테마들은 disqus관련 기능설정 부분이 있는 것으로 압니다.
<br>
<br>

## 마무리
---
좀 더 포스팅이 길어질거라 예상했는데, 의외로 4개로 끝나버렸네요.
뭔가 잊어버린게 있으려나.. 잘 모르겠습니다.

보시기에 불편하시거나, 잘 안되거나, 문제가 발생하는 등의 내용은 연락바랍니다. 
<br>
<br>

## 초보자를 위한 GitHub Blog 만들기 시리즈
---
[초보자를 위한 GitHub Blog 만들기 - 1](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-1/)

[초보자를 위한 GitHub Blog 만들기 - 2](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-2/)

[초보자를 위한 GitHub Blog 만들기 - 3](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-3/)

[초보자를 위한 GitHub Blog 만들기 - 4](https://wlqmffl0102.github.io/posts/Making-Git-blogs-for-beginners-4/)
<br>
<br>