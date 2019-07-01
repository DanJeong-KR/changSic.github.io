---
layout: post
title:  "코드로 구현하는 AutoLayout"
date:   2019-04-10
excerpt: ""
tag:
- iOS
- AutoLayout
comments: true
---

## 코드로 구현하는 오토레이아웃

- AutoLayout Anchor
- [예제프로젝트 AutoLayoutByCode](<https://github.com/changSic/Task/tree/master/Week6/AutoLayout/AutoLayoutByCode>)
- [예제프로젝트 - 스토리보드로, 코드로 오토레이아웃 구현하기](<https://github.com/changSic/Task/tree/master/Week6/AutoLayout/Assignment/ProblemAutoLayout>)

------

### NSLayoutContraint

- 코드가 너무 길고 복잡

  - <img width="646" alt="스크린샷 2019-04-09 오후 4 09 57" src="https://user-images.githubusercontent.com/38423205/55786364-0d664300-5aef-11e9-84f3-5352884da138.png">

- 그래서 iOS9 부터 **NSLayoutAnchor** 나옴

  - <img width="890" alt="스크린샷 2019-04-09 오후 4 11 42" src="https://user-images.githubusercontent.com/38423205/55786368-0fc89d00-5aef-11e9-84ab-ffc4e45951f5.png">

- 내부적으로는 NSLayoutContraint 를 사용하기 때문에 알고 있으면 더 잘 이해할 수 있다.

  - autolayout 을 코드로 구현할 때는 view.safeAreaLayoutGuide 프로퍼티로 제약사항 건다

    (frame 은 view.safeAreaInset 이었었지? **차이점**)

### Anchor 속성들 사진으로 보고 이해하자

<img width="559" alt="스크린샷 2019-04-09 오후 5 53 03" src="https://user-images.githubusercontent.com/38423205/55787039-61bdf280-5af0-11e9-9718-2ccf2a62571a.png">

<img width="480" alt="스크린샷 2019-04-09 오후 5 53 09" src="https://user-images.githubusercontent.com/38423205/55787044-62ef1f80-5af0-11e9-880c-d9738b16fccb.png">

### View 의 수평선, X축에 관련된 제약조건 (**Horizontal Layout Anchors**)

- **NSLayoutXAxisAnchor** **클래스의 객체**
  - Leading anchor
  - Trailing anchor
  - Left anchor
  - Right anchor
  - Center-X anchor



### View 의 수직선, Y 축에 관련된 제약조건 (**Vertical Layout Anchors**)

- **NSLayoutYAxisAnchor** **클래스의 객체**
  - Top anchor
  - Bottom anchor
  - Center-Y anchor
  - First baseline anchor (안함)
  - Last baseline anchor (안함)

### View 의 크기 (**Dimension Layout Anchors**)

- **NSLayoutDimension** **클래스의 객체**
  - Width anchor
  - Height anchor

------

### AutoResizingMaslk

AutoLayout 을 코드로 구현할 때 **autoResizingMask** 를 꺼줘야 하기 때문에 autoResizingMask 보고 넘어간다.

- 코드로 오토레이아웃 잡을때는 꼭 아래의 구문으로 Mask 를 false 로 설정해야 함. 그렇지 않으면 mask 에 의해서도 제약조건이 걸리기 때문에 제약조건이 겹치거나 충돌하다.

- firstView.translatesAutoresizingMaskIntoConstraints = **false**

<img width="794" alt="스크린샷 2019-04-09 오후 4 31 39" src="https://user-images.githubusercontent.com/38423205/55786423-27a02100-5aef-11e9-82e2-5cd5ebcfa475.png">
