Git Backup
===
## 백업?
### : 내컴퓨터에 저장된 파일과 버전이력 등을 다른 컴퓨터, 클라우드 등에 올려두고 안전하게 관리하는 개념
<br><br>


## 지역저장소, 원격저장소
### 1. 지역 저장소(Local Repository): 내컴퓨터에 저장된 Git Repository
### 2. 원격 저장소(Remote Repository): 원격 서버에 저장된 Git Repisitory
##### 주로 Git Hosting 을 말한다.(Git Hub, Git Lab 등)

<br><br>

## **원격저장소 이용방법**
### 1. Git Hosting 사이트(Git Hub, Git Lab 등) 가입/로그인
### 2. Repository(저장소) 생성

<br><br>

## **원격저장소 연결**
### 1. 지역저장소를 원격저장소에 연결(HTTP 기준)
>`git remote add 원격저장소별칭 원격저장소URL`
* ##### 원격저장소별칭은 'origin'을 관습적으로 많이 사용함.(다른 것도 상관 없음)

### 2. 연결 여부 확인
> `git remote`

> `git remote -v`

### 3. 최초 업로드(upstream setting)
> `git push -u 원격저장소별칭 브랜치명`

> `git push -u origin master`: 관습적으로 origin을 원격저장소의 별칭으로 많이 사용함
* ##### Git Hub 의 아이디/비밀번호 입력 필요
* ##### '업스트림 세팅'은 로컬의 브랜치를 원격의 브랜치가 tracking하게 설정하는 개념.
* ##### 다음부터 push 명령어에 인자 생략하여 사용 가능


<br><br>

## **업로드: push**
### : '로컬저장소'의 파일, 버전이력들 => '원격저장소'로 업로드
* ##### 내 컴퓨터에서 작업한 내용을 commit하고, GitHub에 push하여 백업해두는 느낌
> `git push 원격저장소별칭 브랜치`

> `git push`

<br><br>

## **다운로드: clone**
### : '원격저장소'의 파일, 버전이력들 => '지역저장소'로 다운로드
> `git clone 원격저장소URL (option: 디렉터리명)`
* ##### 명령어를 실행한 경로에 '디렉터리' 까지 함께 다운로드 됨
* ##### GitHub에 저장된 내용을 ***'최초로'*** 다운로드 받을 때 사용(.git까지 모두 다운로드 됨)


<br><br>

## **땡겨오기: pull**
### : '원격저장소'의 최신 변경사항만 => '지역저장소'로 다운로드
> `git pull`
* ##### ***clone 이후***, 최신버전만 다운로드 받을 때 사용
* ##### 다른 컴퓨터에서 push한 내용이나, GitHub사이트 상에서 수정한 내용을 다운 받을 때 사용

<br><br>

## **GitHub에서 오픈소스 다운로드 방법**
1. ### zip 파일 다운로드
2. ### clone HTTPS원격저장소URL

