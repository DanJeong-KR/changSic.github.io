---
layout: post
title:  "Status Bar - 상태바 설정하기"
date:   2019-05-28
excerpt: ""
tag:
- iOS
- Status Bar
comments: true
---


### Status Bar
<img width="4448" alt="StatusBar" src="https://user-images.githubusercontent.com/38423205/58478236-89484780-8190-11e9-93ee-b298aee99c36.png">


Status Bar
*	Container 일 경우
	*	내비게이션 컨트롤러에서 내비게이션 스택에 있는 자식(child) 들의 스타일을 모두 통일 시켜준다
*	Content 일 경우
	*	preferredStatusBarStyle
		*	상태바의 글자 숫자들 색 변경
	*	prefersStatusBarHidden
		*	상태바 없어지게 할 수 있는
	*	preferredStatusBarUpdateAnimation
		*	상태바가 변경되면 애니메이션 넣는 속성
	*	prefersHomeIndicatorAutoHidden
		*	아이폰 아래에 홈버튼 사용하지 않을 때 없어지게 만드는 속성
*	[예제 프로젝트](https://github.com/changSic/Task/tree/master/Week13/StatusBarAndHomeIndicatorExample%20(Starter))
