Git Hub 협업
===

## **협업 사용자 추가**
### 1. Git Hub 사이트 접속
### 2. Setting 진입
- Manage access 진입
- Invite a Collaboratro 클릭
- 추가할 사용자의 ID나 Email 입력
- 초청 메일이 자동 발송됨 (Copy Invite Link 주소 보내도 OK)
### 3. Permisstion 선택
- Admin : 관리자 권한
- Write : 읽기+수정 권한
- Read : 읽기 권한

<br><br>

## **협업 방식**
### 1. pull : 최신 버전을 다운 받고 작업 시작
### 2. 작업 수행
### 3. add, commit, push : 작업 내용 업로드
### 4. 충돌 발생 시, 파일 수정해서 push
<br><br>

## **협업 충돌 해결 방법**
### 상황 1: push 하는데, 다른 사람이 먼저 push해둔 최신 작업이 있다는 경고
> 해결 : 최신 버전을 pull 받아서 작업한다.

<br>

### 상황 2: pull 받았는데, 동일 파일의 동일 부분이 서로 충돌난다는 경고
> 해결 : 파일을 열어서 충돌나는 부분을 수정후 add, commit, push 한다.
* 충돌 부분을 수정하여 commit하면, 내 작업과 상대의 작업을 Master브랜치에 merge하는 방식으로 작동한다.


<br><br>

## **fetch 란?**
### pull: 원격 저장소의 브랜치를 다운받아서, 로컬저장소의 브랜치에 병합한다.
### fetch: 원격저장소의 브랜치를 다운만 받고 끝.(merge는 따로 해줘야 한다.)

> `git fetch`

> `git merge origin/mater`
##### * 로컬브랜치에 원격저장소(origin)의 master브랜치를 병합하는 명령어.
##### * fetch할 때마다 다운받은 리모트브랜치 정보를 FETCH_HEAD 파일로 만들어 저장하기 때문에, origin/master 대신에 FETCH_HEAD를 대신 써도 된다.