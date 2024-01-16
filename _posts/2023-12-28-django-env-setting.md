---
title : "Django Env 세팅하기"
categories : [Dev, Django]
tags : [python, Django]
---


## 네이버 SMTP 메일 Send를 위한 Django .env 설정


<br/>
<br/>
<br/>


### 1. requirements.txt 를 통해 django environ 설치
> ![content image](/assets/img/23-12-28_post/9.png)
> - requirements.txt 에 django-environ 을 기입하면 자동설치가 된다.

<br/>


### 2.최상위 폴더에 .env 생성 및 config 정의
>  - 최상위 폴더에 .env 생성
>> ![content image](/assets/img/23-12-28_post/7.png){: width : "150" class="normal"}
>  - .env 내부에 필요한 정보사항 작성 ( 필자의 경우 네이버 SMTP 정보작성 )

```python
# env 작성시에는 띄어쓰기가 없어야함
EMAIL_HOST=smtp.naver.com
EMAIL_PORT=000
EMAIL_USE_SSL=True
EMAIL_HOST_USER=test@naver.com
EMAIL_HOST_PASSWORD=aaaaaaaa
```
>


<br />      

### 3.settings.py 에 .env 정보를 가져올 수 있는 코드 작성
 
```python

import environ
from environ import Env

# 파일의 최상위 폴더
BASE_DIR = Path(__file__).resolve().parent.parent


env = Env()

#최상위 폴더의 ".env" 파일을 읽는다.
env_path = BASE_DIR / ".env"

## 만약 env 정보가 존재한다면 읽기쓰기 권한으로 .env 를열고 
# overwrite=True 를 사용해 기존 정보를 덮어쓴다.
if env_path.exists():
    with env_path.open("rt", encoding="utf8") as f:
        env.read_env(f, overwrite=True)

```
>
>


<br />

### 4. settings.py 최하단에 env 정보 기입해주기
```python

# email config
EMAIL_HOST = env.str("EMAIL_HOST")
EMAIL_PORT = env.int("EMAIL_PORT")
EMAIL_USE_SSL = env.bool("EMAIL_USE_SSL")
EMAIL_HOST_USER = env.str("EMAIL_HOST_USER")
EMAIL_HOST_PASSWORD = env.str("EMAIL_HOST_PASSWORD")

DEFAULT_FROM_EMAIL = f"{EMAIL_HOST_USER}@naver.com"
```
> - 각각의 데이터 타입에 맞는 env 정보를 key값을 통해 가져온다














