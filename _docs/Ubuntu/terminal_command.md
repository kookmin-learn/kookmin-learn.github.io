---
title: how to use terminal?
category : Ubuntu
order: 2
layout: default
comment: true
---
작성자:신민욱 금요일, 24. 3월 2017 

## 터미널을 켜봅시다.
하얀 것은 글씨, 검은건 배경입니다.
하지만 알고보면 ~~전혀 어렵지않고~~ 재미있습니다.

## 프로그램 실행
보통 <code>apt</code>로 설치한 프로그램은 기본적으로 "해당 프로그램 이름"을 입력하면 실행됩니다.
```bash
gedit
```
약간 응용해서.. 관리자 권한으로 특정 경로에서 특정 프로그램을 이용해 파일을 열어봅시다.
```bash
sudo gedit (경로)/(프로그램)
```
**주의점 : sudo 권한은 조심히 사용해야 합니다. rm -rf처럼 위험한 명령어도 있거든요..!**
## 프로그램 설치
만약 프로그램이 없다면 <code>apt install</code>을 써봅시다.
```bash
sudo apt install <설치프로그램>
```
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
```bash
sudo add-apt-repository '저장소 이름'
```
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
## 폴더 안 파일 목록 조회
```bash
ls -al
```
생각해보기 : 옵션은 다양합니다. 한 번씩 비교해보세요!
## 작업 폴더 이동하기
```bash
cd (작업 경로)
```
상위 폴더로 가려면 <code>../</code>!
## 폴더 만들고 지우기
```bash
mkdir (만들 폴더명)
rm -r (지울 폴더명)
```
**주의점 : rm하실때는 sudo를 남발하지마세요!**
##  파일 복사
```bash
cp (옮길 파일) (도착 위치)
```
mv 명령어도 있으나 지우고 옮기는 것이기 때문에 권장하지 않습니다.
## 파일 바로가기 만들기
```bash
ln -s (파일) (바로가기 이름)
```