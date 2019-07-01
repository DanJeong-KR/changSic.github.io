---
layout: post
title:  "MVC Design Pattern"
date:   2019-04-17
excerpt: ""
tag:
- iOS
- DesignPattern
comments: true
---

# MVC
### The King of Design Pattern
* Model - View - Controller 는 iOS 의 기초를 이룬다.
* MVC 는 M, V, C를 각각의 일반적인 역할에 따라 분류하고 이 역할을 기반으로 코드를 깔끔하게 분리한다.

**Model**
* Application 의 **데이터 자체를 정의하며 이것을 어떻게 다룰것인지 정의하는 객체.**
* 대부분의 Application 은 1개 이상의 type(class) 를 가지게 될 것.

**View**
* Model 과 사용자가 상호작용 할 수 있는 control(버튼같은)의 **시각적인 표현**을 담당하는 객체.
* 기본적으로 거의 모두 UIView 를 상속받은 객체이다.

**Controller**
* 컨트롤러는 거의 모든 일을 관리하고 조직하는 **중간에서 다리역할**을 하는 객체이다.
* **Model로 데이터에 접근하고 View 에서 그 데이터를 보여준다.**
* 이벤트를 감지하고 필요에 따라 데이터를 조절한다.


### 이게 베스트
<img width="483" alt="스크린샷 2019-04-17 오후 7 45 30" src="https://user-images.githubusercontent.com/38423205/56282157-69f9db80-6149-11e9-9f35-75d14145740b.png">

![IMG_1254](https://user-images.githubusercontent.com/38423205/56965810-0a63ed00-6b99-11e9-88bf-d76d12faf546.jpeg)
