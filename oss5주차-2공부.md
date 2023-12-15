# 브랜치 개요와 관리
## 1. 브랜치 개요

### 🟠 브랜치

```
✔️ 실 행활에서 용어

- Branch
나무의 가지, 지점


✔️ 깃 브랜치

• 파일 작성 작업을 하다 보면 여러 파일을 관리하는 폴더를 통째로 복사해 활용하는 일이 자주 발생
• 버전 관리를 수행하던 일련의 파일 집합을 통째로 복사해 독립적으로 다시 개발을 진행하는 개념
- 여러 개발자가 타인을 신경 쓰지 않고 동시에 다양한 작업을 할 수 있게 만들어 주는 기능
- 브랜치를 통해 하나의 프로젝트를 여러 갈래로 나누어서 관리

• 브랜치 병합(merge)
- 독립된 브랜치에서 마음대로 소스 코드를 변경하여 작업한 후 원래 버전과 합칠 수 있음

```

### 🟠 브랜치 병합
```
✔️ 브랜치 사용 장점

- 저장소에서 다른 브랜치에는 영향 없이
• 새로운 기능을 개발하거나 버그를 수정
• 새로운 아이디어를 안전하게 실험 가능


✔️ 브랜치 병합
브랜치와 브랜치를 합치는 수행
```
![image](https://github.com/revivalroot/OSS-subject/assets/127114915/98946a9c-34df-4e7d-8070-f7dc1d40f0be)

### 🟠 브랜치 과정
```
✔️ 브랜치와 HEAD
- 브랜치
커밋 사이를 가볍게 이동할 수 있는 포인터

- HEAD
작업 중인 브랜치의 최신 커밋을 가리키는 포인터
• 필요에 따라 특정 커밋이나 브랜치를 가리키도록 헤드 이동 가능

✔️ 새로운 브랜치 생성

- $ git branch bname
-> 단순히 생성하고 HEAD가 이동은 안함

- $ git switch –c bname
- $ git checkout –b bname
-> 생성하고 새 브랜치로 HEAD 이동도 수행

✔️ 브랜치 확인
- $ git branch: 커밋이 발생한 브랜치 목록 보이기
- $ git branch -v: 브랜치마다 마지막 커밋 ID와 메시지도 함께 표시

✔️ 생성된 새로운 브랜치로 이동
- $ git switch [bname]
- $ git checkout [bname]
-> HEAD를 지정한 브랜치로 이동

- $ git switch -
- $ git checkout -
-> HEAD를 이전 브랜치로 이동

✔️ 분리된(detached) HEAD
- HEAD가 현재 브랜치(마지막 커밋)가 아닌 그 이전 커밋을 가리키는 상태

- $ git checkout HEAD~
현재 브랜치에서 마지막 커밋 이전 커밋으로 이동

- 이동 커밋
상대적인 HEAD~ 또는 HEAD^^, commitID를 사용

• 물결 ~: tilde(틸드)
• 삿갓, 모자 ^; caret(커렛)

```

## 2. 브랜치 관리

```
✔️ 최신 커밋 이전에서 두 브랜치 생성
- $ git switch main
HEAD를 main으로 이동

- $ git checkout HEAD~
HEAD를 하나 이전으로 이동

- $ git switch -c hotfix
브랜치 hotfix 생성하고 HEAD 이동

- $ git checkout –b develop
브랜치 develop 생성하고 HEAD 이동

✔️ 명령 branch에서 옵션 -D 또는 -d를 사용
- 아직 병합되지 않은 브랜치라면 강제로 삭제하기 위해 옵션 -D를 사용

- $ git branch [-d | --delete] [branchName]: 지정한 branchName(이미 병합된)을 삭제
- $ git branch -D [branchName]: 지정한 branchName(병합되지 않더라도)을 삭제

✔️ 브랜치 목록 보기
$ git branch --merged: 현재 작업 브랜치를 기준으로 병합된 브랜치 목록 표시
$ git branch --no-merged: 현재 작업 브랜치를 기준으로 아직 병합되지 않은 브랜치 목록 표시
$ git branch --merged branchName: 인자인 branchName 브랜치를 기준으로 병합된 브랜치 목록 표시
$ git branch --no-merged branchName: 인자인 branchName 브랜치를 기준으로 아직 병합되지 않은 브랜치
```

### 🟠 브랜치 관련 명령 정리
```
- $ git checkout bname
전환, 이동

- $ git switch bname
전환, 이동

- $ git checkout -
이전 브랜치로 전환, 이동

$ git switch -
이전 브랜치로 전환, 이동

$ git branch –h
도움말 보기
```
