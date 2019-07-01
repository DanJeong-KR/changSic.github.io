---
layout: post
title:  " [iOS] CollectionView 마인드맵으로 정복하기! "
subtitle:
categories: iOS
tags: note
---

<img width="4249" alt="collectionViewMind" src="https://user-images.githubusercontent.com/38423205/58956101-807ef380-87d8-11e9-99d8-6703685fca1f.png">

###[마인드맵 보기](https://github.com/changSic/Task/files/3257170/CollectionViewPdf.pdf)


### UICollection View
<html><head><title>iOS</title></head><body><ol><li>UICollection View<ol><li>선언</li><li>Layout 과 Content를 나눈다</li><li>Layout<ol><li>Flow Layout</li><li>Section Layouyt</li><li>UICollectionViewDelegateFlowLayout 프로토콜이란 게 있습니다.<ol><li>UICollectionViewDelegate 를 상속받은 아이라서 UICollectionViewDelegate를 채택할 필요가 없어진다</li><li>Item Size</li><li>Section Inset</li><li>Line Spacing</li><li>Interitem spacing</li><li>Header / Footer Size</li></ol></li><li>Layout Metrics</li></ol></li><li>Cell 계층</li><li>스토리보드 에서 CollectionView<ol><li>Collection View 의 cell 에서의 사이즈가 런타임에서 나온다. cell 의 custom size 는 디자인 시에 활용</li><li>셀의 크기가 커지면 어떤 식으로 표현될까 알아보려고  아이템수를 늘려서 스토리보드에서 확인할 수 있다.</li><li>오른쪽 스크롤에서 Indicator 의 위치도 조절가능</li></ol></li><li>코드로 작업할 때<ol><li>ViewController 에서<ol><li>UICollectionView 초기화 하기<ol><li>collectionView 는 init 에 2개 파라미터 있는것 써야한다.</li><li>두번째 파라미터 collectionViewLayout 에는 UICollectionViewFlowLayout 인스턴스를 넣는다</li><li> lazy 키워드를 활용하자</li></ol></li><li>CollectionView 설정하기<ol><li>cell 을 register 하기<ol><li>Custom Cell 이라면 identifier를 타입 프로퍼티로 선언해놓으면 편하네</li><li>header 혹은 footer 가 있다면 supplementaryView 를 register 한다</li></ol></li><li>dataSource 설정</li><li>delegate 설정</li><li>addSubview 하기</li></ol></li><li>FlowLayout 설정하기<ol><li>sectionInset</li><li>minimumInteritemSpacing</li><li>LineSpacing</li><li>itemSize</li><li>headerReferenceSize</li><li>footerReferenceSize</li><li>sectionHeadersPinToVisibleBounds<ol><li>header 혹은 footer 가 스크롤 할 때 고정되는 속성</li></ol></li><li>layout.sectionFootersPinToVisibleBounds </li><li>scrollDirection<ol><li>스크롤 방향 바꾸는 속성</li></ol></li></ol></li><li>Header 와 Footer 설정할래?<ol><li>SupplementaryView 를 register 하기.<ol><li>func register(_ viewClass: AnyClass?, forSupplementaryViewOfKind elementKind: String, withReuseIdentifier identifier: String)</li><li>Cell 이 아니라 View 가 들어간다.</li></ol></li><li>dataSource 에서 메소드 작성해 주어야 한다.<ol><li>kind 로 header 인지 footer 인지 구별할 수 있다.<ol><li>Header 만들기</li><li>Footer 만들기</li></ol></li></ol></li></ol></li><li>scrollDirection 이 바뀜에 따라 유동적으로 셀 바뀌게 할래?</li></ol></li><li>Cell 에서<ol><li>UI 초기화<ol><li>UICollectionViewCell 은 ContentView 가 기본적으로 있음으로 활용하려면 활용 가능</li></ol></li><li>레이아웃 잡기</li><li>데이터 넣어주는 로직 만들기<ol><li>didSet 으로 하거나</li><li>configure 로직을 만들거나</li></ol></li></ol></li></ol></li><li>예제 프로젝트<br>링크: <a href="https://github.com/changSic/Task/tree/master/Week13/CollectionViewExample%20(starter)">https://github.com/changSic/Task/tree/master/Week13/CollectionViewExample%20(starter)</a></li></ol></li></ol></body></html>
