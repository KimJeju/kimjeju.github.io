---
title : "mac 환경에 Django 세팅하기"
categories : [Python, Django]
tags : [python, Django]
---

### Mac 환겅
> - M2 맥북 에어
> - mac os Sonoma 14.2
> - python 3.9.6
> - 터미널 zsh
<!-- ![content image](/assets/img/22-12-17_post/2.png){: width : "150" class="normal"} -->

<hr/>

### 1.Python 설치하기
> 1. pythone 설치 여부 확인
![content image](/assets/img/23-12-20_post/1.png){: width : "150" class="normal"}
>
> 2. 깔려있지 않다면 아래 링크에서 설치하기
>  - python 공식 다운로드 (필자 3.9.6 설치)
>  - [python 공홈](https://www.python.org/downloads/)
>
> 3. python3 명령어를 python 으로 바꾸기 위해 환경변수 설정
> - 터미널에서 vi~/.zshrc 실행 후 아래 코드 입력
> - vi 환경에서 a 를 눌러 input 환경으로 만든 후 맨 아레에 작성 후 esc 누르고 wq( 입력저장 )로 빠져나오기
```
alias python="python3"
# Setting PATH for Python 3.9
export PATH="/Library/Frameworks/Python.framework/Version/3.9/bin:${PATH}"
```

<br />

### 2.가상환경 구축하기
> - 가상환경을 구축하는 이유
> - - 프로젝트마다 격리된 환경을 구축해 프로젝트별 패키지를 관리하기 위함
> - - 진행하는 프로젝트에서 필요로하는 버전의 패키지만 설치 구성 하기 위함
> - - 차 후 더 추가 예정


> 1. virtualenvwrapper 설치
```
// 내 맥 기준 pip 뒤에 3을 안붙여주면 커맨드를 찾지 못한다.
sudo pip3 install virtualenvwrapper
```
> 2. 다시 vi~/.zshrc 를 터미널에서 실행해 아래 환경변수 추가
```
export WORKON_HOME=$HOME/.virtualenvs
export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3
export PROJECT_HOME=$HOME/Devel
source /usr/local/bin/virtualenvwrapper.sh
```
![content image](/assets/img/23-12-20_post/2.png)
> 3. 터미널에서 source ~/.zshrc 실행

<br />

### 3.가상환경 생성
> 1. 가상환경 생성
```
mkvirtualenv 가상환경명
```
> 2. 가상환경 활성화
```
workon 가상환경명
```
![content image](/assets/img/23-12-20_post/3.png)
*가상환경 실행화면*

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














