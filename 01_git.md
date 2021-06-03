# Git

> 분산 버전 관리시스템



## 준비 사항

* [git bash](https://gitforwindows.org/) (windows 사용하는 경우 필요)



## 기본 문법

### 0. git 저장소 생성

```bash
OUTSHINE@DESKTOP-H5BOGOL MINGW64 /d/TIL/test
$ git init
# 비어있는 git 저장소(repository)에 초기화
# test 폴더(절대경로) .git 폴더
Initialized empty Git repository in D:/TIL/test/.git/
```

* 폴더에 git 저장소를 초기화하면,
  * `.git`폴더가 생성되고
  * bash에는 `(master)`라고 표기
* 주의사항
  * git 저장소 내에 git 저장소를 만들면 안됨
    * `git init` 명령어를 입력할 때, `(master)`가 보이면 절대로 입력하지 말 것



## 1. `add`

```bash
$ git add {디렉토리}
$ git add .			# 현재 디렉토리(하위 디렉토리 포함)
$ git andd a.txt	# 특정파일
$ git add myfolder/	# 특정폴더
```

* `working directory` 상태의 파일을 `staging area` 상태로 변경(첫 번째 통 → 두 번째 통)
* commit을 위한 파일들을 추가하는 명령어

### 예시

```bash
$ touch a.txt		# 파일을 만든다 → 코드 작업을 했다
$ git status
On branch master

No commits yet
# Untarcked files: 트래킹 안된 파일들
# git으로 관리된 적 없는 파일들 (예: 파일생성)
Untracked files:
# git add 명령어를 사용
# commit 될 곳에 포함 → Staging area
  (use "git add <file>..." to include in what will be committed)
        a.txt	# ← 빨간텍스트
# 총평
# nothing added to commit: Commit할 것이 없음(SA X)
# untracked file present: WD O
nothing added to commit but untracked files present (use "git add" to track)
```

```bash
No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        a.txt

nothing added to commit but untracked files present (use "git add" to track)

```

## 2. `commit`

```bash
$ git commit -m '{커밋메시지}'
[master (root-commit) dc90372] Add a.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 a.txt
```



* Commit을 통해서 하나의 버전으로 기록
* Commit 메시지는 현재 변경사항들을 잘 나타낼 수 있도록 작성
* Commit은 고유한 ID인 해시값을 가짐
  * SHA-1 알고리즘에 의해 생성
* Commit 목록은 `git log`명령어를 통해 확인



## 3. `log`

```bash
$ git log
commit dc903721f2a2f3cec37b3abb815470cc565b64c1 (HEAD -> master)
Author: tak <edutak.ssafy@gmail.com>
Date:   Thu Jun 3 15:34:01 2021 +0900
    Add a.txt
$ git log -- oneline	# 한줄로
dc90372 (HEAD -> master) Add a.txt
$ git log -2			# 2개
$ git log -- oneline -1	# 1개를 한줄로
```

## 4. `staus`

* working directory, staging area 공간 파일의 상태를 활용할 수 있다.

```bash
$ git status
On branch master
nothing to commit, working tree clean
```



## 실습1. git 저장소 만들고 루트 커밋 남기기

* practice1이라는 폴더를 바탕화면에 만들고
* README.md라는 파일을 만든 이후
* 첫번째 커밋을 남겨보자!

```bash
$ git init
$ touch README.md
$ git add .
$ git status
$ git commit -m 'ADD README.md'
$ git push origin master
$ git remote add origin https://github.com/webdessin/practice1.git
$ git push -u origin main
```

