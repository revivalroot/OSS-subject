# 지역에서 깃허브 원격 저장소 복제 clone

## 1. 클론(clone)

### 🟠 clone
```    
- 클론(clone)개념
원격 저장소를 지역 저장소에 복제(clone)

- $ git clone [복사된-주소]
원격저장소와 동일한 이름으로 복제

- $ git clone [복사된-주소] [새로운-폴더명]
하부 폴더 [새로운-폴더명] 이름으로 복제

- $ git clone [복사된-주소] .
현재 폴더에 바로 복제
```    

### 🟠 remote
```
- $ git remote
원격 저장소 목록을 보여줌
-> 기본 이름 origin 점검
-> 위에서 clone을 했기 때문에 별칭 origin이 위의 주소가 설정

- $ git remote -v
저장소 주소 등 원격 저장소 정보 목록 표시
```

### 🟠 지역에서 깃허브 원격 저장소 복제
```
(1) 깃허브에서 저장소를 생성하고 그 저장소의 주소를 복사
(2) git에서 $ pwd를 통해 현재 디렉토리를 확인한 후 -> $ git clone 저장소 주소 
(3) 혹은 $ git clone [복사된-주소] [새로운-폴더명] or $ git clone [복사된-주소] . 를 이용해 하부 폴더에 새로운 폴더명으로 저장하거나 현재 폴더에 바로 복사 할 수 있음
(4) $ git remote를 이용해 원격 저장소 이름 목록 확인
(5) $ git remote-v를 이용해 원격 저장소 주소와 이름 목록(상세내용)을 확인 가능
```

### 🟠 원격 저장소 별칭관리
```
- $ git remote add origin URL
원격 저장소 별칭 저장

- $ git remote show origin 
원격 저장소의 모든 브랜치 보기 가능

- $ git remote rename origin org
이름 수정

- $ git remote rn org
삭제
```