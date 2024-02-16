---
layout: post
title: Github Blog 만들기(2)
date: 2024-02-16 15:33:00 +0900
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: study.jpg # Add image post (optional)
tags: [Backend, Java, Programming] # add tag
---
# Github 블로그 만들기(2)

## 1. Jekyll

Jekyll은 정적 웹사이트를 생성하는데 사용되는 간단하고 유연한 도구이다. Ruby라는 언어를 이용해 작성되어 있으며, Github pages와 호환되어 있어 무료로 웹사이트를 호스팅할 수 있다. 또한, Jekyll은 Markdown 언어를 사용하여 콘텐츠를 작성하고 웹사이트를 디자인 할 수 있고, Jekyll은 Github의 소스 코드 버전 관리 기능과 연동되어 있어 쉽게 웹사이트를 업데이트하고 관리할 수 있다.

Macos기준 설치 방법  
Homebrew에서 설치한다. (Homebrew가 없을 경우 Homebrew를 먼저 다운로드 해준다.  <https://brew.sh/>)  
```
brew install ruby
```

위의 명령어 실행 후 
```
echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
```
이 명령어 한 번 더 실행하기  -> 설치가 완료되면 Ruby의 패키지 관리도구인 Gem 명령어가 동작한다.
  
이 후 아래의 세가지 명령어를 순서대로 실행한다.
```
gem install bundler
gem install github-pages
sudo gem install -n /usr/local/bin jekyll
```

이제 username.github.io 로 돌아가서 .git을 제외한 내용물들(index.html..)을 삭제한 후 아래 명령어를 실행한다.
```
jekyll new .
```
그런 다음 아래 명령어를 순서대로 실행한다.
```
bundle install
bundle exec jekyll serve <!--로컬 서버가 띄워진다.-->
```
그러면 터미널 창에 server address가 나온다. 그 주소를 브라우저 주소창에 쳐주거나 cmd+클릭을 통해 주소로 이동한다.

![repository](/assets/img/download.png)

아직은 remote에 배포가 안되어 있는 상태!!
```
git add .
git commit -m"커밋 메시지"
git push
```
를 위용하여 원격에 push 해준 후 새로고침하면 minaecho.github.io로 주소가 나온다!!


