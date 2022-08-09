# Git 설정

## **Git이란?**

### **_파일의 이력과 버전을 관리해주는 시스템_**

### 특정 디렉터리에 Git을 설정해두면,

1. ### 파일의 과거 버전으로 쉽게 돌아갈 수 있다.
2. ### 파일을 여러 버전으로 분기하여 작업할 수 있다.

#### \* Git이 설정된 디렉터리를 저장소, 레퍼지터리(Repository)라고 부른다.

#### \* Git이 설정된 디렉터리에는 .git폴더가 만들어지고, 파일의 이력과 버전을 관리하는 파일들이 생성된다.

<br><br>

## **Git의 원리**

### **1. .git 폴더 저장소**

- 파일의 작업 이력과 버전들은 모두 .git폴더 내부에 저장된다.
- 소스코드 뿐만 아니라, 텍스트, 이미지 파일 등도 가능하다.

### **2. 작업 이력**

- 파일을 수정할 때마다 작업 이력이 .git폴더 내부에 차곡차곡 저장된다.
- 나중에 과거 버전으로 돌아가는 명령을 하면, .git폴더 내부에서 과거 버전을 찾아준다.
- 파일 수정 이력을 저장하는 명령을 commit이라고 한다.

### 3. **분기 작업** :

- 원본은 그대로 둔채, A버전, B버전 등으로 분기하여 작업할 수 있다.
- 언제든지 원본, A버전, B버전을 전환하며 작업할 수 있다.
- 원본, A버전, B버전을 각각 브랜치(Branch)라고 부른다.

<br><br>

## **Git 설치**

### 1. 설치 확인

> `git --version`

### 2. 설치 방법

https://git-scm.com/ 에 접속해서 다운/설치 한다.

<br><br>

## **사용자 설정**

### 1. 글로벌 사용자 설정 ( 전체 디렉터리에 적용: **_추천_** )

> `git config --global user.name = '사용자 이름'`

> `git config --global user.email = '이메일 주소'`

<br>

### 2. 로컬 사용자 설정 ( 특정 디렉터리만 적용 )

> `git config user.name '사용자 이름'`

> `git config user.email '이메일 주소'`

##### \* 설정내용 확인방법: `git config --list`

<br><br>

## **Git 설정(초기화): init**

### 특정 디렉터리를 Git Repository로 만든다.

> `git init 경로`

> `git init`

##### \* 경로 생략시, 현재 디렉터리를 Repository로 설정한다.

##### \* 디렉터리 내부에 .git 숨김 폴더가 만들어진다.

##### \* git 삭제방법 : `rm -rf .git`

<br><br>

## **Git 관리대상 제외: .gitignore**

### 특정 폴더나 파일을 Git의 관리대상에서 제외할 수 있다.

1. .gitignore 파일을 만든다.
2. 제외할 대상들(경로, 파일 등)을 적어둔다.
   - #### 특정 파일 제외 : a.txt
   - #### 특정 확장자 제외 : \*.txt
   - #### 특정 폴더 제외 : build/
   - #### 특정 폴더의 특정 확장자 : build/.txt
3. .gitignore 이 안 먹을 땐, git의 캐시를 삭제해주면 된다. \* `git rm -r --cached .`
   <br><br>

## (참고) 각종 설정 관련 내용

### 1. 설정파일 편집방법

> `git config --global -e`

### 2. VSCode를 기본 에디터로 설정

1. VSCode의 Command Palette(Comand + Shift + P) 실행 후

   > Shell command: Install 'code' command in PATH 설정

2. git 설정파일의 core.editor 설정
   > `git config --global core.editor "code"`

### 3. 캐리지리턴 맞춤 설정

> `git config --global core.autocrlf input` : 맥

> `git config --global core.autocrlf true` : 윈도우

### 4. 명령어 별칭 설정

> `git config --global alias.st status`

##### \* git st 만 입력해도, git status가 실행됨

<br><br>

## (참고) 기타 명령어

### 1. 명령어별 옵션 확인

> `git 명령어 -h`

### 2. 디렉터리 내부 파일 확인

> `ls` : 폴더 내부 표시

> `ls -l` : 폴더 내부 자세히 표시

> `ls -a` : 폴더 내부 표시(+숨김 파일 포함)

> `ls -al` : 폴더 내부 자세히 표시(+숨김 파일 포함)
