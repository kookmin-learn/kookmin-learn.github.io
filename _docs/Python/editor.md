---
title: 파이썬 에디터 설치하기
category : Python
order: 3
layout: default
comments: true
---
(윈도우를 사용하는 학생이라면 파이썬이 설치되지 않았을 수 도 있다. 이전 문서인 파이썬 설치하기를 보고 오자)

## 아톰이란?

교수님들은 보통 idle3를 사용하시는데 이 강좌에서는 **atom이라는 에디터를 사용할 예정이다**.

아래에 atom의 스크린샷이 나와있는데, 매우 이쁘고 간결하고 강력한 코드 에디터이다. 코잘남, 코잘녀가 되기 위한 첫걸음이기도 하다

![Imgur](http://i.imgur.com/2JW4OzR.png)


### 설치 1단계 : atom 다운로드 & 설치

![Imgur](http://i.imgur.com/gSxQApK.png)

링크로 가서 아톰을 다운로드 받는다 그리고 설치한다 [https://atom.io](https://atom.io)

우분투는 .deb파일을 다운받고, 파일을 눌러서 실행하면 설치된다.


### 설치 2단계 : atom 실행하기

윈도우와 맥은 실행하는것이 어렵지 않을 것이다.

우분투는 프로그램 검색창에서 atom을 검색하면 쉽게 실행할 수 있다.

### 설치 3단계 : script 설치하기
파이썬을 쉽게 실행하려면 script라는 플러그인(패키지)이 필요하다. 그래서 설치를 할건데 매우 쉽다.
맨위에 보면 여러가지 메뉴들이 있다. 아래의 절차를 따라해보자 :)

1. 윈도우 : 상단 File 메뉴 -> Settings -> Install
2. 맥 : 상단 Atom 메뉴 -> Settings -> Install
3. 우분투 : 상단 Edit 메뉴 -> Preferences -> Install

install을 누르면 설치가 되는데 시간이 조금 걸리는데 인내심을 갖고 기다리다보면 설치가 다 될 것이다. 설치가 다 되면 Setting창을 닫아주자.

![Imgur](http://i.imgur.com/jMELoMM.png)

### 설치 4단계 : 사용해보기

이제 실제로 파이썬 파일을 만들고, 파이썬 파일을 실행시켜 보도록하자. 앗 script가 잘 설치되었나 확인도 해볼겸해서 ㅎ

1. 상단 File 메뉴 -> new File -> test.py
2. text.py에 ```print("Hello Atom")``` 작성하기
3. 저장하기(cntl-s)를 누릅니다.
4. 실행하기 (윈도우/우분투 shift-ctrl-b) (맥 cmd-i) 단축키 누르기

![Imgur](http://i.imgur.com/0j4KraA.png)
위와 같은 그림처럼 hello atom이 출력된다면 성공!!! :)

앞으로 파이썬 코드를 작성하고 실행시킬 때, 이렇게 사용하면 된다.
