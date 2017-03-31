---
title: 파이썬 IDE 설치하기
category : Python
order: 3
layout: default
comments: true
---

> Pycharm을 설치하기 이전에 **python 3.x 버전이 설치 되어있어야 합니다.**
> 설치가 되어 있지 않다면, 옆의 파이썬 설치하기 문서를 참조해주시기 바랍니다.

## Pycharm

![Imgur](http://i.imgur.com/y8j9nLY.png)

많은 개발자들이 python을 개발하기 위해서 사용하는 IDE는 단연코 **pycharm** 일것이다. pycharm은 매우 강력하고 많은 기능들을 지원하며, 자동완성 및 여러가지 기능들을 포함한 IDE이다. 우리는 앞으로 이 pycharm을 사용하게 될것입니다.

## 설치하기

#### 맥과 윈도우
파이참 설치 링크 : [https://www.jetbrains.com/pycharm/](https://www.jetbrains.com/pycharm/)

1. **Download Now**를 누르면 어떤걸 다운로드 할지 선택하는 창이 나온다.
2. **Community Edition** 을 선택하면 자동으로 다운로드가 시작된다.
3. 다운로드가 끝나면 눌러서 설치를 하면 끝난다.(그냥 다 next누르면 된다.)

#### 우분투

우분투는 파이참을 터미널을 열어서 코드를 입력해 설치해줘야 한다. **그래도 단 3줄이면 끝나니 조금 수고를 해주시게** 터미널을 열고 아래 3개의 코드를 순서대로 복사 붙여넣기를 해보자!

```shell
sudo add-apt-repository ppa:mystic-mirage/pycharm
```
```shell
sudo apt-get update
```
```shell
sudo apt-get install pycharm-community
```

#### 설치후

0. 파이참을 실행시켜 줍니다.

1. 여기서 그냥 enter 누릅니다
![Imgur](http://i.imgur.com/S2uYmty.png)

2. 여기서도 역시 OK를 가볍게 눌러준다.
![Imgur](http://i.imgur.com/79UeQvd.png)


## 사용법

1. 먼저 이런 화면이 보일것이다. 여기서 Create Project를 눌러준다.
![Imgur](http://i.imgur.com/3HgWz9a.png)

2. 프로젝트의 이름과 어디에 저장할지 정해준다. 나는 **kookmin** 이라는 이름의 프로젝트를 생성했다.
![Imgur](http://i.imgur.com/BuS78bc.png)

3. 짜잔 그러면 이제 프로젝트가 생성되었다. kookmin 폴더에 오른쪽 클릭을 하고, 아래 사진처럼 **New->Python File** 을 누른다.
![Imgur](http://i.imgur.com/RwiISgc.png)

4. 그러면 파일 이름을 쓰라고 했는데 나는 일단 test라는 이름의 **test.py** 파일을 만들었다.
![Imgur](http://i.imgur.com/hgvTHKN.png)

5. 쨘! 파이썬 코드를 작성할 수 있는 공간이 만들어졌다. 그리고 저기에 코드 한줄을 작성해보자 ```print("Hello World")```
![Imgur](http://i.imgur.com/jtcTxEa.png)

6. 이제 저 파일을 실행시키는 방법을 알아보자. **test.py** 에 오른쪽 클릭을 하고, **Run->test** 를 누르면 파일은 실행된다! 아래에 결과가 출력되는것을 볼 수 있다.
![Imgur](http://i.imgur.com/bHhsdbz.png)

7. 그 이후에 계속 실행할때는 아래 사진의 Play버튼처럼 생긴걸 누르면 된다!
![Imgur](http://i.imgur.com/wwFwPqv.png)
