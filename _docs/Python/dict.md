---
title: 8. 딕셔너리
category : Python
order: 13
layout: default
comments: true
---

## Dictionary

이번에는 새로운 개념을 도입해보자!! 바로 딕셔너리이다. 영어로 딕셔너리는 무슨 뜻인가?? **사전** 이라는 뜻이다. 이 딕셔너리를 사용하는 이유는 여러 정보를 하나의 묶음으로 묶기 위해서 사용된다.

우리가 지금가지 배운 지식으로 메이플스토리 캐릭터를 표현한다고 생각해보자. name, level과 같은 정보들을 아래와 같은 변수들을 선언함으로서 나타낼 수 있었지만 이 변수들은 다 떨어져있기 때문에 이 전체를 묶을 수는 없었다.

```python
name = "타락파워전사"
job = "궁수"
level = 13
...
```

하지만 Dictionary를 이용한다면 저런 **정보들을 하나의 묶음으로 나타낼 수 있다.**

## 무엇인가??

자 아래에 있는 코드가 바로 딕셔너리이다. 딕셔너리는 어떤 객체의 특성들과 값들을 담고있는 변수이다. 간단하게 이야기하면 **"너 이름이 뭐니?"** 라고 하면 바로 **"내 나이는 20살이야"** 라고 바로 이야기 할 수 있는 것 처럼, 모든 객체는 각자의 고유의 특성과 값을 갖고있다.

예를 들어서 **사과의 색:빨간색**, **재학중학교이름:국민대학교**, **미팅한횟수:17** 이런식으로 각각의 값들을 **특성:값** 형태로 나타낼 수 있는데 이를 바로 **key:value** 형식이라고 한다.

딕셔너리는 이런 key:value형식을 기반으로 사용되는데, 아래와 같은 코드를 보면 바로 이해가 가능할 것이다. 예제는 메이플 스토리 캐릭터의 정보에 대한 딕셔너리이다.

```python
user = {
  "name":"타락파워전사",
  "job":"궁수"
  "level":13,
  "hp":550,
  "mp":240,
  "items":["파란포션","소가죽","토비","나뭇가지"]
}
```

## 사용방법

#### 선언하기

딕셔너리를 사용하는 방법은 간단하다. 아래와 같이 **"key"와 value를 :로 이어주면** 되는데, 절대로 Dictionary 안에 같은 key가 1개 이상 존재할 수 없다. 즉 무조건 다른 key들을 사용해야한다.

```python
dic = {
  "key1":value,
  "key2":value,
  ...
}
```

value에는 어떤 값들이든 다 들어갈 수 있다. int, str, bool, list, 심지어 딕셔너리도 들어갈 수 있다. 맨 아래 예제를 보면 어떤 형식으로 사용될 수 있는지 바로 알 수 있다.

#### 값을 가져오기

그럼 값을 가져오려면 어떻게 해야하는가?

[]를 사용해소 오른쪽과 같이 key를 넣어준다면 이에 맞는 value를 넘겨준다. : **dic["key"]**

```python
print(user["name"])  #타락파워전사
print(user["level"])  #13
print(user["items"])  #["파란포션","소가죽","토비","나뭇가지"]
```

## 최종 예제

나의 정보를 Dictionary를 이용해서 표현해보자!!

```python
junseong = {
  "age":16,
  "name":"Junseong",
  "male":True,
  "favorite":["apple","banana","orange"],
  "address":{
    "Country":"South Korea",
    "State":"Kyeong-gi",
    "City":"Koyang"
  },
  "families":[
  {
    "type":"mother",
    "name":"Yunha Kim",
    "age":40
  },
  {
    "type":"father",
    "name":"Dohyeon Kim",
    "age":40
  },
  {
    "type":"sister",
    "name":"Domin Kim",
    "age":40
  },
  ]
}
```
