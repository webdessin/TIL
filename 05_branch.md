# Branch 명령어

- 브랜치 생성

  ```
  $ git branch 브랜치명
  ```

- 브랜치 목록

  ```
  $ git branch
  ```

- 브랜치 이동

  ```
  $ git checkout 브랜치명
  (브랜치명) $
  ```

- 브랜치 생성 및 이동

  ```
  $ git checkout -b 브랜치명
  ```

- 브랜치 병합

  ```
  (master) $ git merge 브랜치명
  ```

  - `master` 브랜치에 `브랜치명` 을 병합

- 브랜치 삭제

  ```
  $ git branch -d 브랜치명
  ```