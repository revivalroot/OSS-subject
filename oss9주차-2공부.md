# 지역과 원격 저장소 연동 push pull

## 1. 개인 접근 토큰 생성(Personal Access Token)

```
githu는 2021년 8월 13일 이후부터는 기존의 비밀번호 대신 토큰을 사용해서 접근하도록 변경되었음.
따라서 github에서 Personal Access Token을 발급 받아 설정해 주어야 한다.

(1) github에 로그인 후 Settings를 클릭
(2) Developers settings를 클릭
(3) Personal Access Token를 클릭 후 Generate new token을 클릭
(4) 암호 인증 후 범위는 Publish를 선택하고 상황에 따라 Repo, Workflow, gist 정도 선택

-> 이렇게 설정을 해놓으면 후에는 토큰이 표시되지 않음
```

## 2. 깃허브 원격 저장소 수정 후 pull

```
Working Directory에서 add를 통해 stage area에 추가해주고 commit을 통해 Git Local Repository에 보냄
그후 Git Local Repository와 Git Server Repositorty가 Push와 Pull을 하면서 상호작용함

- 윈도 push중 오류
(1) 참조 오류 발생 가능
(2) 인증 오류 발생 가능

- (1) 해결 방법
Windows 환경에서 깃 사용자 계정과 암호 설정 및 변경
1. 제어판 - 사용자 계정 - 자격 증명 관리자
2. Windows 자격 증명
3. 일반 자격 증명
4. git 관련 자격 증명 편집

- (2) 해결 방법
PAT(Personal Access Token)로 연결
$ git push -u https://{token}@github.com/{username}/{reop_name}.git
```

## 3. 지역에서 원격 저장소로 push

```
쓰기 권한이 있어야 push가 가능하다.
- push: 로컬 저장소에 남겨놓은 코드 변경 이력들을 원격 저장소로 전송

$ git push <저장소별칭명> <브랜치명>
ex) $ git push origin topic

- 옵션 -u 사용
최초의 한 번만 저장소명과 브랜치명을 입력하고 그 이후에는 모든 인자를 생략 가능
- $ git push origin topic 에서 성공 이후 -> $ git push

대부분의 경우 로컬 저장소와 원격 저장소에서 동일한 브랜치 이름응 사용하기 떄문에 항상 현재 브랜치를 기준으로 git push 명령어가 작동한다면 매우 편리
- $ git config --global push.default current

- git pull 명령
fetch 명령과 병합하는 merge 명령이 순차적으로 진행

-fetch 명령
원격 저장소의 정보를 로컬 저장소(remote/origin)로 가져오는 명령
명령어: $ git fetch <remote>
ex) $ git fetch origin

fetch한 후 origin/mail, origin/head가 더 최신의 위치에 있음


-merge 명령
변경된 정보를 로컬 저장소의 내용과 병합  **병합: 다른 브랜치의 내용을 합침
깃허브에 내용을 반영하려면 fetch 후 merge 해야함
- $ git merge origin/main
```