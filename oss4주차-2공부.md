# 파일삭제rm과복원restore
## 1. 파일 삭제 rm
- 소스 코드의 공개를 뜻하는 용어
- 소스 코드가 공개적으로 접근할 수 있게 설계
- 누구나 자유롭게 확인, 수정, 개작, 재배포 가능
- 저작권자의 권익을 보호할 수 있도록 제도화된 소프트웨어
```
✔️ 리눅스 명령 파일 삭제

- $ rm [file]
작업 디렉토리와 스테이징 영역에서 모두 file 삭제
-> 다음 커밋에서 지정한 file을 삭제하겠다는 의미
-> Tracked 상태의 파일을 제거하여 Untracked 상태로 만듦

- $ git rm –-cached [file]
스테이징 영역에서 file 삭제 -> 작업 디렉토리에서는 삭제되지 않음
$ git Is-files 결과에서 보이지 않음 -> 기본적으로 스테이징 영역의 파일 목록을 표시

✔️ 작업 디렉토리에서 파일 삭제
$ rm f

✔️ 작업 디렉토리와 스테이징 영역에서 파일 삭제
- $ git rm g

✔️ 스테이징 영역에서만 파일 삭제
$ git rm --cached f

- $ git commit –m ‘Delete g’
$ git commit –m ‘Delete g’ 커밋 후 파일 g가 삭제된 상태에서 커밋
-> 이전 커밋과 차이는 g가 삭제된 것, 커밋 이후 log show

** ??은 Untracked를 의미하며 스테이징 영역에서 파일이 삭제되어 추적되지 않는 파일이 된 상태임
** 배시에서 녹색은 스테이징 영역의 표시이며 깃 저장소와 비교해 삭제됨을 의미
```

## 2. 파일 복원 restore
### 🟠 3 영역에서 파일 f가 모두 다른 상태
![image](https://github.com/revivalroot/OSS-subject/assets/127114915/51fe5f17-9b8d-486d-a448-ac840afa10e7)
```
✔️ 작업 디렉토리의 파일 f를 스테이징 영역의 파일 상태로 복구
- 작업 디렉토리에 있던 f 내용이 사라지므로 유의
- 3 영역에서 파일 f가 작업 디렉토리와 스테이징 영역이 같은 상태가 됨
- $ git restore f

✔️ 깃 저장소의 최신 커밋 상태의 파일 f를 스테이징 영역에 복구
- 3 영역에서 스테이징 영역의 파일 f가 깃 저장소 영역과 같은 상태가 됨
- $ git restore --staged f

✔️ 깃 저장소의 최신 커밋 상태의 파일 f를 작업 디렉토리와 스테이징 영역에 한번에 복구
- 파일 f가 현재 커밋 상태의 내용으로 작업 디렉토리와 스테이징 영역 모두 같은 상태가 됨
- $ git restore --source=HEAD --staged --worktree f

✔️ 깃 저장소의 최신 커밋 상태의 파일 f를 작업 디렉토리에 복원
- 파일 f가 현재 커밋 상태의 내용으로 작업 디렉토리에 복사되어 동일하게 됨
- $ git restore --source=HEAD f
- $ git restore --source=HEAD --worktree f


✔️ 깃 저장소의 최신 커밋 상태의 파일 f를 스테이징 영역에 복구
- 3 영역에서 스테이징 영역의 파일 f가 깃 저장소 영역과 같은 상태가 됨
- $ git restore --source=HEAD^ --staged [file]


** -staged는 –S, --worktree는 –W, 짧게 가능(둘 다 대문자)
```
