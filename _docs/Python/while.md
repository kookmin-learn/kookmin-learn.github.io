---
title: 7-2. 반복분 2(While문)
category : Python
order: 11
layout: default
comments: true
---

## while 반복문

저보다 설명을 잘해둔 [(링크)while문에 대해서 알아보자](https://wikidocs.net/21) 이 링크를 참조해주세요 :)

for문에서는 정해진 리스트에서 하나하나 꺼내왔다면, while문은 무한정 반복하는 **무한반복문** 이다.

무한반복문은 어떤 조건이 만족할 때, 무한정 계속 반복한다. 무슨소리인지 모르겠으니 코드를 보자(역시 개발자 문서)

아래 코드는 while문의 기본적인 구조이다. while문 안에잇는 조건이 True라면, 무한정 조건이 False가 될 때까지 계속 반복한다. (조금 헷갈릴 것 같다)

```python
while 조건:
  실행할 코드들
  ...
```

간단하게 아래와 같은 패턴을 생각하면 될것이다.

```python
while 숙제안함:
  숙제하기!!!

숙제 다함!!
```

아래의 코드의 결과를 보면 "Hello!!!!"가 무한정으로 출력이 될 것이다. 왜냐하면, 조건이 True로 고정이기 때문에 멈추지 않고 무한하게 출력이 되는 것이다.

```python
while True:
  print("Hello!!!!")
```

보통 아래 코드와 같은 형식으로 많이 사용된다. 반복할 때마다 count를 1씩 증가시키는데, 언제까지 반복하냐면 count<5 라는 조건이 만족할 때. 즉, count가 5보다 작은동안은 계속 반복한다. 그리고 count가 5가 된다면 멈추게 된다.

```python
count = 0

while count<5:
  count +=1
  print("Count :"+str(count))

print("Finished!")

#결과
>> Count : 1
>> Count : 2
>> Count : 3
>> Count : 4
>> Count : 5
>> Finished!!
```
