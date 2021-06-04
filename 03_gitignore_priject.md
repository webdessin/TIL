# 프로젝트 기본

예시는 아래 django 프로젝트를 기준으로 함

![image-20210604101052306](D:/git/TIL/md-images/image-20210604101052306.png)



## Git 저장소 설정

```bash
$ git init
```



## gitignore

> git으로 관리하지 않을 파일 / 폴더 등을 관리

* `.gitignore` 파일을 만들어서 관리

```bash
user.csv	# 특정 파일
venv/		# 특정 폴더
*.csv		# 특정 확장자
```

* 개발 프로젝트시 어떤 것들을 gitignore로 관리를 하는가?
  * OS(운영체제)에서 활용되는 파일들 
  * IDE(통합개발환경 - pycharm), Text editor(vs code) 등에서 활용되는 파일 
    * 예) pycharm -> .idea/
  * 개발 언어(python) 혹은 프레임워크(django)에서 사용되는 파일
    * 가상환경 - `venv/`
    * `__pycache__/` ...

![image-20210604101521527](D:/git/TIL/md-images/image-20210604101521527.png)

![image-20210604102556118](D:/git/TIL/md-images/image-20210604102556118.png)



### gitignore.io

* [링크](https://gitignore.io)

* 본인 개발 환경에 대한 내용을 넣고 생성하면, 일반적으로 개발자들이 많이 쓰는 gitignore 문서를 제공한다.

* 혹은, github에서 제공하는 문서들을 받아서 활용해도 좋다. 

  [링크](https://github.com/github/gitignore) [파이썬 링크](https://github.com/github/gitignore/blob/master/Python.gitignore)

![image-20210604101917056](D:/git/TIL/md-images/image-20210604101917056.png)

## 실습3. Githup Profile README



### 내용

* 로컬에 github username - ex) edutak으로 폴더를 만든다.
* 안에 README.md 파일을 만든다.
  * 내용으로 자기소개를 작성한다.
* 커밋을 한다.
* Github에 github username으로 원격 저장소를 만든다.
* Push를 한다.



# 자주하는 실수 모음

## submodule => git 속 git

![image-20210604091558961](D:/git/TIL/md-images/image-20210604091558961.png)

* 가끔 Github에 폴더에 화살표가 있을 때

  * => Git 저장소 내부에 Git 저장소가 있는 경우  

* 솔루션 : submodule 형식으로 활용할 수는 있지만, 처음에는 복잡하게 가지말자!

  ![image-20210604092118640](D:/git/TIL/md-images/image-20210604092118640.png)

## 경로 공백 처리

* `마크다운_문법.md` 



## 약속

* git 명령어는 항상 .git 폴더가 있는 곳에서 하자!

* git 저장소로 활용되는 폴더에 다른 git 저장소를 옮기지 말자!


## 커밋 없는 경우

![image-20210604100322069](D:/git/TIL/md-images/image-20210604100322069.png)

* 커밋이 없어서 push할 수가 없음. 혹은 브랜치가 없다.
* remote 설정은 되어 있는 것을 확인할 수 있음.



## 가능? 불가능?

### 1. TIL 폴더명 바꿔도 되나요? .git 의 상위폴더! => O 바꿔도됨! 전혀 상관 없음

![image-20210604093246731](D:/git/TIL/md-images/image-20210604093246731.png)

* 폴더 이동도 자유롭게 해도 되지만, 항상 이동할 때 해당 폴더가 다른 git 저장소인지 체크는 할 필요가 있다!
* 프로젝트 폴더 이름이 바뀌는 것은 커밋과 상관이 없다.

## 2. 원격저장소 이름이랑 로컬 폴더 이름은 같아야 할까요? =>  X

원격 저장소 이름이랑 로컬 폴더 이름은 전혀 상관이 없습니다.

그러면 상관이 있는 것은 무엇일까요?

```bash
$ git remote -v # 원격 저장소 정보 조회 
```

그리고 정보만 기록되어 있어서 `clone` `pull` `push` 등의 명령어를 입력할 때 활용되는 것이지, sync가 되어 있는 것은 아니다!

