---
title: 2.터미널 사용하기
category : Ubuntu
order: 2
layout: default
comment: true
---  

## 터미널을 켜봅시다.
![](http://i.imgur.com/EjSKlYd.png)
하얀 것은 글씨, 검은건 배경입니다.
하지만 알고보면 ~~전혀 어렵지않고~~ 재미있습니다.
## 관리자 권한[^1] 받기
명령어를 입력할때마다
```bash
E: 잠금 파일 /var/lib/dpkg/lock 파일을 열 수 없습니다 - open (13: 허가 거부)
E: 관리 디렉터리를 (/var/lib/dpkg/) 잠글 수 없습니다. 루트 사용자가 맞습니까?
```
이런 형식의 문구가 출력된 것을 본적이 있을 겁니다.
이럴 때는 본인이 <code>루트 사용자가 맞습니까?</code>에 대한 답을 주면되겠죠?
<code>sudo</code>를 명령어 앞에 붙여 본인이 루트사용자가 맞다고 인증을 하면 됩니다.

sudo명령어는 substitute user do의 줄임말로써 다른 사용자의 권한을 가져온다는 의미를 가지며, 대부분은 파일 접근이 쉬운 관리자(루트)권한을 가져올때 쓰인답니다.

>**주의!** : 관리자 권한을 획득할 sudo 명령어는 조심히 사용해야 합니다. rm -rf[^2]처럼 위험한 명령어도 있거든요..!

## 프로그램 실행
보통 <code>apt</code>로 설치한 프로그램은 기본적으로 "해당 프로그램 이름"을 입력하면 실행됩니다.
```bash
gedit
```
약간 응용해서.. 관리자 권한으로 특정 경로에서 특정 프로그램을 이용해 파일을 열어봅시다.
```bash
sudo gedit (경로)/(파일)
```
>ex) <code>sudo gedit 바탕화면/예제.txt</code>
## 프로그램 설치
만약 프로그램이 없다면 <code>apt install</code>을 써봅시다.
```bash
sudo apt install <설치프로그램>
```
>깃이라는 프로그램을 설치합니다.
ex) <code>sudo apt install git </code>
### 만약 이런 오류가 뜬다면...
```bash
 ThinkPad@ThinkPad-T460 ~  sudo apt install kakaotalk
[sudo] password for ThinkPad : 
패키지 목록을 읽는 중입니다... 완료
의존성 트리를 만드는 중입니다
상태 정보를 읽는 중입니다... 완료
E: kakaotalk 패키지를 찾을 수 없습니다
```
말 그대로 설치할 프로그램이 저장소에 존재하지 않은 겁니다.
만약 PPA가 존재한다면 설치해줍시다.
><b>잠시만요! PPA는 무엇인가요? </b>: 
ppa란, 우분투에서 기본으로 선별한 프로그램을 제외한 나머지 프로그램들을 위한 소프트웨어 저장소랍니다.
터미널에서 <code>E:[]패키지를 찾을 수 없습니다</code>라고 출력되는 것 또한, 우분투에서 준비해온 프로그램이 아니라는 증거죠!

```bash
sudo add-apt-repository '저장소 이름'
```
>와인이라는 프로그램의 ppa는 이런식으로 추가할 수 있습니다. 
ex)<code>sudo add-apt-repository ppa:ubuntu-wine/ppa</code>

## 프로그램 업데이트
```bash
sudo apt update; sudo apt upgrade
```
<code>;</code> 다음은 자동으로 명령어가 차례대로 실행됩니다.
## 프로그램 삭제 
자 설치는 했는데, 삭제를 하고 싶다고 하시면... install 대신 remove를 입력해주세요.
```bash
sudo apt remove "패키지"
```
>깃이라는 프로그램을 삭제합니다. 
ex) <code>sudo apt remove git </code>

## 폴더 안 파일 목록 조회
```bash
ls -al
```
><b>생각해보기</b> : 옵션은 다양합니다. 한 번씩 비교해보세요!
## 작업 폴더 이동하기
```bash
cd (작업 경로)
```
상위 폴더로 가려면 <code>../</code>! ex)<code>cd ../</code>
## 폴더 만들고 지우기
```bash
mkdir (만들 폴더명)
rm -r (지울 폴더명)
```
**주의점 : rm하실때는 sudo를 남발하지마세요, 시스템 관련 파일을 건드릴 수 있습니다!**
##  파일 복사&이동
복사할 때 : 
```bash
cp (옮길 파일) (도착 위치)
```
>mp3.mp3 파일을 music 폴더에 넣습니다.
ex) <code>cp mp3.mp3 music/ </code>

이동할 때 : 
```bash
mv (옮길 파일) (도착 위치)
```
><b>주의!</b> : 파일을 지우고 이동하기 때문에 신중해야합니다. 

## 파일 바로가기 만들기
```bash
ln -s (파일) (바로가기 이름)
```
>program폴더의 file파일을 바탕화면에 link라는 이름으로 바로가기를 만들어줍니다.
ex) <code>ln -s program/file 바탕화면/link</code>

[^1]: 파일의 읽기(r),쓰기(w),실행(x) 접근을 관리하는 체계,
[^2]:해당 드라이브의 모든 파일과 폴더를 지우고 사라지는 명령어
