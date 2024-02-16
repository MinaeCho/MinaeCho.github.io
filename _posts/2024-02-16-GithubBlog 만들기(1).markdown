---
layout: post
title: Github Blog 만들기(1)
date: 2024-02-16 15:33:00 +0900
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: study.jpg # Add image post (optional)
tags: [Backend, Java, Programming] # add tag
---
# Github 블로그 만들기(1)

## 1. 새로운 Repository를 만들자


![repository](/assets/img/screenshot.png)

이때 repository name은 Owner랑 일치해야 한다.

Repository name : username.github.io 의 형식으로 만들어 준다!!  
<br>
## 2. 자신의 폴더로 repository를 clone 하자

동일한 페이지에서 초록색 Code 버튼을 누르면 clone을 할 수 있는 주소가 나온다.

이 주소를 복사 한 뒤 터미널을 열어 clone하고 싶은 폴더에서 **git clone HTTPS주소** 명령어를 이용해 clone을 해준다.  
<br>

## 3. Clone 한 폴더에서 index.html 파일을 생성하자

만들어진 repository를 git clone 한 후 Visual Studio Code 에서 연 후에, ```index.html``` 을 만들어 준다.

이는 웹 브라우저가 홈페이지 url에 처음 접근 하였을때 읽는 파일이다. -> 추후 삭제 예정  
<br>

## 4. Github에 공유하자
**git add .** , **git commit -m"add index.html"**, **git push** 명령어를 통해 Github에 공유한다.

![repository](/assets/img/screenshot2.png)

이후 Github의 settings->Pages를 보면, 나의 Github블로그가 만들어진 것을 확인 할 수 있다.

해당 링크로 이동하면 아까 만들었던 index.html이 보인다.

