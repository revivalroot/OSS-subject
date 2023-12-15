# 파일 비교 diff
## 1. 3 영역 파일 비교 diff

```
✔️ 깃 3 영역의 파일 비교
✔️ 커밋 간의 파일 비교
- HEAD
- HEAD~ HEAD^
~ -> tilde, 틸드, 물결
^ -> caret, 커렛, 모자, 삿갓

- HEAD~~ HEAD~2 HEAD^^ HEAD^~
두개 이전 커밋

- 저장소 하부의 .git 폴더에 정보로 숨겨진 파일
스테이징 영역
깃 (지역) 저장소

- 리눅스 명령어 ls로 보이는 파일
작업 디렉토리의 파일

- 깃 명령 git ls-files로 보이는 파일
스테이징 영역의 파일
```

### 🟠 깃 3 영역의 파일 비교 깃 명령어
```
✔️ 스테이징 영역 기준으로 작업 디렉토리 파일 비교
- $ git diff

✔️ 깃 저장소 기준으로 스테이징 영역 파일 비교
- $ git diff --staged HEAD 
- $ git diff --staged HEAD~

✔️ 깃 저장소 기준으로 작업 디렉토리 파일 비교
- $ git diff HEAD
- $ git diff HEAD~

✔️ 커밋 간의 파일 비교
-> $ git diff 048171 0c747d
-> $ git diff HEAD^ HEAD

```
