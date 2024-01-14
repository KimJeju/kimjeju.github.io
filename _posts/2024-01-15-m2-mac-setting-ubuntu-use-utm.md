---
title : "M2 맥북에 Utm을 사용해서 우분투 22.04 가상환경 세팅하기"
categories : [Dev, linux]
tags : [os, linux ]
---


### 1. 우분투 다운받기

> <a href="https://ubuntu.com/download/server/arm">우분투 ios 다운로드</a>
> - 다운로드 받은 후 본인이 찾기 편한 폴더로 이동 시켜놓기
> ![content image](/assets/img/24-01-15_post/1.png){: width : "150" class="normal"}

<br/>

<hr/>

### 2. 가상환경 머신 UTM 다운받기
> <a href="https://mac.getutm.app/">UTM 다운로드</a>
> - 받은 후 설치 및 실행 시키기
> - ![content image](/assets/img/24-01-15_post/2.png){: width="550" height="550"}


<br/>

### 3. 가상머신에서 우분투 ios 세팅하기
> - UTM 실행 및 새 가상환경 만들기 클릭
> - - ![content image](/assets/img/24-01-15_post/3.png){: width="550" height="550"}
>
> - 버추얼라이즈 선택
> - - ![content image](/assets/img/24-01-15_post/4.png){: width="550" height="550"}
> 
> - Os 리눅스 선택
> - - ![content image](/assets/img/24-01-15_post/5.png){: width="550" height="550"}
>
> - boot ios image 에서 탐색 눌러 아까 다운받은 ios path 설정
> - - ![content image](/assets/img/24-01-15_post/6.png){: width="550" height="550"}
>
> - 이름 설정 및 저장
> - - ![content image](/assets/img/24-01-15_post/7.png){: width="550" height="550"}

<br/>

### 4. 우분투 실행 및 초기설정
> - 우분투 초기실행 화면, Try or Install ubuntu server 선택
> - - ![content image](/assets/img/24-01-15_post/8.png){: width="650" height="650"}
>
> - 필자는 언어 English 선태 
> - - ![content image](/assets/img/24-01-15_post/9.png){: width="650" height="650"}
> 
> - Continue without updating 선택 및 프록시 설정 나올 때 까지 done 선택
> - - ![content image](/assets/img/24-01-15_post/10.png){: width="650" height="650"}
>
> - 프록시 설정
> - 프록시에 "http://kr.ports.ubuntu.com/ubuntu-ports" 입력
> - - ![content image](/assets/img/24-01-15_post/11.png){: width="650" height="650"}
> 
> - 미러사이트 설정
> - - ![content image](/assets/img/24-01-15_post/12.png){: width="650" height="650"}
>
> - 디스크 설정화면에서, 가상머신 전제 디스크를 사용하도록 use an entire disk 체크 및 done
> - - ![content image](/assets/img/24-01-15_post/13.png){: width="650" height="650"}
>
> - 다음 화면 에서 done을 누르면 디스크가 초기화 될 수 있다는 경고가 나옴
> - 하지만 새로 만드는 것 이므로 continue
> - - ![content image](/assets/img/24-01-15_post/13.png){: width="650" height="650"}
> - - ![content image](/assets/img/24-01-15_post/14.png){: width="650" height="650"}
>
> - 위 부터 차례대로 본인에 맞게 정보 입력 done
> - - ![content image](/assets/img/24-01-15_post/15.png){: width="650" height="650"}
>
> - 그 다음 유료플랜 사용할 거냐 뭍는데 스킵
> - - ![content image](/assets/img/24-01-15_post/16.png){: width="650" height="650"}
>
> - open ssh 설치할 것인지 묻는데 차후 사용할 것이니 install 에 체크 done
> - - ![content image](/assets/img/24-01-15_post/17.png){: width="650" height="650"}
>
> - 아래 목록 중 필요한 패키지 체크 및 설치 ( 필차는 우선 스킵 )
> - - ![content image](/assets/img/24-01-15_post/18.png){: width="650" height="650"}
>
> - 모든 설정을 마치면 우분투 패키지 설치에 들어감
> - - ![content image](/assets/img/24-01-15_post/19.png){: width="650" height="650"}
>
> - view full log를 통해 진행사항 확인가능
> - - ![content image](/assets/img/24-01-15_post/20.png){: width="650" height="650"}
>
> - 설치가 완료되면 reboot now 가 뜨는데 reboot now 선택
> - - ![content image](/assets/img/24-01-15_post/21.png){: width="650" height="650"}


<br/>

### 5. 가상머신으로 우분투 실행
> - 설치 완료 후 부팅용 이미지 파일 (.ios) 초기화 후 실행
> - - ![content image](/assets/img/24-01-15_post/22.png){: width="650" height="650"}
>
> - 초기화 한 가상머신 실행
> - - ![content image](/assets/img/24-01-15_post/23.png){: width="650" height="650"}
>
> - 실행 후 아까 설정한 유저네임 및 비밀번호 입력
> - - ![content image](/assets/img/24-01-15_post/24.png){: width="650" height="650"}
>
> - 정상실행 확인
> - - ![content image](/assets/img/24-01-15_post/25.png){: width="650" height="650"}


### 참고 
> - <a href="https://gymdev.tistory.com/">개발 짐 블로그</a>
