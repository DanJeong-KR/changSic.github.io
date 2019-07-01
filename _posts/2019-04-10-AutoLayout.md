---
layout: post
title:  "AutoLayout"
date:   2019-04-10
excerpt: "AutoLayout 의 개념적인 부분에 대해"
tag:
- iOS
- AutoLayout
comments: true
---

# AutoLayout

뷰에 주어진 제약조건에 따라 뷰의 크기와 위치를 **동적으로** 계산해 배치할 수 있다.



### 외부 또는 내부의 변화에 **동적으로** 반응하여 유저 인터페이스 구성

---

### 외적 변화 요소

* 서로 다른 기기 ( 스크린 크기 )
* 기기 회전
* Split View 로 진입하거나 빠져나올 때
* 등등 더 있을 수 있다.



### 내적 변화 요소

* 앱 내부에서 보여지는 컨텐츠 변화
  * e.g 게임에서 100명 죽이면 나오는 버튼을 오토 레이아웃을 설정해서 내가 원하는 위치에 나올수 있다던지
* 국제화 지원( 텍스트, 날짜와 숫자, RTL 등)
  * e.g 안녕하세요 Hello 글자 길이가 다른것을 동적으로 대응할 수 있다던지
* Dynamic Type 지원 (글꼴 크기)
  * e.g 글꼴에 따라 다른 글자 크기를 대응할 수 있다던지

---



### 유저 인터페이스 구성하는 주요 접근 방식

---

Frame 방식 -> Autoresizing masks -> **AutoLayout**

* Frame 방식
  * 동적인 변화에 대한 유지관리에 많은 노력이 필요
  * 원점 위치와 크기로 영역 계산
  * 가장 유연하며 **빠른 성능!**
    * 성능(속도가) 중요한 경우 Frame 으로 작업해야 겠네. 아래 그림은 AutoLayout 과의 성능 비교
    * <img width="740" alt="스크린샷 2019-04-09 오후 1 47 11" src="https://user-images.githubusercontent.com/38423205/55774534-7c806f00-5ad0-11e9-8e96-f85a5be4dfa1.png">
* AutoLayout 방식
  * 내, 외적 변경 사항에 동적으로 반응
  * Frame 기반에 비해 느린 성능
* [오토레이아웃과 Frame 방식으로 같은 UI 를 구현하는 예제](<https://github.com/changSic/Task/tree/master/Week6/AutoLayout/AutoLayoutExample>)
  * Frame 방식으로 구현할 때 safeAreaInsets 과 UIApplication.shared.statusBarFrame 으로 상태바와 safeArea 의 frame 값 얻어올 수 있다.
    * viewdidload 에서는 safeAreaInset 프로퍼티 사용이 안되네 (아직 로드가 안됨.)
      * *viewWillAppear -> viewWillLayoutSubviews -> viewDidLayoutSubviews -> viewDidAppear*
      * viewWillLayoutSubviews 에서 safeAreaInset 프로퍼티 사용가능*
      * *정확히 말하면 viewWillLayoutSubviews 전에 ViewSafeAreaInsetsDisChanged () 부터 사용가능 한 것.*

---



### AutoLayout 설정하기

---

* 컨트롤 드래그 방식

<img width="890" alt="스크린샷 2019-04-09 오전 11 09 53" src="https://user-images.githubusercontent.com/38423205/55774557-928e2f80-5ad0-11e9-8769-f4a44ff83d31.png">

* Tools 사용하기

<img width="400" alt="스크린샷 2019-04-09 오전 11 14 59" src="https://user-images.githubusercontent.com/38423205/55774565-97eb7a00-5ad0-11e9-8e66-941cd02ba626.png">



* Resolve AutoLayout Issues Tool

  * 에서 missing constraints 추가하는거 는 보통은 쓰지마세요. 원치 않은 제약사항이 걸립니다.



### AutolLayout Attributes

<img width="665" alt="스크린샷 2019-04-09 오전 11 20 35" src="https://user-images.githubusercontent.com/38423205/55774580-acc80d80-5ad0-11e9-8e43-15b8b573fcee.png">



### Contraint 계산을 어떻게 하는지

<img width="906" alt="스크린샷 2019-04-09 오전 11 33 59" src="https://user-images.githubusercontent.com/38423205/55775150-10ebd100-5ad3-11e9-8889-c13926d6df8c.png">

* **기준점이** 중요하다!
  * muliplier : 시작 지점 기준으로 곱하기
  * 기준점에 따라서 값은 계속 달라짐을 주의! 기준점을 잘 설정하는게 중요하네



### Nonambugouous, Satisfiable 특징

* 모호하면 안되고 모든 사항이 만족되어야 한다는 특징.
* 레이아웃을 설정하는 방법은 여러가지가 있다.
  * center 값을 잡아도 되고 가로 길이를 설정해도 되고 등등같은 모양이더라도 제약사항이 다를 가능성이 있다.



### LayoutGuide

* x 시리즈의 노치 디자인과 그 이전버전의 디자인의 레이아웃을 설정하기.

<img width="791" alt="스크린샷 2019-04-09 오후 12 25 07" src="https://user-images.githubusercontent.com/38423205/55775161-1ba66600-5ad3-11e9-9093-5b4e2ebe412d.png">

<img width="944" alt="스크린샷 2019-04-09 오후 12 25 24" src="https://user-images.githubusercontent.com/38423205/55775166-1cd79300-5ad3-11e9-915d-68d7cb5d75c7.png">



### contrain margin 설정하기.

* default 로 상위 뷰 기준으로 약간의 마진이 설정됨.
* 오토레이아웃 툴에서 contrain to margin 버튼 으로 설정가능
* First Item 에서 Relative to margin 버튼 으로 설정가능



### Leading 과 Left 의 차이

* FirstItem 쪽에서 Respect Language direction 버튼
* 아랍과 같은 나라는 leading 이 오른쪽 편
* 삶의 방식이 아예 다르기 때문에
* Left 과 나라와 독립적으로 왼쪽을 표현.



### Proirty

* 우선순위.
* 같은 제약조건일 경우 우선순위가 높은 제약조건으로 실행된다.
* 실선으로 표시됨.



##  Intricsic Content Size

---

* 고유의 컨텐츠 사이즈
  * 컨텐츠를 잘라내거나 줄이지 않고도 온전히 표현할 수 있는 최소한의 공간
  * XCode 에서 버튼이나 라벨은 top 이랑 leading 만 설정해줘도 오류 안난다.  버튼, 라벨 모두 고유의 사이즈가 있기 때문.
* 레이아웃 작업 시 이 사이즈를 통해 제약 조건을 자동 생성하여 적용할 수 있음
* UIView 는 자체 컨텐츠가 없어서 자체 사이즈를 정할 수 없음
  * UIViewNoIntrinsicMetric 이라는데
* 객체별 Intricsic Content Size
  * <img width="893" alt="스크린샷 2019-04-09 오후 3 33 49" src="https://user-images.githubusercontent.com/38423205/55786249-dabc4a80-5aee-11e9-868e-75d74d1df34c.png">



### CHCR

* Intricsic Size 의 값을 기준으로
  * Content Hugging : 더이상 늘어나지 못하도록 **최대 크기 제한**
  * Content Compression Resistance : 더 이상 줄어들지 못하도록 **최소 크기 제한**
  * <img width="764" alt="스크린샷 2019-04-09 오후 3 35 31" src="https://user-images.githubusercontent.com/38423205/55786284-ec055700-5aee-11e9-96e5-ff7ecf93cf3d.png">
  * <img width="901" alt="스크린샷 2019-04-09 오후 3 35 36" src="https://user-images.githubusercontent.com/38423205/55786289-edcf1a80-5aee-11e9-967e-b6499d710192.png">

### Priorty

* 상황에 따라 우선순위를 바꿔서 사용할 수 있다.
* 코드로 우선순위를 바꿔서 특정 상황에 특정 버튼에 애니메이션을 준다던지 할 수 있다.
