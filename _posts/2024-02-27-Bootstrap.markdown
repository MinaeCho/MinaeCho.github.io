---
layout: post
title: Bootstrap 사용하기
date: 2024-02-27 20:54:00 +0900
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: boot.jpg # Add image post (optional)
tags: [Backend, Java, Programming] # add tag
---
# Bootstrap

## 1. Bootstrap의 기본


**Bootstrap을 HTML에 포함하기**

- 홈페이지에서 다운로드 받거나
- CDN을 통해서 인터넷에서 바로 받아온다.
<br>
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Bootstrap demo</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
  </head>
  <body>
   <h1>Hello </h1>
   <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-C6RzsynM9kWDrMNeT87bh95OGNyZPhcTNXj1NW7RuBCsyN/o0jlpcV8Qyq46cDfL" crossorigin="anonymous"></script>
  </body>
</html>
```
**Bootstrap- Text**

1. align
- bootstrap은 css속성을 class로 적용할 수 있게 만들어져 있다.
- 즉, text-start 클래스를 추가하면 text-align : start;가 적용된다!  
<br>
```html
<!-- 편의 기능 - 텍스트 -->
    <p class="text-start">text-start class 적용</p>
    <p class="text-center">text-center class 적용</p>
    <p class="text-end">text-end class 적용</p>
```
2. 굵기
- fw-* 클래스들로 굵기를 조정할 수 있고,
- fst-* 클래스로 기울임을 적용할 수 있다.
<br>
```html
  		<!-- 편의 기능 - 굵기와 기울기 -->
    <!-- fw-{굵기}, lighter, light, normal, bold, bolder -->
    <p class="fw-bolder">bolder 굵기</p>
    <p class="fw-lighter">lighter 굵기</p>

    <!-- fst-italic -->
    <p class="fst-italic">italic체</p>
  ```

*처음엔 bootstrap의 docs에서 콘텐트와 utilities 참고

3. color
- 글자에 적용할 때는 text-*클래스를 활용한다.
- 요소 배경에는 bg-* 클래스를 활용한다.
- text-bg-*클래스를 사용하면 배경색에 적절한 글자색이 같이 골라진다.

```html
<!-- 편의 기능 - 색상 -->
    <!-- text-{색상} -->
    <p class="text-primary">text-primary</p>
    <p class="text-info">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Id nobis eius qui odit commodi nihil dolores, impedit cupiditate nulla esse eum neque unde iste! Nisi officiis consectetur cupiditate dicta aspernatur?</p>

    <!-- bg-{색상} -->
    <p class="bg-primary">Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio cumque reiciendis placeat cupiditate blanditiis numquam. Odit nemo recusandae, ratione nisi impedit, odio rerum quaerat labore illo consequatur porro nihil aliquam.</p>

		<!-- text-bg-{색상} -->
    <p class="text-bg-primary">Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio cumque reiciendis placeat cupiditate blanditiis numquam. Odit nemo recusandae, ratione nisi impedit, odio rerum quaerat labore illo consequatur porro nihil aliquam.</p>
```

4. bootstrap-box model
- css box model을 조작하기 위한 클래스도 정의되어 있다.
    - 부모 요소를 기준으로 너비와 높이를 w-*와 h-*로 지정한다.
    - 25~100% 까지 25% 간격으로 사용 가능.

```html
<!-- 요소의 높낮이 조절 -->
    <!-- w-*, h-* 25 ~ 100% -->
    <div style="width: 500px; height: 500px;">
      <div class="w-50 h-50 bg-primary">
        <div class="w-50 h-50 bg-primary-subtle">
          <div class="w-50 h-50 bg-secondary"></div>
        </div>
      </div>
    </div>

    <div style="height: 40px;" class="vw-100 bg-info">

    </div>
```
- margin과 padding도 정의되어 있다.
    
    {m 또는 p}{방향}-{크기 (0~5 또는 auto)}
    
    -px-3:  좌우 방향으로 padding
    
    -mb-4: 아래 방향으로 margin
<br>
5. Flex
- d-flex를 사용하면 flex container가 된다.
- 축의 방향은 flex-* 형태로 정의
- flex-wrap은 flex-wrap 또는 flex-nowrap을 사용한다.
- flexbox적용도 가능하다
    - justify-content-*: start,end,center,between,around,evenly
    - align-items-*: start,end,center
    - align-content-*:start,end,center,between,around