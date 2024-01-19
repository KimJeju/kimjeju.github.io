---
title : "드림핵 64se64 문제 풀이"
categories : [Dev, hacking]
tags : [hacking]
---


### Description
> 문제내용 : welcome 을 출력하는 html 페이지 소스를 분석하여 CTF 를 파악한다.


## 풀이
<hr/>

### 1. 문제 페이지에서 접속 vm 서버 생성하여 html 페이지 접근하기
> - 웹해킹 문제라 http// 로 접근할 수 있다.
> ![content image](/assets/img/24-01-19_post/1.png){: width="550" height="550"}

<br/>

### 2. 문제 페이지에서 소스 보기를 통해 html 구조확인하기
> - html 페이지에서 오른쪽 클릭 소스보기를 클릭한다.
> ![content image](/assets/img/24-01-19_post/2.png){: width="550" height="550"}
> - input 창에 있는 인코딩문자열을 모두 복사한다.
> ![content image](/assets/img/24-01-19_post/3.png){: width="550" height="550"}

<br/>

### 3. 복사한 base64 코드 decoding 하기
> - 복사한 암호코드를 base64 decoding 사이트에서 decoding 한다.
> ![content image](/assets/img/24-01-19_post/4.png){: width="550" height="550"}
> <a href="https://base64.guru/converter/decode">base 64 decoding 사이트</a>

<br/>

### 4. decoding 해서 나온 파이썬 코드 웹 컴파일러로 돌리기
> - decoding 후 나온 파이썬 코드를 본인의 편한 컴파일러로 돌린다.
> - - 필자는 편하게 웹컴파일리로 돌렸다.
> ![content image](/assets/img/24-01-19_post/5.png){: width="550" height="550"}
> <a href="https://www.mycompiler.io/ko/online-python-compiler">웹 파이썬 컴파일러</a>

<br/>

### 5. 웹 컴파일러로 돌려 나온 DH{} 코드 드림핵에 정답제출하기
> ![content image](/assets/img/24-01-19_post/6.png){: width="550" height="550"}
