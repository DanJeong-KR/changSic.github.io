---
layout: post
title:  "Server 와 Client"
date:   2019-04-13
excerpt: ""
tag:
- iOS
- 특강
comments: true
---

## 이재성 강사님 특강

### Server and Client

서버 (Server)
* 클라이언트에게 네트워크를 통해 정보나 서비스를 제공하는
  * 서버컴퓨터(ServerComputer) 또는 서버프로그램(ServerProgram)

클라이언트
* 서버가 제공하는 서비스를 요청 (Request) 하고
* 서비스 요청을 위해 필요 인자(Parameter) 를 서버가 원하는 방식에 맞게 제공하며
* 서버로부터 반환되는 응답(Response) 에 사용자에게 적절한 방식으로
* 표현(UI) 하는 기능을 가진 프로그램 이나 시스템
  * e.g.
    * 앱
    * 인공지능 스피커도 하나의 클라이언트


HTTP 를 통해 정보를 요청하고 응답받는
<img width="583" alt="스크린샷 2019-04-13 오후 1 26 13" src="https://user-images.githubusercontent.com/38423205/56101858-3eb59780-5f63-11e9-9b86-f01fda88bb71.png">


NS -> NextStyle 의 약어였구나

마크업 언어
* HTML : 정적
* CSS : Cascading(종속적이다.) Style Sheet
프로그래밍 언어
* JavaScript : 마우스 올려놓으면 UI 생기네?
  * 웹사이트의 동적인 컨트롤

프로그래밍 언어는 마크업 언어를 컨트롤 할 수 있음.


## API / JSON and XML
Website 모든 데이터(수백 ~ 수천 라인의 HTML/CSS/JS 코드 Response ) 앱 브라우저로 넘김

Mobile Native Application
* UI 는 모두 구현되 있음
  * 작은 데이터 조각만 필요
  * <img width="300" alt="스크린샷 2019-04-13 오후 3 03 35" src="https://user-images.githubusercontent.com/38423205/56101870-51c86780-5f63-11e9-8d91-e356d4a19597.png">


### XML and JSON
XML : 데이터 낭비가 너무 많아 -> JSON 으로 표현하기 시작

JSON : "속성" : "값" 쌍으로 이루어진 **데이터 객체**
* 예시
!<img width="657" alt="스크린샷 2019-04-13 오후 3 10 27" src="https://user-images.githubusercontent.com/38423205/56101882-60af1a00-5f63-11e9-8ee8-99dd63631f88.png">

* 실제 현업에서 (로그인 성공시 ...)
<img width="396" alt="스크린샷 2019-04-13 오후 3 11 49" src="https://user-images.githubusercontent.com/38423205/56101883-63117400-5f63-11e9-8949-af528af0eb8c.png">

* JSON 으로 받은 HTML status code 에 따라 서버의 문제인지 클라이언트릐 문제인지 알 수 있다. (크롬 개발자 도구 에서 확인할 수 있는 것 처럼 native app 에서도 할 수 있는 것.)

REST API
<img width="673" alt="스크린샷 2019-04-13 오후 3 20 56" src="https://user-images.githubusercontent.com/38423205/56101925-a9ff6980-5f63-11e9-9f03-bc2063b28540.png">

[연습할 수 있는 사이트 punkapi](https://punkapi.com/documentation/v2)

[JSON Parsing 해주는 사이트](http://jsonparseronline.com/)

오픈 API 들이 있다.
* 카카오
* 구글
* 페이스북 ...

Wep Application
* 구글 docs

* 웹 프론트엔드 프레임워크
  * Angular.js
  * Vue.js
  * React

7. 하이브리드 앱


### React Native
"Learn Once, write anywhere"

React Native가 iOS / Android 각각의 플랫폼에 맞는 Native UI로 변환 → 결과물 자체는 Native App

### 팀프로젝트 팁 (나중에 발표자료 다시 보자)

프로젝트 사이즈를 정말 작게 만들어야 합니다.
* 일주일마다 **눈에 보이도록**
* 백엔드 작업동안 데이터가 제공되지 않을 때 가상의 데이터라도 만들어서 앱을 만들어야 한다.
  * 백엔드에서 실패할 수도 있음.
* 핵심기능 부터 구현해라
  * 로그인 하는 것들은 나중에 하고~


* 내부  컨텐츠를 같이 준비하기
* 내가 가고싶은 회사의 서비스나 도메인과 유사한 프로젝트로 결정 하세요~

* 데이터 모델링 같이 하기
  * 클라이언트는 언제든 바꿀 수 있지만, 백엔드는 한번 정하면 바꾸기 어려우므로 같이 정하기
  * 변수명 같은 것도 되도록이면 맞추세요. 서로 의사소통 문제가 생길 수도 있음.
