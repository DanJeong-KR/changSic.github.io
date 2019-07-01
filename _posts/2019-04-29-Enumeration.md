---
layout: post
title:  "Enumerations - 열거형"
date:   2019-04-29
excerpt: ""
tag:
- Swift
- Enum
comments: true
---

### Enumerations

* An enumeration defines a common type for a group of related values and enables you to work with those values **in a type-safe way**  within your code.

* enumeration cases can specify **associated values** of any type to be stored along with each different case value


### enum cases 반복문에서 사용하기
* CaseIterable 프로토콜을 enum 이 채택하면 반복문에서 사용할 수 있다.
<img width="901" alt="스크린샷 2019-04-29 오후 3 51 01" src="https://user-images.githubusercontent.com/38423205/56895668-b4257a00-6ac4-11e9-8a9f-662e0633bdd0.png">


### Raw values
* Raw values can be strings, characters, or any of the integer or floating-point number types.
* Each raw value **must be unique** within its enumeration declaration.
<img width="684" alt="스크린샷 2019-04-29 오후 5 38 35" src="https://user-images.githubusercontent.com/38423205/56895667-b38ce380-6ac4-11e9-9c9f-f1c57b815e4e.png">

### enum 객체 내부에서 값을 변화시키려면?  Mutating
<img width="975" alt="스크린샷 2019-04-29 오후 9 05 57" src="https://user-images.githubusercontent.com/38423205/56895665-b38ce380-6ac4-11e9-9784-c6ff8e4e5320.png">
