---
layout: post
title:  "Frame and Bound"
date:   2019-04-03
excerpt: ""
tag:
- iOS
comments: true
---

### frame, bounds 모두
* UIView 의 instance property
* CGRect Type -> 사각형 이라는 의미.

### frame
* The frame rectangle, which describes the view’s location and size in **its superview’s coordinate system.**
* 이 View 가 소속되있는 superview 의 좌표 시스템이 기준으로 자신의(UIView) 위치를 지정하는 사각형
* 상위 뷰가 움직이면 하위 뷰도 움직임 -> 쉬워서 예시 안듬

### bounds
* The bounds rectangle, which describes the view’s location and size in **its own coordinate system.**
* 자기 자신의 좌표 시스템을 기준으로 자신(UIView)를 표현하는 사각형(rectangle)
* 예시
  * <img width="293" alt="스크린샷 2019-04-17 오후 5 48 03" src="https://user-images.githubusercontent.com/38423205/56274521-d10f9400-6139-11e9-8df9-eb1f566cef1f.png">
  * frame 이 이렇게 잡혀있는데
  * 이 때 상위 뷰 , 하위 뷰 모두 bounds.origin 은 0
  * 여기서 노란색 뷰(상위 뷰) 의 bounds.origin  70, 80 으로 바꾸면
  * <img width="287" alt="스크린샷 2019-04-17 오후 5 48 57" src="https://user-images.githubusercontent.com/38423205/56274520-d10f9400-6139-11e9-8248-2db84ab61e00.png">
  * 70, 80 인 지점에서 노란색 뷰(상위 뷰) 만 새로 그린다.
  * 그러므로 빨간 뷰(하위 뷰) 는 왼쪽 위로 올라간 것처럼 보임 -> 스크롤 뷰의 원리


### ScrollView 의 핵심이 bounds
<img width="819" alt="스크린샷 2019-04-17 오후 5 52 08" src="https://user-images.githubusercontent.com/38423205/56274519-d076fd80-6139-11e9-8c56-87222792df6d.png">
* ScrollView 의 bounds 를 양수로 변경하면 아이폰을 움직이지 않아도 다른 화면을 스크롤 해서 볼 수 있음.
