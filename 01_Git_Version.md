Git 기본 명령어
====
## 1. git init
#### 특정 디렉터리를 git을 통해 관리하라고 설정하는 명령어
#### .git 숨김 폴더에 git repository가 생성된다.
#### git repository에는 파일들의 변경 '역사'가 저장된다.
>`git init 경로`
##### *참고) 경로를 생락하면 현재 경로에 git repository 생성*
##### *참고)`ls -al` : .git 숨김폴더 확인 명령어*
##### *참고)dot ( . ) 은 현재 경로를 의미*

<br><br>

## 2. 세가지 상태
### Git은 파일을 세가지 영역으로 구분하여 관리한다.
| Working Tree | Staging Area | Repository |
|:------------:|:------------:|:----------:|
|생성/수정된 파일들|버전을 생성할 후보들|실제 저장된 버전들|
<br>

#### 1. 워킹 트리 : 파일을 작업(생성/수정)하는 환경.워킹 디렉터리라고도 한다.
##### 그냥 내가 작업하는 폴더 공간과 비슷한 개념이다.
##### 이 상태의 파일들은 git이 관리하지 않는다.(untracked상태)
#### 2. 스테이징 : 작업한 파일들을 버전으로 만들기 위해 후보로 올려두는 공간
##### 이때부터 git이 관리하기 시작한다.(tracked상태)
##### tracked 상태가 된 파일에 변경사항이 발생하면 git이 모두 파악한다.
#### 3. 레포지터리 : 실제로 commit을 수행하여 버전으로 등록하여 저장하는 공간

<br>

> `git status`: Working Tree, Staging Area 의 상태 확인 명령어
##### -s, -v, -b 등의 옵션 제공


<br><br>

## 3. Staging 추가 : add
### 1) Git은 처음 생성된 파일들을 자동으로 관리하지 않는다 : untracked 상태
### 2) Staging Area에 넣어 커밋 후보군으로 등록해줘야 관리를 시작한다 : tracked 상태
> `git add 파일명` : Staging Area에 파일 등록

> `git add .` : Working Tree에 있는 모들 파일을 Staging Area에 등록


<br><br>

## 4. Repository 추가 : commit
### : Staging Area에 있는 파일들을 commit 해주어야, Repository에 버전으로 저장된다.
> `git commit` : Respository에 버전 등록(에디터로 커밋 메시지 별도 작성 필요)

> `git commit -m '메시지'` : '커밋메시지'와 함께 Respository에 버전 등록

> `git commit -am '메시지'` : tracked된 모든 파일의 add와 commit 동시 수행 *(최초 생성된 untracked 파일은 불가)*

##### `git commit` 은 Staging Area에 있는 **'모든 파일들'** 을 Repository로 등록하여 버전을 생성한다. 
##### `git --amend` 나 `git --amend -m '메시지'`로 마지막 커밋의 메시지를 수정할 수 있다.

<br><br>

## 5. 파일 수정
### tracked 되고 있는 기존 파일들은, 
### 수정이 발생하면 ***modified*** 상태가 되면서 다시 Working Tree 에 들어간다.
### 다시 Staging Area 등록하여 커밋 후보군으로 올려주고,
### Commit 해주어야 새로운 버전으로 저장된다.
> `git add 파일명`

> `git commit -m '메시지'`

<br><br>


## 6. 커밋 로그 확인
### 커밋 이력을 확인할 수 있다.
> `git log` : 기본 커밋 이력

> `git log --p` : 변경된 상세 이력(차이점)

> `git log --stat` : 연관된 파일을 보여줌

> `git log --oneline` : 한줄로 제목만 보여줌

> `git log --all` : 모든 브랜치의 로그를 보여줌

> `git log --decorate` : Branch, HEAD 정보도 보여줌

> `git log --graph` : 그래프로 시각적으로보여줌

<br><br>

## 7. 버전간 차이점 확인 : diff
### 파일을 수정했을 때,
### commit 된 마지막 버전과의 차이를 확인할 수 있다.
> `git diff`

<br><br>

## 8. 과거 버전 '확인' : checkout
### checkout 명령어를 통해 HEAD가 과거의 특정 커밋을 가르키게 하면, Working Tree가 해당 버전의 모습으로 돌아간다. 
> `git checkout 커밋ID`
##### *과거로 돌아가도, 최신 커밋은 그대로 남아있다. HEAD만 과거로 이동할 뿐!*

### 다시 최신 커밋으로 돌아가려면 HEAD가 특정 브랜치를 가르키도록 하면 된다.
> `git checkout master`
##### _참고) 원래 checkout은 브랜치를 변경하는 용도로 주로 사용한다._

<br><br>

## 8. 커밋(버전) 삭제 : reset
### 특정 버전 '이후'의 커밋들을 삭제한다.
### 살아남은 특정 버전이 최신 상태의 커밋이 된다.
> `git reset --hard 커밋ID`
##### 최신 버전들을 삭제해서 과거로 돌아가는 과격한 방법이다.

<br><br>

## 9. 커밋(버전) 상쇄 : revert
### 최신 커밋을 상쇄시켜서 ***그 전의 상태로 되돌리는*** 커밋을 수행한다.
### 즉, 새로운 커밋을 만들어서 과거 상태와 동일하게 만든다.

> `git revert 커밋ID` : '커밋ID'를 상쇄시키는 커밋이 수행된다. => '커밋ID'의 ***바로 전 단계***와 동일한 상태가 된다.

> `git revert HEAD` : 직전 커밋만 상쇄시킬때는 HEAD를 사용해도 된다.

> `git revert 과거커밋ID .. 최신커밋ID` : 범위 연산자를 통해 여러 커밋 상쇄
##### *여러 단계 전의 과거로 돌아가려면, 최신 커밋부터 역순으로 하나씩 revert해주어야 하지만, 위의 범위 연산자를 활용해도 된다.*

##### 새로 커밋하는 명령이므로, 커밋 메시지를 작성하는 창이 뜬다.
##### 아무런 커밋도 삭제되지 않으므로 reset보다 안전하게 과거로 돌아가는 방법이다.

<br><br>

## # 자주 작업하는 내용들 정리.
### 1. 프로젝트 폴더 생성

### 2. 로컬 저장소(git repository) 생성 
   >`git init`

### 3. 파일 생성(수정)

### 4. tracked/modified 상태 체크
   >`git status`

### 5. Staging Area 등록
   >`git add 파일명`

### 6. Git Repository에 커밋
   >`git commit -m '커밋 메시지'`

   >`git commit -am '커밋 메시지'` : tracked 상태의 파일은 한번에 add, commit 가능

### 7. 커밋 로그 확인
   >`git log`

### 8. 브랜치 생성
   >`git branch 브랜치명`

### 9. 브랜치 전환
   >`git checkout 브랜치명`

### 10. 브랜치 병합
   >`git checkout 메인브랜치`

   >`git merge 병합할브랜치`

### 11. 이전 커밋으로 되돌리기(상쇄)
   >`git revert 이전커밋ID6자리`

### 12. 원격저장소(GitHub) 연결
   >`git remote add origin 원격저장소URL.git`

### 13. 원격저장소(GitHub)로 올리기
   >`git push -u 원격저장소별칭 브랜치` : 최초 push할 때

   >`git push 원격저장소명 로컬브랜치`

   >`git push` : 인자를 생략할 수 있음

### 14. 원격저장소(GitHub)에서 다운받기
   >`git clone` : 최초에 다운받을 때(커믹이력이 저장된 git repository 포함)

   >`git pull` : 변경사항만 다운받을 때

### 15. 최초 설정 이후 작업 순서
1. pull : 먼저 원격의 최신 버전을 다운 받는다.
2. 작업 : 로컬에서 작업을 한다
3. commit : 작업 내용을 버전으로 등록한다.
3. push : 원격에 올린다.



