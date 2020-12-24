Git Hub 협업
===

## **협업 사용자 추가**
### 1. Git Hub 사이트 접속
### 2. Setting 진입
### Manage access 진입
### Invite a Collaboratro 클릭
### 추가할 사용자의 ID나 Email 입력
### 초대메일이 가면, Accept 하면 됨
- ##### Copy Invite Link 항목의 주소를 보내줘도 됨
### Permisstion 에서 Admin, Write, Read 를 설정하면 끝

<br><br>

## **협업 방식**
### 1 Step : pull => 최신 버전을 다운 받고 작업 시작
### 2 Step : 작업 시작/종료
### 3 Step : add, commit, push => 작업 내용 업로드

<br><br>

## **협업 충돌 해결 방법**
### 상황 1: push 하는데, 다른 사람이 먼저 push해둔 최신 작업이 있다는 경고
> 해결 : 최신 버전을 pull 받아서 작업한다.

<br>

### 상황 2: pull 받았는데, 동일 파일의 동일 부분이 서로 충돌난다는 경고
> 해결 : 파일을 열어서 충돌나는 부분을 수정후 add, commit, push 하면 된다.
* 내 작업과 상대의 작업을 Master브랜치에 합쳐서 merge하는 방식이라고 보면 될듯.


<br><br>

## **fetch 란?**
### pull: 원격 저장소의 브랜치를 다운받아서, 로컬저장소의 작업 브랜치에 병합까지 해준다.
### fetch: 원격저장소의 브랜치를 다운만 받고 끝.
### fetch한 다음에, merge로 리모트 브랜치를 로컬 작업 브랜치에 병합해 주어야 한다.
> `pull = fetch + merge origin/master`
* origin/master 대신에 git merge FETCH_HEAD 라고 해도 됨
* fetch할 때마다, 다운로드 받은 리모트브랜치 정보를  .git폴더 내부에 FETCH_HEAD 파일을 만들어 저장한다.