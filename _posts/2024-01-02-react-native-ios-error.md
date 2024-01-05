---
title : "react-native run-ios 시 에러"
categories : [Dev, react]
tags : [python, Django]
---


## react-native 앱 세팅 중 ios 빌드 에러발생

<hr/>

### 에러코드

```

--- xcodebuild: WARNING: Using the first of multiple matching destinations:
{ platform:iOS Simulator, id:550BB99C-01A0-4CCD-928A-F64604A0774F, OS:16.4, name:iPhone 14 Pro }
{ platform:iOS Simulator, id:550BB99C-01A0-4CCD-928A-F64604A0774F, OS:16.4, name:iPhone 14 Pro }
** BUILD FAILED **

```

<br/>
<br/>

<hr/>

### 해결
>  react native 프로젝트 ios 폴더에서 아래 명령어 실행

```

cd ios
pod instsall
cd ..
npx react-native run-ios

```

<br/>
<hr/>

### 정상 작동
![content image](/assets/img/single_source/2024_01_03.png){: width : "150" class="normal"}

##