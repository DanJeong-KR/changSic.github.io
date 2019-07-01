---
layout: post
title:  "ScrollView 내부의 객체 AutoLayout 설정하기"
date:   2019-04-11
excerpt: ""
tag:
- iOS
- UIScrollView
- AutoLayout
comments: true
---


### ScrollView
제한된 뷰의 크기보다 더 큰 크기를 가진 컨텐츠를 표현하기 위한 뷰
* e.g 지도를 표현할 때 아이폰 스크린의 제한된 크기로 지도 콘텐츠를 전부 표현을 못하기 때문에 스크롤을 이용해서 보지 못하는 부분을 볼 수 있게 한다.
* <img width="507" alt="스크린샷 2019-04-11 오후 2 09 36" src="https://user-images.githubusercontent.com/38423205/56101980-1bd7b300-5f64-11e9-9bcb-165a00f06a39.png">


### 스토리 보드로 하기
[ScrollViewExample](https://github.com/changSic/Task/tree/master/Week6/ScrollView/ScrollViewExample)
* 2가지 방법
  * 스크롤 뷰를 넘어서는 뷰 위치 설정   
    * <img width="857" alt="스크린샷 2019-04-11 오후 5 08 06" src="https://user-images.githubusercontent.com/38423205/56101985-1e3a0d00-5f64-11e9-9ccd-6e0b097f260a.png">


  * 스크롤 뷰 안에 보여질 뷰들 설 (보기 쉽지만 트릭 사용)    
    * <img width="460" alt="스크린샷 2019-04-11 오후 3 13 24" src="https://user-images.githubusercontent.com/38423205/56101981-1c704980-5f64-11e9-8fb0-83e5815da658.png">
    * width 값을 내가 보기쉽게 0.5 하나 , 실제 크기인 스크롤 뷰의 width 로 2개 설정한다.
    * 0.5 인 아이는 build time 에서 보이지 않도록 설정한다.
      * <img width="262" alt="스크린샷 2019-04-15 오전 10 52 48" src="https://user-images.githubusercontent.com/38423205/56103223-af14e680-5f6c-11e9-92ff-873a0d598b69.png">
    * width 가 ScrollView 인 아이는 prioirty 를 999 로 설정해주면 우선순위에 따라서 0.5 인 아이가 없어지면 나타난다. -> 이래서 트릭이라고 하는 것

### 코드로 하기
[ScrollViewByCode](https://github.com/changSic/Task/tree/master/Week6/ScrollView/ScrollViewByCode)
* 1.AutoresizingMask 라는 속성 false 로 해주기
  * UIView 에서 AutoresizingMask 라는 속성이 autolayout 으로 default 로 설정되기 때문에 이 속성을 false 로 해주지 않으면 내가 설정한 autolayout 과 충돌한다. (겹친다.)

* 2. ScrollView 오토레이아웃 설정하기.
  * <img width="978" alt="스크린샷 2019-04-15 오후 6 53 20" src="https://user-images.githubusercontent.com/38423205/56123655-d7720480-5faf-11e9-9416-a8642be34c7b.png">
  * **먼저 AutoresizingMask 라는 속성 false 로!!**

* 3. UIView 객체 오토레이아웃 설정하기 (초기화는 이미 다 한것임)
  * <img width="821" alt="스크린샷 2019-04-15 오후 6 53 47" src="https://user-images.githubusercontent.com/38423205/56123654-d6d96e00-5faf-11e9-8d78-9215994766a1.png">
  * ScrollView 안에 들어가는 뷰이므로 **앞, 뒤, 위, 아래, 넓이, 높이 모두 설정해 주어야 함을 주의**
