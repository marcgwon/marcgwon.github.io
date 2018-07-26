---
layout: post
title: Docker로 anaconda 설치
categories:
  - python
tags:
  - python
  - anaconda
  - docker
excerpt_separator:  <!--more-->

---

#### Docker 이미지 검색

```sh
docker search anaconda3
```
continuumio/anaconda3를 선택.
<br>
<br>

#### 설치 및 실행

```sh
docker run -it -p 8888:8888 -v $(pwd):/notebooks --name anaconda3 continuumio/anaconda3
```

-it : 인터렉티브, 터미널 모드  
-p : 로컬과 컨테이너의 포트 오픈 및 연결  
-v : 로컬 현재 디렉토리를 컨테이너의 /notebooks 디렉토리와 바인딩  
--name : 컨테이너 이름 설정  
continuumio/anaconda3 : 이미지 이름  
<br>
<br>
#### jupyter notebook 실행

```sh
jupyter notebook --ip='*' --port=8888 --no-browser --allow-root
```

실행 후 완료 메시지와 함께 접속 url을 표시해줌

`http://localhost:8888/?token=TOKEN_STRING`
<br>
<br>

