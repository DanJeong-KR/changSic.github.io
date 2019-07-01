---
layout: post
title:  "구글 검색 스마트하게 하자!"
date:   2019-04-10
excerpt: ""
tag:
- Tip
comments: true
---


### 구글 검색 특징
  * 영어 대소문자는 구분X
  * 단어의 순서는 영향을 줌

### 키워드를 넣어서 검색조건 추가하기
**site:[url]**
* http site:w3schools.com -> http 라는 검색어를 w3schools.com 사이트 내에서만 검색
* http site:org -> http 라는 검색어를 *.org 사이트에서만 검색.

**intitle:[keyword] , intext:[keyword]**
* iOS site:org intitle:swift -> iOS 검색 결과중 swift 가 반드시 제목에 포함되고 .org 사이트에 해당하는 링크만 검색
* iOS intext:objective-c -> iOS 검색 결과중 본문에 objective-c 가 들어간 경우만 검색

**filetype:[extension]**
* baseball filetype:pdf -> baseball 검색 결과 중 pdf 파일 확장자와 관련된 것만 출력

**"Exact Phrase"**
* "사느냐 죽느냐 그것이 문제로다" -> 이 문장과 정확히 일치하는 문장이 있는 문서만 검색.

**[keyword] ~or~ [keyword]**
* piano or guitar -> 피아노 또는 기타에 대한 검색 결과

**-[keyword] 지정 키워드 관련 결과 ~제거~**
* salsa -dancing -> salsa 에 대한 결과 중 dancing 과 관련된 결과 제거.

**+[keyword] 지정키워드 ~필수 포함~**
* 애플 +아이폰 -> 애플에 대해 검색하고 아이폰 키워드 필수 포함
