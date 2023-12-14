# 리눅스와 깃 명령어
## 1. 리눅스 명령어

### 🟠 리눅스 명령어
```
- $ pwd 
> Print Working Directory
> 현재 폴더 표시

✔️ $ cd
> Change Directory

✔️ $ mkdir dname
>Make Directory

✔️ $ ls
> File or folder list
> 다양한 옵션
-l: 파일의 상세정보
-a: 숨김 파일 표시
-al: 위 두개를 조합

✔️ 파일 관련 명령: 생성
- $ touch fname
> 빈 파일 fname 생성

✔️ 표준 출력으로 결과 표시 echo
- $ echo git bash
- $ echo ‘print()’
> 이후 문자열을 컴퓨터 터미널에 출력(disply)하는 명령어
> 단순한 문자열은 가능하나 괄호 등이 있는 경우, 작은 또는 큰 따옴표 사용

✔️ $ cat fname
> 파일 내용 보이기

✔️ $ cp a b
> 파일 a를 b로 복사

✔️ $ mv f1 f2
> 파일 f1을 f2로 이름 수정

✔️ 파일 및 폴더 삭제
- $ rm fname
> 파일 fname 삭제

- $ rm –rf dname
> 하부에 서브폴더와 파일이 있어도 폴더 삭제, 옵션 사용
-f : 강제로 파일이나 디렉토리를 삭제
-r : 디렉토리 내부의 모든 내용을 삭제
```

```
✔️ cat (Concatenate)
파일의 내용을 화면에 출력

- cat file1
file1의 내용을 출력

- 파이프(pipe) 기호인 | (vertial var)의 의미
앞 명령의 표준 출력을 뒤 명령의 표준입력으로 처리

- cat file1 file2 | more
file1과 file2의 내용을 페이지별로 출력

- cat file1 file2 | head
file1과 file2의 내용을 처음부터 10번째 줄까지만 출력

- cat file1 file2 | tail
file1과 file2의 내용을 끝에서부터 10번째 줄까지만 출력
```

```
✔️ Redirection 명령어 연산 
- '>' 기호
기존에 있는 파일 내용을 지우고 저장

- '>>' 기호
기존 파일 내용 뒤에 덧붙여서 저장

- '<' 기호
파일의 데이터를 명령에 입력

활용 사례
- echo aaa > a.txt
(새) 파일 a.txt에 문자열 aaa 복사(replace)

- echo bbb >> a.txt
(새) 파일 a.txt에 문자열 bbb 추가

- cat < file1
file1의 결과 출력

✔️ 전체 폴더를 삭제하거나 하부 폴더 .git 삭제
- $ rm –rf .gi
-f : 강제로 파일이나 디렉토리를 삭제
-r : 디렉토리 내부의 모든 내용을 삭제

```