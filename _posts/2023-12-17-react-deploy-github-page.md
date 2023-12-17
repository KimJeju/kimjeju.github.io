---
title : "리액트 프로젝트 깃허브 페이지로 배포하기"
categories : [Blog, gitblog]
tags : [git]
---

### 리액트 프로젝트 깃 허브 페이지 배포 step

> gh-page 라이브러리 설치하기
> - ##### 본인의 패키지에 맞게 아래 두 커맨드 리액트 프로젝트 폴더 cmd 에서 실행 
> - npm install gh-pages --save
> - yarm install gh-pages 
![content image](/assets/img/22-12-17_post/2.png){: width : "150" class="normal"}
*npm install gh-pages --save 실행화면*


<br/>

> package.json 파일에 본인의 레파지토리 주소 및 npm script 추가하기
> - package.js 최상단의   "homepage": "https://{본인 깃허브 이름}.github.io/{본인 레포지토리 이름}/" 작성
> ![content image](/assets/img/22-12-17_post/9.png)
*package.json 에 깃주소 추가*
>
> - scripts 블럭안에 "predeploy": "npm run build", "deploy": "gh-pages -d build" 두 스크립트 추가
> ![content image](/assets/img/22-12-17_post/3.png)
*package.json 에 script 추가*

<br/>

> build script 실행
> - 추가한 script "npm run deploy" 실행
> ![content image](/assets/img/22-12-17_post/7.png)
*script 실행 화면*

<br/>

> github page 에 빌드 배포 
> - 본인의 레포지토리에 setting 들어가기
> ![content image](/assets/img/22-12-17_post/10.png)
>
> - pages 에 들어가기
> ![content image](/assets/img/22-12-17_post/11.png){: width="50%" height="50%"}
> 
> - npm run deploy 실행 시 생성되는 gh-pages 브랜치로 변경하기
> ![content image](/assets/img/22-12-17_post/12.png){: width="50%" height="50%"}
>
> - git에 프로젝트 소스 올리기

<br/>

> github action에서 파이프라인 확인하기
> ![content image](/assets/img/22-12-17_post/5.png)

<br/>
> github action에서 파이프라인 확인하기
> ![content image](/assets/img/22-12-17_post/13.png)










