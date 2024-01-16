---
title : "Django 부트스트랩 추가해보기"
categories : [Dev, Django]
tags : [python, Django]
---


### 1. 프로젝트 최상위 폴더에 requirements.txt 추가
> - requirements.txt 는 Django 부트스트랩에 텍스트형식 패키지 관리 시스템이다.
> - 프로젝트 최상위 폴더에 추가해준다.
>> ![content image](/assets/img/23-12-27_post3/1.png){: width : "150" class="normal"}


<br />      

### 2.requirements.txt 에 bootstrap5 추가 및 인스톨
> - requirements.txt 에 django-bootstrap5 입력
> - bootstarp5 설치
> 
>> ![content image](/assets/img/23-12-27_post3/3.png){: width : "150" class="normal"}



<br />

### 3. 사용할 html 파일에 bootstrap 로드
> - bootstrap 로드하기
>> ![content image](/assets/img/23-12-27_post3/4.png){: width : "150" class="normal"}
> - bootstrap form 정의하기
>> ![content image](/assets/img/23-12-27_post3/5.png){: width : "150" class="normal"}

### 4. view 함수 정의하기
> - 이번엔 람다식으로 정의
>> ![content image](/assets/img/23-12-27_post3/6.png){: width : "150" class="normal"}

### 5. Main 앱의 urls 에 url 연결해주기
> - 사용한 url과 함수를 parameter로 넘겨준다
>> ![content image](/assets/img/23-12-27_post3/7.png){: width : "150" class="normal"}
> - 페이지 잘 로드 되는지 확인
>> ![content image](/assets/img/23-12-27_post3/8.png){: width : "150" class="normal"}
















