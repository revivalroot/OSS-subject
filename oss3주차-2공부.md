# 로그 이력과 과거 여행
## 1. 여러 커밋과 로그 이력

```
🟡 깃 설정과 지역 저장소 생성

✔️ 깃 기초 설정
- $ git config --global user.name elysia: 사용자 이름
- $ git config --global user.email hskang@gmail.com: 전자메일 설정
- $ git config --global core.autocrlf true: 자동 줄바꿈
- $ git config --global core.safecrlf false: 안전 줄바꿈
- $ git config --global core.editor 'code --wait’: 기본 편집기 설정
- $ git config --global init.defaultBranch main: 기본 브랜치 이름 설정

✔️ 깃 저장소에 저장
- $ git add, commit

✔️ 모두 커밋 이력 보기
$ git log
-> --oneline --graph --all -n

✔️ 측정한 커밋 이력 보기
$ git show [HEAD]
-> --oneline

✔️ 로그의 옵션
- 명령 git log
기본적으로 가장 최근의 커밋부터 표시
- $ git log --graph: 문자 그림으로 로그 이력 그리기
- $ git log --reverse: 오래된 커밋부터 표시 --graph와 함께 사용할 수 없음
- $ git log --all: 모든 브랜치의 로그 이력 표시
- $ git log -n: 최근 n개의 로그 이력 표시
```

## 2. 과거 이전 버전으로 이동
```
🟡 버전 이동

✔️ 바로 이전 버전으로 가기
$ git checkout HEAD~
$ git switch –d [이전커밋]

✔️ 다른 브랜치로 이동 
- $ git checkout [branch] 
- $ git switch [branch]

과거로 이동하기 위해서는 작업 영역이 clean 해야함
✔️ 현재 상태를 clean한 상태로 하는 방법
- 임시 저장인 git stash
- 작업 디렉토리와 스테이징 영역의 저장하고 3 영역이 동일한 상태가 되도록

✔️ 다시 최신 버전으로 돌아오기
$ git checkout main

✔️ 다시 checkout 이전으로 돌아오기
$ git checkout -

```