---
layout: post
title: "Eureka Project"
date: 2022-11-28 20:00:00 +0900
categories: jekyll update
comments: true
---

## Jekyll이랑 Github Pages을 사용하여 블록 만들기

### 시작하기 전 준비 

- git(git bash) 설치

- Github에 <username>.github.io 저장소 만들기

<!--more-->

- Windows OS에서 ruby, jekyll 설치

- 로컬 저장소를 폴더를 만들기

### 로컬에서 jekyll을 설치하기

- 로컬 저장소에서 git bash 시작하기

- ``jekyll -v`` 명령을 돌리고 jekyll이 잘 설치되어있는지 확인하기

- 확인한 후 ``jekyll new . --force`` 명령을 돌리고 jekyll을 설치하기

- 실헹 후 ``ls`` 명령을 돌리고 웹파일들을 확인하기

- 마지막에 ``bundle exec jekyll serve`` 명령을 보내고 로컬에 웹을 돌려 보기

### 로컬에서 리모트로 남기기

- git bash을 시작하고 ``git status`` 명령을 돌리고 현재 상태를 보기

- ``git add * -f`` 명령을 보내고 모든 파일의 상태를 Staged으로 변경하기

- ``git commit -m "<comment>"`` 명령을 쓰고 comment 남기기

- ``git push origin main`` 명령을 보내고 모든 파일을 리모트로 올리기

### 포소트 업로드 하기

- 로컬 저장소의 _posts 폴더에서 새로운 파일을 만들기

- 파일 이름을 "YYYY-MM-DD-포스트-제목.md" 형식으로 정해주기

- 포스트 정보를 정해 놓고 내용을 쓰기

```markdown
---
layout: post
title: "제목"
date: YYYY-MM-DD HH-MM-SS +GT
categories: 카테고리
---
```

- 내용울 다 쓴 후에 파일을 저장하기

- 저장된 파일을 ``git add _posts/YYYY-MM-DD-포스트-제목.md`` 명령을 보내고, ``git commit -m "<message>"`` 명령으로 반영하기 

- 그 다음에 ``git push origin main`` 명령으로 리모트로 업로드 하기

### 원하는 테마를 설치하기 

- 원하는 테마의 저장소에 들어가기

- ``git clone``해서 로컬에 데마 저장소를 받아오기

- 테마파일들을 로컬저장소에 반영하기 

- ``_post`` 폿스트 폴더를 제외하고 테마를 덮어쓰기

- 변경된 파일들을 리모테에 반영하기 ``(git add/rm)`` 
-- add - 추가하기 
-- rm - 제거하기

### 댓글 기능을 추가하기

- Disqus 홈페이지에서 Signup을 눌러서 회원가입하기

- "I want to install Disqus on my site" 선택하기

- 사이트 정보를 입력하기

- Platform 중 Jekyll 선택하기

- 설명에다라 Setup을 해놓기

- 다음과 같은 key-value를 ``_config.yml`` 파일에 추가하기 
```markdown
comment: 
    provider:       "disqus"
    disqus:
        shortname:  "<username>"
```

- Disqus 홈페이지에서 Universal Code를 복사하고 ``_layouts/post.html`` 파일에 수정해 놓기 
![screenshot](https://raw.githubusercontent.com/20223073/20223073.github.io/main/public/screenshot.png)

- 주석 해제 후, PAGE_URL과 PAGE_IDENTIFIER를 설정
![sceenshot](https://raw.githubusercontent.com/20223073/20223073.github.io/main/public/screenshot1.png)

- 댓글을 허용하고 싶은 포스트에 ``comments: true``를 추가하기 
![screenshot](https://raw.githubusercontent.com/20223073/20223073.github.io/main/public/screenshot2.png)

### 내가 만든 추가 기능들

- date-format 변경함

![screenshot](https://raw.githubusercontent.com/20223073/20223073.github.io/main/public/screenshot14.png)

- post.excerpt 기능 추가함

![screenshot](https://raw.githubusercontent.com/20223073/20223073.github.io/main/public/screenshot15.png)

- Read more 버턴 추가함

![screenshot](https://raw.githubusercontent.com/20223073/20223073.github.io/main/public/screenshot16.png)