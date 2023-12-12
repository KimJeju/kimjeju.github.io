---
title : "git fatal : the remote end hung up unexpected 에러 핸들링"
categories : [Git, Error Handling] 
tags : [git, github, error]
---

### 문제
>깃허브에 Port Folio 관련 소스를 업데이트 도중 git fatal : the remote end hung up unexpected 에러 발생

- 원인 : 단일 파일 Post 최대 용량이 1MB 인데 Fort Polio 소스 내 동영상 파일이 1MB를 초과하여 발생


### 해결방안
- 깃허브 단일 파일 최대 Post 용량의 제한을 늘려준다

### 방법
> - 터미널 콘솔창에 아래와 같은 명령어를 입력해준다.
> - 아래 코드는 깃 Post 단일 용량 제한을 늘려주는 코드이다.
> - 본인의 기호에 맞게 원하는 용량을 http.postBuffer 뒤에 지정할 수 도 있다

<br/>

---
```C#
git config --global http.postBuffer 1024MB
```
---

<br/>
<br/>
<br/>



>참고 자료
> - https://choitaetae.tistory.com/123 블로그
