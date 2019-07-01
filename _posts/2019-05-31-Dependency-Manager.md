---
layout: post
title:  "Dependency Manager"
date:   2019-05-31
excerpt: "CocoaPods , Carthage 사용방법"
tag:
- iOS
- Dependency Manager
- CocoaPods
- Carthage
comments: true
---

<img width="3780" alt="Dependency Manager" src="https://user-images.githubusercontent.com/38423205/58967112-8253b180-87ee-11e9-88b5-40dffb5b5ca9.png">
### [Dependency Manager 마인드맵 보기](https://github.com/changSic/Task/files/3257761/Dependency.Manager.pdf.pdf)



### 마인드맵의 계층구조
<html><head><title>iOS</title></head><body><ol><li>Dependency Manager<ol><li>CocoaPods<br>링크: <a href="https://cocoapods.org/">https://cocoapods.org/</a><ol><li>pod 파일 만들고 pod 파일 편집하기</li><li>CocoaPods 설치하기</li><li>i 누르고 편집에서 쓸 pod 추가하고</li><li>추가한 pod 설치하기 (추가한 라이브러리 설치)</li><li>Xcode project 파일이 아니라 workspace 로 사용해야 한다</li></ol></li><li>Carthage<br>링크: <a href="https://github.com/Carthage/Carthage">https://github.com/Carthage/Carthage</a><ol><li>Carthage 설치하기<ol><li>Carfile 생겨있음</li></ol></li><li>Cartfile 편집해서 라이브러리 추가하기</li><li>추가한 라이브러리를 설치하기</li><li>xcode project 에서 Build Phases 의 Link Binary With Libraries 로 가서</li><li>Cartfile 에 설치한 Framework 를 xcode project 에 추가하기</li><li>+ 버튼 누르고 New Run Scrip Phase 들어가서</li><li>Shell 과 input Files 부분 수정하기<ol><li>Shell<ol><li>/usr/local/bin/carthage copy-frameworks</li></ol></li><li>Input Files<ol><li>$(SRCROOT)/Carthage/Build/iOS/추가할 라이브러리 이름.framework</li></ol></li></ol></li></ol></li></ol></li></ol></body></html>
