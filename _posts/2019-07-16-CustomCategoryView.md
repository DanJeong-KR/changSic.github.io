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
  <a href="/assets/ViewTouch.gif">
	<img src="/assets/ViewTouch.gif">
  </a>
	<img src="/assets/CategoryTouch.gif">
  <a href="/assets/CategoryTouch.gif">
  </a>
</figure>

<figure>
  <a href="/assets/ScrollingWithIndicatorBar.gif">
	<img src="/assets/ScrollingWithIndicatorBar.gif">
  </a>
  <figcaption>
    <a href="/assets/ScrollingWithIndicatorBar.gif" title="카테고리를 스크롤 해도 파란색 IndicatorBar가 따라갑니다 ">
    </a>
  </figcaption>
</figure>

### Usage
1. DownLoad My DemoProject

2. Copy `CustomCategoryTabBar`Folder and Paste this file into your Project
<figure>
  <a href="/assets/CustomCategoryTabBarFolder.png">
	<img src="/assets/CustomCategoryTabBarFolder.png">
  </a>
</figure>


3. Inherit CategoryTabBarViewController on the ViewController you will use
(this case is DemoViewController)
<figure>
  <a href="/assets/InheritCategoryTabBarVC.png">
	<img src="/assets/InheritCategoryTabBarVC.png">
  </a>
</figure>

4. When you initialize the ViewController, DemoViewController in this case, you can give 3 arguments and last argument is option
(First 2 argument is `withTitles`and `withViews`)
(last argument is `withScrollOption` and default is true)
<figure>
  <a href="/assets/CategoryTabBarInit.png">
	<img src="/assets/CategoryTabBarInit.png">
  </a>
</figure>

### Examples

#### If you need
* 2 categories and Category Name is `First` and `Second`, Your code is like this
<figure class = "half">
  <a href="/assets/categoryCodeDemo1.png">
	<img src="/assets/categoryCodeDemo1.png">
  </a>
  <a href="CategoryNumIs2.gif">
	<img src="CategoryNumIs2.gif">
  </a>
</figure>

* 4 categories and Category Name is `Hi` and `My` and `name` and `is`, Your code is like this
<figure class = "half">
  <a href="/assets/categoryCodeDemo2.png">
	<img src="/assets/categoryCodeDemo2.png">
  </a>
  <a href="/assets/ dCategoryNumIs4.gif">
	<img src="/assets/CategoryNumIs4.gif">
  </a>
</figure>
