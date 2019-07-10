---
layout: post
title:  "Swift API Design Guidelines"
date:   2019-07-10
excerpt: "주석 , 변수 네이밍 등 Swift에 최적화된 Design Guideline 을 정리하자.
"
tag:
- iOS
- Swift
comments: true
---

# Swift API design guidelines

#### 축약하지 말고 길더라도 명확하도록 쓰자

###함수 주석규칙

- 하는일 - 될 수 있으면 function의 기능을 한 줄로 요약

- 파라미터의 역할 - 이 파마미터를 가지고 무었을 할 것 인지

- 리턴의 의미 -



### 네이밍

- 함수를 읽을 때 (외부파라미터) 읽는사람이 애매하지 않도록 (자연스럽게 읽힐 수 있도록)  해야한다. *사용할때도 마찬가지 (내부파라미터)*

![스크린샷 2019-07-10 오전 11 11 55](https://user-images.githubusercontent.com/47776915/60935093-b184a380-a303-11e9-90e0-e73ee93df142.png)

![스크린샷 2019-07-10 오전 11 12 56](https://user-images.githubusercontent.com/47776915/60935102-b9444800-a303-11e9-94a6-7c9c16593b9b.png)



- 중복되는 의미가 되는 네이밍 지양

![스크린샷 2019-07-10 오전 11 25 01](https://user-images.githubusercontent.com/47776915/60935602-610e4580-a305-11e9-84b6-64ff52ccbca6.png)

![스크린샷 2019-07-10 오전 11 24 54](https://user-images.githubusercontent.com/47776915/60935614-6cfa0780-a305-11e9-9d19-cd4ac4de7828.png)



- 타입보다는 역할이나 의미에 우선순위

![스크린샷 2019-07-10 오전 11 29 17](https://user-images.githubusercontent.com/47776915/60935781-ff9aa680-a305-11e9-96f9-702b65480ab2.png)

![스크린샷 2019-07-10 오전 11 29 10](https://user-images.githubusercontent.com/47776915/60935783-ff9aa680-a305-11e9-8903-3b2a5ec8f8a6.png)



- 목적이나 의도하는 바가 애매모호한 타입들( `Any`, `AnyObject`, 혹은 `Int` `String` 같은 기본타입들 ) 사용 할 때에는 생략을 지양하고 의도하는 바를 더 명확하게 해야한다.

![스크린샷 2019-07-10 오전 11 33 26](https://user-images.githubusercontent.com/47776915/60935979-910a1880-a306-11e9-94aa-3dd89b768ed9.png)

![스크린샷 2019-07-10 오전 11 33 19](https://user-images.githubusercontent.com/47776915/60935980-91a2af00-a306-11e9-94df-979286f83f5d.png)
