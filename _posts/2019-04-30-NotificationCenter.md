---
layout: post
title:  "Notification Center"
date:   2019-04-30
excerpt: ""
tag:
- iOS
- Notification Center
comments: true
---


### UINotificationCenter 라는 객체로 이벤트를 받아서 옵저버처럼 사용할 수 있다.
* didSet , willSet 도 프로퍼티 옵저버
* <img width="620" alt="스크린샷 2019-04-30 오전 11 34 15" src="https://user-images.githubusercontent.com/38423205/56966025-52830f80-6b99-11e9-90a9-11b159d65503.png">


### addObserver(observer: Any, selector: Selector, name: NsNotification.Name?, object: Any?)
* observer: 옵저버를 등록할 객체
* selector: 지정한 알림이 발생했을 때 반응할 메서드
* name: 알림을 구분하기 위한 이름
* object: 특정 객체를 지정하면 그것을 통해 발생하는 알림만 등록, nil이면 전체

### userInfo 를 통해 keyboard 객체 정보를 받을 수 있다.
<img width="795" alt="스크린샷 2019-04-30 오전 11 46 40" src="https://user-images.githubusercontent.com/38423205/56966024-52830f80-6b99-11e9-8a76-1c5742da4c60.png">
* 시스템에서 키보드가 올라올 때 자동으로 호출되는 UIResponder 를 통해 Notification 을 받음.

* UIApplication 에도 기본적으로 제공하는 Notification 이 있다.
<img width="809" alt="스크린샷 2019-04-30 오후 12 02 49" src="https://user-images.githubusercontent.com/38423205/56966022-52830f80-6b99-11e9-8289-a7a7ba4de832.png">


### 등록한 옵저버를 제거해주어야 한다.
* 추가한 observer 는 해당 컨트로럴 가 없어질때 지워주어야 한다. 그렇지 않으면 계속 메모리에 남아 있다
* post 는 신경쓸 필요 없고.
<img width="644" alt="스크린샷 2019-04-30 오후 1 38 21" src="https://user-images.githubusercontent.com/38423205/56966021-51ea7900-6b99-11e9-8ce5-32aa16f60c89.png">


### 탭바 컨트롤러가 있고 서로다른 뷰 컨트롤러에서 Notification 을 보내려고 할 때 생기는 문제
* SecondViewController 가 아직 로드 되지 않아 탭바로 한번 클릭하고 나서야 Notification 을 받는데 ViewWillDisappear 메소드로 해결가능 하다.
* SecondVC 가 load 되고 나서 FirstVC 의 ViewWillDisappear 가 수행되기 때문.
=> 라이프 사이클 코드의 정확한 시점들을 알아두자.
