---
layout: post
title:  "@IBDesignable / @IBInspectable"
date:   2019-04-18
excerpt: ""
tag:
- iOS
comments: true
---

### @IBDesignable
 - 코드로 작성한 내용을 런타임이 아닌 컴파일 타임에 스토리보드에서 미리 렌더링하여 볼 수 있도록 해주는 키워드

### @IBInspectable
 - 스토리보드의 Attributes Inspector에 원하는 프로퍼티 항목을 추가해 설정할 수 있도록 하는 키워드
 - 반드시 타입을 지정(Type Annotation)해주어야 함
 - 프로퍼티 옵저버 또는 계산 프로퍼티를 이용해 변경사항을 즉시 확인 가능
 - Inspector에서 설정한 값은 User Defined Runtime Attributes에 반영됨


### 사용하기
<img width="459" alt="스크린샷 2019-04-18 오후 2 24 37" src="https://user-images.githubusercontent.com/38423205/56338726-2ef9b580-61e6-11e9-9617-f07c2be541ed.png">

* @IBInspectable
  * **어트리뷰트 인스펙터에** 내가 정의한 변수가 생김!
  *  <img width="261" alt="스크린샷 2019-04-18 오후 2 27 34" src="https://user-images.githubusercontent.com/38423205/56338724-2e611f00-61e6-11e9-97a6-64e50ab93031.png">
  * **Identity 인스펙터에** User Defined Runtime Attributes 에도 나옴
  * <img width="263" alt="스크린샷 2019-04-18 오후 2 27 48" src="https://user-images.githubusercontent.com/38423205/56338723-2e611f00-61e6-11e9-88bb-00eef35d56d7.png">


* @IBDesignable
  * run 해서 시뮬레이터를 실행시키지 않아도 바로바로 스토리보드에서 확인 가능
  * Corner Radius 20 으로 변경하면 스토리보드에서 바로 적용됨
  * <img width="164" alt="스크린샷 2019-04-18 오후 2 27 25" src="https://user-images.githubusercontent.com/38423205/56338725-2e611f00-61e6-11e9-8209-10a572abcc24.png">
