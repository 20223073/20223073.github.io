---
layout: post
title: "Jekyll 사이트에 Google Anlytics 추가하기"
date: 2022-11-28 22:00:00 +0900
categories: jekyll update
comments: true
---


### Google Analytics에 들어가서 구글 계정으로 로그인 하기

- 측정 시작 버턴을 누른다

![screenshot4](https://raw.githubusercontent.com/20223073/20223073.github.io/main/public/screenshot4.png)

<!--more-->

### 속성 설정하기

- 다음과 같이 설정한다

![screenshot5](https://raw.githubusercontent.com/20223073/20223073.github.io/main/public/screenshot5.png)

- 아무박스를 클릭하지 않고 `만들기` 버턴을 누른다

![screenshot6](https://raw.githubusercontent.com/20223073/20223073.github.io/main/public/screenshot6.png)

- 다음에 창이 뜨면 체크 후 `동의함` 버턴울 누른다

![screenshot7](https://raw.githubusercontent.com/20223073/20223073.github.io/main/public/screenshot7.png)


### Gtag 측정 ID 생성하기

- 성공하면 `완료`라는 창이 뜬다

![screenshot8](https://raw.githubusercontent.com/20223073/20223073.github.io/main/public/screenshot8.png)

- 다음 같이 창이 나올 때 `웹` 버턴을 누른다

![screenshot9](https://raw.githubusercontent.com/20223073/20223073.github.io/main/public/screenshot9.png)

- 뜬 창에 웹의 정보를 입력해주구 `스트림 만들기` 버턴을 누른다

![screenshot10](https://raw.githubusercontent.com/20223073/20223073.github.io/main/public/screenshot10.png)

- 다음과 같이 측정 ID가 나오면, 측정 ID 생성 완료

![screenshot11](https://raw.githubusercontent.com/20223073/20223073.github.io/main/public/screenshot11.png)

### 측정 ID를 웹에 설치하기

- *_includes* 디록테리에서 *`google_analytics.html`* 이라는 파일을 만들어서 다음 코드를 저장해 둔다.

![screenshot](https://raw.githubusercontent.com/20223073/20223073.github.io/main/public/screenshot13.png)
[source code](https://raw.githubusercontent.com/20223073/20223073.github.io/main/_includes/google_analytics.html)

- `_config.yml` 파일에서 다음 key-value를 추가한다.
*`G-XXXXXXXXXX`를 자기 측정 ID로 변경해야 됨*
```
# Google Analytics
google_analytics: G-XXXXXXXXXX
```

- 다음 코드를 `</head>` 태그의 위에 붙여넣기
![screenshot](https://raw.githubusercontent.com/20223073/20223073.github.io/main/public/screenshot12.png)


마지막에 모든 파일을 저장하고 리모트에 푸시하면 완료.
