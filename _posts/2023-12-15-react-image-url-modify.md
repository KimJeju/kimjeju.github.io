---
title : "chirpy 템플릿 프로필 image url 설정하기"
categories : [Blog, gitblog]
tags : [git]
---

### chirpy 템플릿 Image Url 설정하기

깃 블로그를 만드는 도중 avarta 와 image가 올라가지 않는 현상이 발생해서
원인을 찾고 Url를 설정해서 이미지를 올리는 작업 진행

---

> ■ Image 가 올라가지 않은 원인
> - Config.yml 의 이미지 기본 url 이 "https://chirpy-img.netlify.app" 으로 설정 되어있음
> - "assets/img/[source]" 로 img url을 설정해도 " "https://chirpy-img.netlify.app/assets/~ 으로 설정됨"

---

--- 

> ■ 해결
> - Config.yml 의 이미지 기본 url 수정
> - Config_yml 62번줄 수정


### Config.yml 수정부분


```javascript
theme_mode: dark # [light|dark] 

# The CDN endpoint for images.
# Notice that once it is assigned, the CDN url
# will be added to all image (site avatar & posts' images) paths starting with '/'
#
# e.g. 'https://cdn.com'

// 이부분
img_cdn: "https://chirpy-img.netlify.app"


# the avatar on sidebar, support local or CORS resources
avatar: "/assets/img/source/avartar.png"

# boolean type, the global switch for TOC in posts.
toc: true
```

### To

```javascript
theme_mode: dark # [light|dark] 

# The CDN endpoint for images.
# Notice that once it is assigned, the CDN url
# will be added to all image (site avatar & posts' images) paths starting with '/'
#
# e.g. 'https://cdn.com'

// 빈공백으로 설정하면 local folder를 참조
img_cdn: ""


# the avatar on sidebar, support local or CORS resources
avatar: "/assets/img/source/avartar.png"

# boolean type, the global switch for TOC in posts.
toc: true
```
---

## 프로필 업로드 확인
![content image](/assets/img/22-12-15_post/change_profle.png){: width : "350" class="normal"}





