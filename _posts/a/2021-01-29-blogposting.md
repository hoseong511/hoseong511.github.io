---
title:  "블로그 소개"
excerpt: "나의 깃허브 블로그"

categories:
  - a
tags:
  - [Blog, jekyll, Github, Git, Python django]

toc: true
toc_sticky: true

date: 2021-01-29
last_modified_at: 2021-01-31


---
## GitHub Pages
Python django 페이징처리에 대해서 찾아보던 중 관련 블로그에서<sup>[1)](#footnote_1)</sup> 작성글도 보고 작성자의 깃허브도 보고나서 지난날의 게으름을 반성하며 깃허브 블로그 만들기를 마구 검색하기 시작했다.   

GitHub Pages는 사용자가 DB나 Server를 구성할 필요 없이 간단히 이용할 수 있다고 한다. 아래참조!   

{% include video id="2MsN8gpT6jY" provider="youtube" %}

이와 더불어 GitHub Pages에 날개를 달아줄 친구를 소개하겠다. 그것은 바로 <span style="color:yellow">**Jekyll**</span>이라고 불리는 친구인데, 이 녀석이 Markdown으로 된 텍스트를 GitHub-Pages내에서 이용할 수 있게 도와주는 고마운 녀석이다. 이로써 한층 더 편리하게 블로그 포스팅이 가능해졌다는 말이다!!
#### 0. 내 환경
- git version 2.24.3
- jekyll 4.2.0
- gem 3.2.3
- ruby 2.7.2
- rbenv 1.1.2
- homebrew 2.7.6
- terminal 2.10
- macOS Catalina 10.15.7

#### 1. GitHub
- 공식문서에서 제공하는 방식대로 따라하면 쉽게 Hello Wolrd를 !!!<sup>[2)](#footnote_1)</sup>   
- 공식문서에서 여러분의 GitHub Pages를 만들어 Hello World를 보았다면 다음 단계이다. <span style="color:yellow">**Jekyll**</span>를 설치해보고 제공하는 theme를 이용해 편리하게 블로그다운 블로그를 만들어보자!

#### 2. Ruby
- <span style="color:yellow">**Jekyll**</span>를 설치하기에 앞서 <span style="color:yellow">**Jekyll**</span>를 이용할 수 있도록 만들어주는 친구가 필요하다. 그게 바로 **Ruby**라는 녀석이다.
- 여러 시행착오를 겪고(?) **rbenv**라고 원하는 버전의 **Ruby**를 이용하게 도와주는 툴을 이용할 것이다.
- ```
  $ brew install rbenv
  $ rbenv install 2.7.2
  $ rbenv rehash
  $ echo '[[ -d ~/.rbenv   ]] && export PATH=${HOME}/.rbenv/bin:${PATH} && "$(rbenv init - )"' >> ~/.zshrc
  $ cd <your local repository>
  $ rbenv local 2.7.2
  ```
  환경변수를 잡는 명령어가 안된다면 직접 .zshrc를 편집해야한다..

#### 3. Jekyll
- 이제 <span style="color:yellow">**Jekyll**</span>를 설치해보자.
- ```
  $ gem install bundler jekyll
  $ jekyll new myblog
  $ cd myblog
  $ bundle exec jekyll serve
  ```
  브라우저로 http://localhost:4000 접속하면     
  ![image](https://user-images.githubusercontent.com/62678380/106360381-74f02100-635b-11eb-9057-cf155502c707.png){: .align-center}
- 역시 공식문서가 짱이다.<sup>[3)](#footnote_1)</sup>

#### 4. minimal mistakes theme
- 내 블로그 테마는 minimal misktakes라는 theme인데 github 블로그를 이용하는 사람들 대부분이 이 theme이다.. ~~그래서 나도 minimal mistakes를 이용했다 ㅋㅋㅋㅋㅋㅋ~~
- [jekyll theme](http://jekyllthemes.org/) 여기서 원하는 theme를 골라보자!
- 방식은 아래와 같다.<sup>[4)](#footnote_1)</sup>   
   1. 깃 다운로드
   2. Gem파일을 이용한 방법   
   3. Remote theme 방법
 - 깃 다운로드의 경우, 깃 위치에 복붙하면 된다.
 ~~나는 깃 다운로드해서 복붙했..~~

 여기까지가 GitHub Pages를 만들고 theme까지 적용시키는 과정이고, 블로그 포스팅을 내 입맛에 맞게 즐기는 일만 남았다 :)



<!-- ![2020](https://user-images.githubusercontent.com/62678380/106272400-595e1b00-6274-11eb-96bb-4e517542425a.jpeg){: .align-center} -->

<!-- ```python
print("a")
``` -->


---
<a name="footnote_1">1)</a> [Today.log](https://parkhyeonchae.github.io/2020/04/01/django-project-17/)   
<a name="footnote_1">2)</a> [Github Pages 시작](https://pages.github.com/)   
<a name="footnote_1">3)</a> [jekyll 빠른시작](http://jekyllrb-ko.github.io/docs/)   
<a name="footnote_1">4)</a> [minimal mistakes 시작](https://github.com/mmistakes/minimal-mistakes)
