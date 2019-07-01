---
layout: post
title:  " [iOS : CoreGraphics] CGAffineTransform 을 사용해서 Animation 구현하기! "
subtitle:
categories: iOS
tags: note
---

#### UIView 아래의 Animation 계층
<img width="269" alt="스크린샷 2019-06-25 오전 11 17 39" src="https://user-images.githubusercontent.com/38423205/60073389-43fd4280-975b-11e9-914d-7f85d9a3d56e.png">

---

<img width="1777" alt="CGAffineTransform" src="https://user-images.githubusercontent.com/38423205/60073162-a30e8780-975a-11e9-8ce5-e33153de93d9.png">

#### [마인드맵 자세히 보기](https://github.com/changSic/Task/files/3323777/CGAffineTransform.pdf)

---

-   #### CGAffineTransform

    1.  3 x 3 matrix 로 표현된다
        1.  point (x, y) 에서 변경된 결과 point(x', y')
    2.  이어붙이기
    3.  줄이거나 늘리기
        1.  공식
        2.  두값이 - 값이면 회전한다.
    4.  움직이기
    5.  회전하기
    6.  원상 복귀 하기
