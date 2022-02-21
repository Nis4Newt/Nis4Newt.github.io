---
title: "[git][기초] git config"
layout: single
categories: git
tag:
  - config
  - git config

last_modified_at: 2022-02-16T00:00:00-00:00
---

## config 설정
git config는 사용자 맞춤설정을 통해 git을 더 쉽고 편하게 사용 할 수 있도록 도와준다.   
git의 설정을 추가/변경/삭제

기본 폼 `git config`   

### config 설정범위
git config는 3가지의 범위로 나눌 수 있다.   

1. System (전체 시스템)
   - 모든 사용자와 모든 저장소에 적용되는 설정파일
   - C:\Program Files\Git\etc\gitconfig 파일
   - `git config --system`를 통해 접근
2. Global (사용자)
   - 해당 사용자에게 적용되는 설정 파일
   - C:\Users\user\.gitconfig 파일
   - `git config --global`를 통해 접근
3. Local (로컬저장소)(기본)
   - 현재 작업중인 저장소의 git 디렉토리
   - 디렉토리\.git\config 파일
   - `git config --local`를 통해 접근
     - 범위 옵션을 지정하지않으면 기본적으로 --local이 적용된다

※각 config에 중복된 설정이 있다면 가장 좁은 범위의 설정이 우선시 된다

---

### 사용자 정보 설정
git을 설치하고 가장 먼저 해야하는 것은 사용자 이름과 이메일 주소를 설정하는 것이다.   
git은 커밋 할 때마다 이 정보를 사용한다.

```
$ git config --global user.name "smith"
$ git config --global user.email smith@email.com
```
`--global`로 설정한 사용자의 정보는 한번만 입력하면 커밋할때 시스템이 해당 정보를 사용한다.   
만약 프로젝트에서 다른 사용자정보를 사용하고 싶다면 `--global` 옵션을 제외하고 새로 입력하면 된다.

---

### git 기본 브랜치명 변경
master <-> main 간 기본브랜치명 변경 이슈도 있고 해서 추가

#### 초기
> 비교적 최근 추가된 명령어
> ```
> git config (--global) init.defaultBranch main
> ```
> 위의 명령어를 통해 기본 브랜치를 main으로 설정할 수 있다.
> 
> **github**   
> repository를 생성시 설정하거나 관련 setting에서 변경해 줄 수 있다.
> ![git_post_1_0](https://user-images.githubusercontent.com/46421475/154085274-f79f9499-636c-4215-a3b7-b34dd6dcb5d1.png)
> 
> ![git_post_1_1](https://user-images.githubusercontent.com/46421475/154085287-bbb0a394-c4fd-4fc9-8888-9dada19e0fd9.png)

#### 브랜치 변경 (나중에 브랜치에서 자세하게)

1. 원격저장소의 브랜치명에 맞춰 `로컬 저장소 브랜치명 변경`
  - 로컬브랜치를 원격브랜치에 연결하고자 한다면 브랜치를 생성하는게 일반적이지만 혹시 브랜치명을 변경하고 싶다면
  - `git branch -m oldbranch newbranch`를 통해 브랜치명을 변경 후 `git fetch`
  - 로컬 - 원격 브랜치명이 같다면 다른 작업없이도 알아서 연결된다.
2. 로컬저장소의 브랜치명에 맞춰 `원격 저장소 브랜치명 변경`       
  - 원격브랜치는 사실 로컬이 반영된 리포지토리이기에 브랜치명을 바꿀 일은 사실 거의 없다.
  - github를 통해 쉽게 브랜치명을 바꾸거나
  - 로컬에서 oldbranch를 삭제하고 newbranch를 만드는 정도의 방법이 있다.

---

### alias

config alias를 통해 명령어에 별칭을 지정할 수 있다.   
```
$ git config alias.co checkout
$ git config alias.br branch
$ git config alias.ci commit
$ git config alias.st status
```
이와 같이 설정하면 `git ci`만으로 커밋 할 수 있다.   

단순 명령어 뿐아니라 `$ git config --global alias.last 'log -1 HEAD'` 처럼 구문자체도 사용할 수 있다.   
개인적인 추리로는 alias를 사용하면 마치 인라인 함수처럼 `log -1 HEAD`(사용하려는 기능)이 `last`(alias) 대신 삽입되어 사용되는게 아닌가 싶다.   

**외부 명령어**   
alias는 git의 명령어 뿐 아니라 외부명령어도 실행 할 수 있다.   
외부명령어는 명령어 앞에 `!`를 붙여 사용하고 명령어도 `''`로 감싸줘야 한다.   
```
$ git config alias.make '!vi'
$ git make somefile.txt
  => vi somefile.txt 와 동일
```

---

\<부록\>    

![git1](https://user-images.githubusercontent.com/46421475/154095411-ea9c5fa1-8d82-404b-a206-923e0afc8fdd.jpg){: .align-center}
<div align="center">  
  마무리 짱구
</div>