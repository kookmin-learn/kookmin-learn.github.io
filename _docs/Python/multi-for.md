---
title: 7-3. 중첩 반복문
category : Python
order: 12
layout: default
comments: true
---

## 중첩반복문이란?
우리는 지금까지 반복문을 배웠다. for문과 while문을 이용해서 여러가지 반복을 해봤고, 어떤 방식으로 사용되는 건지 알 수 있었다.

중첩 반복문이란 말 그대로 반복문을 여러개 중첩해서 사용하는 것이다. 엥? 이게 무슨말이냐고?? 실제 예를 한번 들어보도록 하자.

예를 들어서 3x3구구단을 for문을 이용해서 구현한다고 생각해보자! 아래처럼 정말 효율적인 코드를 작성할 수 있다!!! 와 정말 대다내!!!

```python
# 1*n
for number in range(1,4):
  print("1*",number,"=",1*number)

# 2*n
for number in range(1,4):
    print("2*",number,"=",1*number)

# 3*n
for number in range(1,4):
    print("3*",number,"=",1*number)
```

생각해보니 대다나지는 않은 것 같다. 지금은 3x3의 구구단이지만 **19x19 구구단은 생각만해도 끔찍할 것 같다.** 그럼 조금더 생각해서 해결점을 찾아보자... 음.. 반복.. 반복을 곂쳐서 사용하면 되지 않을까??? 맞다!!! 반복을 중첩해서 사용해보면 될것 같다.

뒷자리를 1부터 3까지 반복하는 반복문을 앞자리도 1부터 3까지 반복하는 반복문에 중첩하면 될것 같다!!!! 바로 아래와 같은 코드처럼 말이다!!

```python
# 3x3 짜리 구구단 출력해보기
for i in range(1,4):
  for j in range(1,4):
    print(i,"*",j,"=",i*j)
```

위의 코드를 해설해보자면 다음과 같다.
1. i=1일때 j=1 / 1*1=1
2. i=1일때 j=2 / 1*2=2
3. i=1일때 j=3 / 1*3=3
4. i=2일때 j=1 / 2*1=1
5. i=2일때 j=2 / 2*2=1
6. i=2일때 j=3 / 2*3=1
7. ...



```python
# 예제 4: 구구단 9x9
for number in range(1,10):
  for subnumber in range(1,10):
    print(number,"*",subnumber,"=",number*subnumber)

#결과
# 1*1=1
# 1*2=2
# 1*3=3
#...
```
