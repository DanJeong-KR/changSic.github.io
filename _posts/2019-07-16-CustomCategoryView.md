---
layout: post
title:  "Custom Category TabBar 만들었어요!"
date:   2019-07-10
excerpt: "Category TabBar 를 추상화 시켜서 어디든 재사용 할 수 있게 만들어보자!
"
tag:
- iOS
- OpenSource
comments: true
---

# Custom Category TabBar

### Features
<figure class="half">
	<img src="/assets/ViewTouch.gif">
	<img src="/assets/CategoryTouch.gif">
</figure>

<figure>
	<img src="/assets/ScrollingWithIndicatorBar.gif"></a>
  <figcaption> 카테고리를 스크롤 해도 파란색 IndicatorBar가 따라갑니다 </figcaption>
</figure>

### Usage
1. DownLoad My DemoProject

2. Copy CustomCategoryTabBarFolder and Paste this file into your Project
<figure class="half">
	<img src="/assets/CustomCategoryTabBarFolder.png">
</figure>

3. Inherit CategoryTabBarViewController on the ViewController you will use
(this case is DemoViewController)
