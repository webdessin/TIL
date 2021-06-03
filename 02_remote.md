# 원격 저장소(remote repository) 기초



## 기본 설정

* 로컬 git 저장소
* Gitup remote repository를 생성



## 명령어

### 원격 저장소 설정

```bash
$ git remote add origin 저장소 URL
```

* 깃(git), 원격저장소(remote) 추가해줘(add) origin이라는 이름으로 저장소 URL에
  * origin은 원격저장소 이름
* origin이라는 이름으로 저장소 URL에 원격저장소를 추가



### 원격 저장소 목록 보기

```bash
$ git remote -v
origin https://github.com/webdessin/practice1.git (fetch)
origin https://github.com/webdessin/practice1.git (push)
```



### 원격 저장소 설정 삭제하기

```bash
$ git remote rm origin
```

* 깃(git), 원격저장소(remote) 삭제해줘(rm: remove) origin을



### push

```bash
$ git push origin master
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 217 bytes | 217.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/edutak/practice1.git
 * [new branch]      master -> master
```

* 깃(git), 푸쉬해줘 origin 원격 저장소에 master 브랜치!



## 실습2. TIL 폴더 만들고 원격 저장소에 올리기

### 주의사항

기존의 TIL폴더에 `git`폴더가 있는 경우 지우고 진행

원격 저장소도 기존에 TIL 이름으로 만든 경우에는 다른 이름으로 진행



### 실습

1. 로컬에 TIL 폴더를 만들고, 오늘 작성한 마크다운 파일을 옮긴다.
2. 커밋
3. 원격 저장소에 TIL이라고 만들고, push한다.
   * 원격 저장소도 기존에 TIL 이라는 이름으로 만든 경우에는 다른 이름으로 저장
4. 다 올라갔으면, 구글 스프레드 시트에 URL 기록



### 추가 실습 (선택)

* 지금까지 배운 내용들을 TIL폴더에 하나씩 기록해보고,
* 추가 커밋과 push를 해본다.