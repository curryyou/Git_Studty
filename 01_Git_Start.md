Git 기본 명령어
====
## 1. git init
#### 디렉터리를 git을 통해 관리하라고 설정
#### .git 숨김 폴더에 git repository가 생성됨
#### git repository에 모든 파일 변경의 역사가 저장됨
>`git init 경로`
##### *참고) 경로를 생락하면 현재 경로에 git repository 생성*
##### *참고)`ls -al` : .git 숨김폴더 확인 명령어*
##### *참고)dot ( . ) 은 현재 경로를 의미*

<br><br>

## 2. 세가지 상태
| Working Tree | Staging Area | Repository |
|:------------:|:------------:|:----------:|
|생성/수정된 파일들|버전을 생성할 후보|실제 버전으로 저장|

<br>

### Git은 파일을 세가지 영역으로 구분하여 관리한다.
> `git status`: Working Tree, Staging Area 의 상태 확인 명령어
##### -s, -v, -b 등의 옵션 제공


<br><br>

## 3. Staging 추가 : add
### 1) Git은 처음 생성된 파일들을 관리하지 않는다 : untracked 상태
### 2) Staging Area에 넣어 커밋 후보군으로 등록해줘야 관리를 시작한다 : tracked 상태
> `git add 파일명` : Staging Area에 파일 추가

<br><br>

## 4. Repository 추가 : commit
### Staging Area에 있는 파일들을 Repository로 commit해줘야 버전을 갖게 된다.
> `git commit` : Respository에 버전 등록

> `git commit -m '메시지'` : 커밋메시지와 함게 Respository에 버전 등록

##### `git commit` 은 Staging Area에 있는 **'모든 파일들'** 을 Repository로 등록하여 버전을 생성한다. 


<br><br>

## 5. 파일 수정
### tracked 되고 있는 기존 파일이라도, 
### 수정이 발생하면 **modified** 상태가 되면서 Working Tree 에 들어간다.
### 다시 Staging Area 등록하여 커밋 후보군으로 올려주고,
### Commit 해주면 새로운 버전으로 저장된다.
> `git add 파일명`

> `git commit -m '메시지'`

<br><br>


## 6. 커밋 로그 확인
### 커밋 이력을 확인할 수 있다.
> `git log` : 기본 커밋 이력

> `git log --p` : 변경된 상세 이력(차이점)

> `git log --stat` : 연관된 파일을 보여줌

> `git log --graph --all --decorate` : 그래프로 보여줌

<br><br>

## 7. 버전간 차이점 확인
### 파일을 수정했을 때,
### commit 된 마지막 버전과의 차이를 확인할 수 있다.
> `git diff`

<br><br>

## # 작업 순서 정리
### 1. 프로젝트 폴더 생성

### 2. git repository 생성 
   >`git init`

### 3. 파일 생성(수정)

### 4. Staging Area 등록
   >`git add 파일명`

### 5. Git Repository에 커밋
   >`git commit -m '커밋 메시지'`

### 6. 커밋 로그 확인
   >`git log`







