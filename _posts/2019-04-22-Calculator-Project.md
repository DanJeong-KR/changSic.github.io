---
layout: post
title:  "iOS 계산기 만들기 Part 1"
date:   2019-04-22
excerpt: ""
tag:
- iOS
comments: true
project: true
---

### 구현 참고사항
* displayLabel 에는 2 + 3 / 4 와 같이 여러 개의 표현식이 출력되지 않고 결과창에는 항상 숫자만 표현
* 곱하기(×)와 나누기(÷)는 control + command + spacebar를 눌러서 수학 기호를 사용해야 함
* 2 + 3 * 4를 하면 2 + (3 * 4) = 14가 되는 게 아니라 (2 + 3) * 4 와 같이 항상 누른 순서대로 연산
* 2 + =  순으로 누르면 현재 displayLabel에 표현된 숫자인 2가 더해져 2 + 2 = 4 와 같이 동작. 단, 다시 한 번 = 를 누르면 더 이상 계산되지 않음
* 2 + + + x - 3 = 순으로 누르면 최종적으로 - 연산자가 적용되어 2 - 3 = -1
* 등호(=)를 눌러 계산 결과가 나온 뒤 연산자를 누르지 않고 바로 숫자를 입력하면
  기존의 값은 초기화되고 다시 처음부터 시작

### 테스트 케이스
* 12 = 3          => 결과: 3  -  12는 초기화 되고 최초에 3을 누른 것부터 다시 시작
* 12 + 3 = + 4 =  => 결과: 19 -  12 + 3 + 4 = 19
* 12 + 3 + + - +  => 결과: 15 -  이후에 계산할 연산자만 바뀌고 숫자는 고정
* 12 + - x / 3 =  => 결과: 4  -  마지막으로 누른 연산자(/)로 연산. 12 / 3 = 4
* 12 + =          => 결과: 24 -  12 + 12 = 24
* 12 + = = =      => 결과: 24 -  12 + 12 = 24,  등호(=)는 이전 연산자에 대해 한 번만 계산
* 12 +-*/ +-*/    => 결과: 12  - 연산자를 막 바꿔가면서 눌렀을 때 이상 없는지 체크
* 1 * 2 + 3 / 2 - 1 => 결과: 1.5
* 숫자를 큰 수나 작은 수 음수로 놓고 여러가지 계산해보기

### 1. 버튼과 라벨 Action Method 연결하기
<img width="957" alt="스크린샷 2019-04-23 오후 5 05 15" src="https://user-images.githubusercontent.com/38423205/56575709-69f25380-6601-11e9-9da4-bc02dfec9864.png">

### 2. 입력된 버튼 종류에 따른 수행 명령 구분하기
* 작업해야할 것들을 큰 그림으로 그려서 enum 으로 만들기.
<img width="531" alt="스크린샷 2019-04-23 오후 5 09 45" src="https://user-images.githubusercontent.com/38423205/56575708-69f25380-6601-11e9-951a-46b8fb64586b.png">
  * 이렇게 작업을 크게 나누고 버튼에 따른 수행명령을 구분한다.

* 버튼에 따라서 구분하기.
<img width="624" alt="스크린샷 2019-04-23 오후 5 11 29" src="https://user-images.githubusercontent.com/38423205/56575707-69f25380-6601-11e9-81e1-d8639953ae01.png">



### 3. 입력한 버튼의 title 을 DisplayLabel 에 출력하기.
* displayValue 라는 연산 프로퍼티를 정의해서 DisplayLabel 에 직접 접근하지 않고 DisplayLabel 을 관리한다.
<img width="640" alt="스크린샷 2019-04-23 오후 5 25 52" src="https://user-images.githubusercontent.com/38423205/56575706-6959bd00-6601-11e9-97dc-a55d69147017.png">


### 4. addDigit 기능 구현하기
( 숫자 버튼을 눌렀을 때 DisplayLabel 에 숫자가 하나씩 추가되는 기능 )
performCommand 메소드를 정의한다.
<img width="887" alt="스크린샷 2019-04-23 오후 5 33 34" src="https://user-images.githubusercontent.com/38423205/56575704-6959bd00-6601-11e9-9a5f-908c31b762e5.png">

### 5. addDigit 기능 개선하기
( 숫자 1을 누르면 1 이 입력되어야 하지만 10 이 DisplayLabel 에 표현되는 문제와 숫자 길이가 너무 길면 화면에 모두 표현되지 못하므로 숫자 길이를 제한하는 기능 )
* shouldResetText 라는 flag 를 정의해서 숫자 버튼이 처음으로 입력될 때를 알려주게 만들기
<img width="528" alt="스크린샷 2019-04-23 오후 5 41 49" src="https://user-images.githubusercontent.com/38423205/56575703-6959bd00-6601-11e9-9bbc-3ad081d4c754.png">
* 첫 문자가 아닐때만 문자열 뒤에 추가해주고, 길이를 제한하는 로직
<img width="881" alt="스크린샷 2019-04-23 오후 5 42 53" src="https://user-images.githubusercontent.com/38423205/56575702-6959bd00-6601-11e9-8ae4-267feed6a701.png">


### 6. 사칙연산 기능 구현하기
* 계산한 값을 저장하는 변수와 연산자 정보를 저장할 변수
<img width="538" alt="스크린샷 2019-04-23 오후 5 54 20" src="https://user-images.githubusercontent.com/38423205/56575701-68c12680-6601-11e9-9ad1-1c798799491c.png">

* 새로운 값이 들어오면 계산을 수행하는 calculate 함수 구현
<img width="675" alt="스크린샷 2019-04-23 오후 5 55 01" src="https://user-images.githubusercontent.com/38423205/56575700-68c12680-6601-11e9-81d4-7104c3f3e956.png">

* performCommand 에 구현한 기능 적용하기.
<img width="862" alt="스크린샷 2019-04-23 오후 6 00 25" src="https://user-images.githubusercontent.com/38423205/56575696-68c12680-6601-11e9-8b07-09a83f5bdd08.png">


### 7. 소수점 자리수 제한하는 기능 추가하기
* 문자열을 받아서 자리수 제한하고 문자열로 돌려주는 함수 limitFractionDigits 추가
<img width="613" alt="스크린샷 2019-04-23 오후 7 40 42" src="https://user-images.githubusercontent.com/38423205/56575695-68289000-6601-11e9-92d0-ce1926325a09.png">



### 8. clear 버튼과 = 버튼 구현하기
<img width="537" alt="스크린샷 2019-04-23 오후 7 50 21" src="https://user-images.githubusercontent.com/38423205/56575694-68289000-6601-11e9-890d-4926d81ad272.png">
