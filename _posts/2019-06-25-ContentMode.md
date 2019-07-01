---
layout: post
title:  " [iOS : ContentMode] UIImageView 의 contentMode 알기! / contentMode 로 image layout 결정하기! "
subtitle:
categories: iOS
tags: note
---

<img width="2479" alt="ContentMode" src="https://user-images.githubusercontent.com/38423205/60062311-9fb3d580-9733-11e9-9678-5e5539534b91.png">

### [마인드맵 자세히 보기](https://github.com/changSic/Task/files/3323152/ContentModePdf.pdf)

---

#### **전체 마인드맵 계층**

**contentMode**

*  원본 이미지
*  imageView
    1.  가로쪽
        1.  370 x 65
    2.  세로쪽
        1.  100 x 400
*  Scaling
    1.  scaleToFill
        1.  aspect ratio 변경
        2.  imageView 의 bounds 에 맞춰 resize
        3.  여백 없음
    2.  scaleAspectFit
        1.  aspect ratio 유지
        2.  imageView 의 bounds 에 맞추기 위해 image를 resize
        3.  나머지는 여백으로 채움
    3.  scaleAspectFill
        1.  aspect ratio 유지
        2.  imageView 의 bounds 에 채우기 위해 image 를 resize
        3.  나머지 여백 짜름 (없어짐)
*  redraw
    1.  View 의 bounds 가 변할 때 setNeedsDisplay 메소드를 호출 한다
    2.  System 은 기본적으로 View 의 bounds 가 변할 때 View 의 layout 를 redraw 를 하지 않으려고 ContentMode 를 사용하는 것
        1.  View 의 bounds 가 변할 때마다 계속 layout 을 그리면 비효율적이잖아
    3.  근데 redraw 를 하고싶으면? redraw 모드로 설정하면 된다.
*  Position
    1.  center
    2.  top
        1.  이미지의 상단 고정(pin)
    3.  bottom
    4.  left
    5.  right
    6.  topLeft
        1.  이미지 상단 좌측 고정(pin)
    7.  topRight
    8.  bottomLeft
    9.  bottomRight
