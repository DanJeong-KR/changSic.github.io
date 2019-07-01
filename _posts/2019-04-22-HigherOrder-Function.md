---
layout: post
title:  "Higher-Order-Function"
date:   2019-04-22
excerpt: ""
tag:
- Swift
- Higher-Order-Function
comments: true
---

### Higher-Order-Function 이란?
* 하나 이상의 함수를 인자로 취하는 함수
* 함수를 결고로 반환하는 함수
* 이를 만족시키기 위해서는 함수가 해당 언어에서 First-Class(일급 객체) 이어야 한다.


### 1급 객체가 되려면?
* 변수나 데이터에 할당할 수 있어야 한다.
>  let returnValue = function(firstClassCitizen)
* 객체의 인자로 넘길 수 있어야 한다.
* 객체의 리턴값으로 리턴할 수 있어야 한다.
> func function(_ parameter: @escaping ()->()) -> (()->()) {
return parameter
}

Collection Type 에서
Swift 가 제공해주는 고차함수들
* forEach
  - 컬렉션의 각 요소(Element)에 동일 연산을 적용하며, 반환값이 없는 형태
* map 
  - 컬렉션의 각 요소(Element)에 동일 연산을 적용하여, 변형된 새 컬렉션 반환
* filter 
  - 컬렉션의 각 요소를 평가하여 조건을 만족하는 요소만을 새로운 컬렉션으로 반환
* reduce 
  - 컬렉션의 각 요소들을 결합하여 단 하나의 타입을 지닌 값으로 반환.
  - e.g. Int, String 타입
* flatMap  compactMap
  - 중첩된 컬렉션을 하나의 컬렉션으로 병합 
* compactMap
  - 컬렉션의 요소중 옵셔널이 있을 경우 제거 
  - (flatMap으로 사용하다가 Swift 4.1 에서 compactMap 으로 변경됨)


forEach
* 함수기 때문에! break 키워드 같은거 for 문에서 썻던거 쓸 수 없어! return 으로 control flow 해야 한다.
* 반환값이 없어!

map
* forEach 와 같지만 **반환값이 있는 것.**

fill
* 조건을 만족하는 요소만 **새로운 컬렉션** 으로 나온다.

reduce
* 컬렉션의 각 요소들을 결합하여 단 하나의 타입을 지닌 값으로 반환
> let sum1to100 = (1...100)
  .reduce(0) { (sum: Int, next: Int) in
    return sum + next
  }
// 첫 매개변수 0 은 초기값,

compactMap
> let optionalStringArr = ["A", nil, "B", nil, "C"]
print(optionalStringArr.compactMap { $0 })
// 결과 ["A", "B", "C"]

flatMap
> let nestedArr = [[1, 2, 3], [1, 5, 99], [1, 1]]
print(nestedArr.flatMap { $0 })
// 결과  [1, 2, 3, 1, 5, 99, 1, 1]


### 고차함수 연습하기
* immutableArray 배열의 각 인덱스와 해당 인덱스의 요소를 곱한 값 중
* 홀수는 제외하고
* 짝수에 대해서만 모든 값을 더하여 결과 출력

> let immutableArray = Array(1...40)
> print(immutableArray.enumerated().map{ $0 * $1 }.filter
> { return $0 % 2 == 0 }.reduce(0) { $0 + $1 })
