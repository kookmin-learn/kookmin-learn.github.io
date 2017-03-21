---
title: 조건문
category : Python
order: 7
layout: default
comments: true
---

## 조건문이란?
간단하다. "~일때 ~해라"를 생각하면 된다.

어떤 조건일때 어떤 행동을 할지 정해주면된다. **조건문에는 아래와 같은 요소가 필요하다**
1. 조건문 (if 문에 들어가는 조건)
2. 할 행동 (if 문이 성립할 때 실행할 코드들)

```python
if 조건:
  할 행동들
```
**if문 안에서 할 행동들은 Tab키를 눌러서 들여쓰기를 해준다**

예를 들어서 "사과가 0개이면 사과를 다시 사온다"라는 문장은 아래와 같은 코드로 나타 낼 수 있다.
```python
if apple == 0:
  buy_apple()
```

로그인을 할때에는 아이디와 비밀번호가 모두 맞아야 한다.
(아이디가 20171603이고 비밀번호가 junseong123일때 입력받은 id,pw와 비교한다)
```python
if id == "20171603" and pw == "junsong123":
  print("로그인 성공 !!!")
```

## 조건문을 만드는 방법

1. 먼저 비교연산자에 대해서 알아야 한다.
[데이터타입문서 : 비교연산자 섹터](https://codertimo.github.io/Python/datatype/#비교연산자)
2. ```if 조건 :```형식으로 작성한다
3. 밑줄부터 tab을 써서 할 일들을 묶는다
4. Tab이 적용된 코드만 if문 안에 포함되어있는 것이다.

## ```else:``` 아니라면

else는 if문에 들어있는 조건이 맞지 않으면 실행되는 명령어이다.

```python
if id == "20171603" and pw == "junsong123":
  print("로그인 성공 !!!")
else:
  print("로그인 실패 !!")
```

## ```elif 조건문 :``` if문이 틀리고, 조건을 추가할때

if 문이 틀렸는데, 뭔가 조건을 하나 더 걸어보고 싶다. 예를 들어서 비밀번호만 틀렸을때 와 같은 경우말이다. elif에서도 걸리지 않으면 else에서 걸리게 된다.

```python
if id == "20171603" and pw == "junsong123":
  print("로그인 성공 !!!")
elif id== "20171603" and pw != "junseong123":
  print("비밀번호가 틀립니다. !!")
else
  print("등록되지 않은 유저입니다.")
```

## 복수 조건

## and

만약에 name이 준성이고 student_id도 20171603이면 Hi Junseong을 출력하고자 한다. 물론 아래처럼 if문을 곂쳐서 2개를 사용할 수 도 있지만 뭔가 비효율적인 것 같다.

```python
if name =="Junseong":
  if student_id =="20171603":
    print("Hi Junseong")
```

그래서 **그리고 and**  라는 연산자를 활용한다
```python
if name=="Junseong" and student_id =="20171603":
  print("Hi Junseong")
```

## or

그럼 만약에 name이 준성이거나 또는 student_id가 20171603일 때. 즉, 둘중 하나만 성립해도 로그인을 할 때엔 어떻게 하면 될까??

그럴때는 **또는** 이라는 연산자 **or** 을 사용한다. 그러면 둘중 하나만 성립해서 print가 된다.

```python
if name=="Junseong" or student_id =="20171603":
  print("Hi Junseong")
```
