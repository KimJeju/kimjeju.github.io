---
title : "드림핵 Baby Linux 풀이"
categories : [Dev, hacking]
tags : [hacking]
---


### Description
> - 문제내용 : 제공된 html 페이지 및 소스코드를 분석해 옳바른 명령어를 수행해 flag.txt 의 경로 및 flag를 찾아낸다.
> - 풀이법 : 재공된 html 페이지의 input을 linux 서버의 input 창이라 생각하고 명령어를 수행한다
> > - 참고 : $() 구조는 소괄호 안에 서술한 스크립트 명령어에 대한 output을 return 한다

## 풀이
<hr/>
### 1. 문제 페이지에서 접속 vm 서버 생성하여 html 페이지 접근하기
> ![content image](/assets/img/24-01-22_post/2.png){: width="550" height="550"}


<br/>

### 2. pwd 및 ls 명령어를 통해서 구조 분석하기
> - "pwd" 명령어를 입력하여 현재 내 위치를 파악한다.
> - "ls" 명령어를 입력하여 현재 폴더에 어떠한 파일들이 있는 지 파악한다.
> ![content image](/assets/img/24-01-22_post/1.png){: width="550" height="550"}

<br/>

### 3. ls 명령어를 통해 나온 파일 분석하기
> - "ls" 명령어를 나온 목록 중 hint.txt 를 cat 을 통해서 출력한다.
> ![content image](/assets/img/24-01-22_post/3.png){: width="550" height="550"}
*Result로 flag 의 위치를 파악할 수 있다.*

<br/>

### 4. flag.txt 출력하기
> - cat 명령어를 통해 ./dream/hack/hello/flag.txt 를 출력한다.
> > - 주의 : 제공된 소스코드에 보면 input에 "flag" 문자열이 포함되면 result에 "No!" 가 출력되며 return 되는데 이때 와일드카드를 사용한다.  
> > ![content image](/assets/img/24-01-22_post/4.png){: width="550" height="550"}
>  - 최종명령어 : cat ./dream/hack/hello/fl?g.txt

<br/>

### 5. DH{} 코드 드림핵에 정답제출하기
> ![content image](/assets/img/24-01-22_post/6.png){: width="550" height="550"}
