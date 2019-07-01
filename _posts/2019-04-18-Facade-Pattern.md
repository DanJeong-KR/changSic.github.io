---
layout: post
title:  "The Facade Design Pattern"
date:   2019-04-18
excerpt: ""
tag:
- iOS
- DesignPattern
comments: true
---


# The Facade Design Pattern
* 복잡한 하위 시스템에 대한 하나의 interface 를 제공한다.
* 사용자에게 여러 클래스들이나 API 들을 노출하지 않고 오직 하나의 통일된 간단한 API 만 노출한다.
<img width="700" alt="스크린샷 2019-04-17 오후 8 45 18" src="https://user-images.githubusercontent.com/38423205/59762418-3155ba00-92d2-11e9-9b29-f0d831148b4e.png">

* 이 패턴은 많은 수의 클래스로 작동하는, 특히 그게 사용하고 이해하기 어려울 때 이상적이다.
* 코드를 **인터페이스**와 내가 **숨긴 클래스들**의 실행으로부터 분리시킨다.


<img width="1008" alt="스크린샷 2019-04-17 오후 8 59 47" src="https://user-images.githubusercontent.com/38423205/59762449-416d9980-92d2-11e9-939f-8c55f6b4c9cd.png">

* LibraryAPI 가 인터페이스 / PersistencyManager, HTTPClient 가 숨긴 클래스들.
* 사용자는 LibraryAPI 만으로만 접근해서 복잡한 내부 PersistencyManager, HTTPClient 가 어떻게 돌아가는지 알 필요가 없다.
* **LibraryAPI만 외부 코드에게 노출되고** PersistencyManager, HTTPClient 의 복잡한 부분은 숨겨진다
 * 이 숨겨짐 을 구현할 때 **access control**(private) 같은 것들을 꼭 잘 사용해야 함을 유의
