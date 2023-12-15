# 깃 커밋과 로그
## 1. 버전관리를 위한 add, commit 명령


```
🟡 깃 3 영역

✔️ 작업 영역
- working directory(folder), working tree
- 탐색기 상의 폴더 하부

✔️ 스테이징 영역
- staging area, index
- 저장소의 .git 폴더의 파일 index

✔️ 깃 저장소(git repository)
- 저장소
- 저장소의 .git 폴더의 여러 정보

```

```
✔️ 파일 생성 후 add, commit 수행

- $ git add
파일을 Working tree => Staging Area로 이동(복사)

- $ git commit
Staging Area에 준비된 파일 => Git repository(버전관리)로 이동(복사)

✔️ 깃 상태 보기
- 명령 git status
$ git status: [--long] 현재의 상태 표시, 기본 값(default value)
$ git status: [--short | -s] 현재의 상태를 간단히 표시
$ git config --global --edit:  도움말 보기

```

```
✔️ 파일 생성
- 리눅스 명령 echo와 수정 라다이렉션(redirection) > 또는 추가 라다이렉션 >>를 사용

ex) 
$ echo create > hello.txt
$ cat hello.txt
create

✔️ untracked file
- 처음 만들어진 파일
- 추적되지 않는 파일(untracked file)
-> 커밋에 포함시키려면 “git add <file> …” 사용

✔️ 커밋
- 커밋(commit)
버전 관리를 위해 현재 스테이지 영역의 내용에 대해 스냅샷(snap shot)을 찍는 명령
즉 커밋으로 버전 관리를 위해 인덱스에 추가된 파일들의 현재 상태를 저장

- $ git commit: 커밋 메시지를 입력할 기본 편집기 실행됨
- $ git commit -m ‘message': 커밋 메시지를 직접 입력 [-m | --message]
- $ git commit -a -m ‘message' or $ git commit -am ‘message'
-> 추가와 커밋을 함께 실행 [-a | --all]

✔️ nothing to commit, working tree clean
- 커밋할 것은 없고, 작업 트리는 깨끗한(clean) 상태
- 3 영역이 동일한 상태
```

## 2. 버전 로그 이력 확인
### 🟠 log
```
✔️ $ git log
- $ git log: 로그 이력 정보를 표시
- $ git log: --oneline 로그 이력을 한 줄로 표시
- $ git log [--patch | -p]: 로그 이력과 함께 파일의 변화(이전 커밋과의 차이)를 표시

✔️ 옵션 --oneline
- 한 줄로 간략히 표시
- 커밋 ID 일곱자리, (마지막 커밋 HEAD -> 브랜치이름), 커밋 메시지 제목

✔️ 옵션 --patch 또는 -p
커밋 정보 뿐 아니라 이전 커밋과 현재 커밋 파일의 차이가 표시

✔️ 커밋 정보 git show
- $ git show: 마지막 커밋(HEAD)의 커밋 정보 표시
- $ git show: --oneline 커밋 로그 한 줄과 파일 차이 표시
- $ git show: -s 파일 차이는 표시되지 않음
- $ git show [HEAD]: 지정한 HEAD의 커밋 정보 표시
- $ git show [commitID]: 지정한 commitID의 커밋 정보 표시

인자가 없으면 HEAD가 생략, 가장 최근 커밋의 정보와 함께 이전 버전과의 파일 차이 diff가 표시
```



