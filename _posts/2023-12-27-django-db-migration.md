---
title : "Django Model 마이그레이션 해보기"
categories : [Python, Django]
tags : [python, Django]
---

### Mac 환겅


### 1.Python 설치하기
> 1. models.py 에 모델 클래스 정의
![content image](/assets/img/23-12-27_post/1.png){: width : "150" class="normal"}
>


<br />

### 2.manage.py 가 있는 폴더에서 마이그레이션 만들기
![content image](/assets/img/23-12-27_post/2.png){: width : "150" class="normal"}
>
```python
python manage.py makemigrations {본인 앱 이름}
```


<br />

### 3. Db 와 마이그레이션 진행하기
![content image](/assets/img/23-12-27_post/3.png){: width : "150" class="normal"}
>
```python
python manage.py migrate {본인 앱 이름}
```
> - 마이그레이션 시에 어떤 Sql 문 실행되었는지 확인하기
> ![content image](/assets/img/23-12-27_post/4.png){: width : "150" class="normal"}
```python
python manage.py sqlmigate {본인 앱 이름} { initial 된 마이그레이션 번호 }
```
> - Db 에서 마이그레이션 잘 되었는지 확인하기
> ![content image](/assets/img/23-12-27_post/5.png){: width : "150" class="normal"}

### 4.가상환경에 Django 설치
> 1. 장고설치
```
pip3 install django
```
> 2. 장고 버전 확인
```
python -m django --version
```
![content image](/assets/img/23-12-20_post/4.png)
> 3. 장고 프로젝트 생성
```python
django-admin startproject 플젝이름 
```
> 4. 프로젝트 생성 폴더에 setting.py => Timezone 설정
![content image](/assets/img/23-12-20_post/5.png)
> 5. 프로젝트 폴더로 가서 프로젝트 실행
```python
python manage.py runserver
```

### 5. 실행확인
> - 터미널 상에 실행 url 입력 및 확인
![content image](/assets/img/23-12-20_post/6.png)














