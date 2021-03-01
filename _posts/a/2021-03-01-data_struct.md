---
title:  "내가 쓰는 git 명령어"
excerpt: "쉽게 commit과 push를 하자!"

categories:
  - a
tags:
  - [GitHub, git]

toc: true
toc_sticky: true

date: 2021-02-10
last_modified_at: 2021-02-10


---
컴퓨터를 구매하고 코딩 관련 공부를 열심히 하고픈 마음에 시작한 블로그, 깃허브 잔디심기!!   
사실 잔디심기는 시각적인 만족을 위한 것 같다(뭐.. 일석이조지 공부도 하고 시각적으로 만족도 하고 ㅎㅎ) 그렇게 깃허브를 관리하기 위해 관련 도구를 찾아보던 중 동기에게 **[소스트리(SourceTree)](https://www.sourcetreeapp.com/)** 얘기를 들었던 기억이 났다. ~~이름이 생각안나 다시물어봤지만~~

처음에는 깃허브 로그인 접속이 잘 되었고 여러 차례 로그인, 깃 클론을 하더라도 문제없이 작동되었다. 문제를 감지한 날, 깃 클론을 해야할 일이 있어서 깃허브에 로그인을 하려했던걸로 기억한다. 그때 팬이 미친듯이 돌아가고 소스트리는 강제종료되는 현상이 일어난것이다. 해당 문제는 [여기서](https://jira.atlassian.com/browse/SRCTREE-7272) 확인가능하다.   

문제를 확인하면서 해결해보려 했는데... 편하자고 쓰는 도구인데 도대체 왜 내가 불편함을 겪으면서 이 도구에 맞춰 내 컴퓨터를 맞춰야지? 하는 생각이 들면서 터미널로 갈아탔다.   
그렇게해서 내가 자주 쓰는 명령어를 정리해봤다.   

#### git status
원격 리포지토리와 현재 내 작업영역과의 차이(상태)를 알려준다.   
git commit과 push를 하기 전, 항상 git status로 원격 리포지토리와 내 작업영역의 상태를 확인해야 군더더기를 없앨 수 있다.   
이와 더불어 ```git log```도 있다 이건 commit의 기록을 볼 수 있는 명령어이다.

#### 리포지토리를 새로 만들었을때
```
git init
git add . # 소스 코드를 작업하는 영역에서 이루어진 작업 내용을 Git의 스테이징 영역으로 이동시킨다.
git commit -m "" # 로컬 Git의 리포지토리에 반영
git branch -M main
git remote add origin https://github.com/xxxx/xxxx.git
git push -u origin main # 원격 Git의 리포지토리에 반영
```

#### 다른 pc에서 깃허브 작업을 할때
```
git clone
git add .
git commit -m ""
git push
```

#### 작업 되돌리기
```
git reset HEAD~1 # 1개 이전 이력으로 돌아감
```
reset은 시간을 되돌리는 기능이다. 위와 같이 명령어를 입력하면 1개 이전에 입력했던 commit으로 돌아간다.