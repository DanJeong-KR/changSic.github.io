---
layout: post
title:  "Git과 Mac Terminal 명령어 정리"
date:   2019-04-03
excerpt: "iOS를 공부하면서 필요했던 Git 의 지식과 MacTerminal 명령어를 정리합니다."
tag:
- Git
- Terminal
comments: true
---

## Git

- [Git 이란 무엇인가](https://wodonggun.github.io/wodonggun.github.io/study/Git-%EC%9D%B4%EB%9E%80.html)

## Mac Terminal 명령어, git 명령어 정리.

- ls : 목록 조회
- cd : 경로 이동 / c.g cd ~/Desktop
- pwd : 경로 확인
- 파일
  - touch : 파일 생성
  - cp : 복사
  - mv : 이동
  - rm : 삭제
- vi : 텍스트 에디터 실행
  - <img width="1183" alt="스크린샷 2019-04-08 오후 3 04 32" src="https://user-images.githubusercontent.com/38423205/55704573-69f62f00-5a17-11e9-85a2-f35e9e42b9aa.png">



## vi 텍스트 에디터

vimtutor

* 터미널에서 치면 vi 편집기 튜토리얼 나온다.

쉘 프롬프트에서 (terminal 명령) 에서 빔을 시작하려면

* vim FILENAME <Enter>

<ESC> 를 쓸 때

* 멍령 모드로 돌아가는데 쓰며, 원치 않는 명령이나 완전히 입력되지 않은 명령을 취소하는데 쓰인다.

vim 에서 빠져나가기

* 수정한 내용을 무시한 채로 빠져나가기 <ESC> :q! <Enter>
* 수정한 내용을 저장한 채로 빠져나가기  <ESC> :wq <Enter>



커서 이동

* <— : h
* —> : l
* 위 : k
* 아래 : j
* 또는 화살표

지우기

* 명령모드 커서 위에서 **x**

* 삭제명령 **d** 에 대해서

  *  횟수 - 명령을 몇 번 수행할 지 (옵션, 기본값=1).

     d    - 지우는 명령

     대상 - 아래에 제시된 대상에 대해 명령을 수행

    * 한 단어만 지우고 **dw**
    * 그 줄 끝까지 지우기 **d$** (줄 지우기를 많이 쓰기 때문에 **dd** 라고 하면 줄 전체가 지워짐)
    * e.g. 2dd 라고 하면 2줄 전체가 지워짐

삽입하기

* 명령모드에서 **i**

취소 (UNDO) 명령

* u : 마지막 명령 취소
* U : 커서가 있는 줄 전체를 명령 취소 (한 번에)
* CTRL-R : 앞으로 취소 (앞으로 되돌리기)
