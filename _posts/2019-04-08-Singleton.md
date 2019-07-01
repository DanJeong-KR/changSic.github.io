---
layout: post
title:  "Singleton Pattern"
date:   2019-04-08
excerpt: ""
tag:
- iOS
- DesignPattern
comments: true
---

## Singleton

* 특정 클래스의 인스턴스에 접근할 때 항상 동일한 인스턴스만을 반환하도록 하는 설계 패턴

* 한 번 생성된 이후에는 프로그램이 종료될 때까지 항상 메모리에 상주

* 어플리케이션에서 유일하게 하나만 필요한 객체에 사용

* UIApplication, AppDelegate 등



### iOS 에서 Singleton Pattern 으로 구현된 객체들

---

**let** screen = UIScreen.main

**let** userDefaults = UserDefaults.standard

**let** application = UIApplication.shared

**let** fileManager = FileManager.default

**let** notification = NotificationCenter.default

---



### Singleton 객체 선언하기

---

**class** SingletonClass {

​    *// 타입 프로퍼티 (전역변수) -> 한번 생성된 이후에는 프로그램이 종료될 때까지 메모리에 상주함.*

  **static** **let** shared = SingletonClass() *// 자기 자신의 인스턴스를 저장.*

**private** **init**() {} *// init 에 private 으로 외부에서 초기화 못시키게 함으로써 싱글톤을 구현!*

  **var** x = 0

}

---

### static keyword

* Type Property (인스턴스 프로퍼티와 다른점 + 의미.)
  * You can also define properties that belong to the type itself, not to any one instance of that type. There will only ever be one copy of these properties, no matter how many instances of that type you create. These kinds of properties are called *type properties*.
  * universal to *all* instances of a particular type, such as a constant property that all instances can use

### static 으로 type property 의 특성을 사용하지 않으면

* 객체의 사용을 강제로 하나만 존재하게 할 수 없네.
* 인스턴스를 초기화 하는 것 자체를 막으려면
* 타입 프로퍼티로 객체에 접근하고 초기화하는 방법 뿐이네.
* => static 키워드로 타입프로퍼티를 사용해서 private init 을 객체 내부에서 한번 초기화한 shared 인스턴스( Singleton 의 유일한 객체 ) 를 유일한 인스턴스로 가져서 Singleton Pattern을 구현


Q **init 앞에 private 키워드를 없애서 싱글톤 객체뿐만 아니라 해당 클래스가 다른 객체도 생성할 수 있게 사용하는 예시도 있을까? 그럴거면 객체에 하나의 인스턴스만 생성해서 사용하는 싱글톤 객체의 사용 목적에 어긋난다고 생각하는데**
* 하나 이상은 굳이 있을 필요가 없어. 그런데 니 맘은 다를 수도 있으니 쓸려면 써라.굳이. 막을 필요는 없다. 중요한 문제가 아니라서 굳이 집중할 필요가 ..
* priviate 붙어있는 싱글톤
    * UIApplication
* 안붙어 있어서 여러 인스턴스도 생성할 수 있는 싱글톤
    * UserDefaults, NotificationCenter 등등.
