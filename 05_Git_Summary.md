자주 작업하는 내용들 정리
===

### 1. 프로젝트 폴더 생성

<br>

### 2. 로컬 저장소(git repository) 생성 
   >`git init`

   >`git init 경로`

<br>

### 3. 파일 생성(수정)

<br>

### 4. tracked/modified 상태 체크
   >`git status`

<br>

### 5. Staging Area 등록
   >`git add 파일명` : 특정 파일 등록

   >`git add .` : 전체 파일 등록

<br>

### 6. Git Repository에 커밋
   >`git commit`

   >`git commit -m '커밋 메시지'`

   >`git commit -am '커밋 메시지'` : tracked 상태의 파일을 한번에 add, commit

<br>

### 7. 커밋 로그 확인
   >`git log`

   >`git log --graph`

<br>

### 8. 브랜치 생성
   >`git branch` : 브랜치 확인

   >`git branch 브랜치명` : 브랜치 생성


<br>

### 9. 브랜치 전환
   >`git checkout 브랜치명`

<br>

### 10. 브랜치 병합 (순서대로 진행 필요)
   >`git checkout 메인브랜치`

   >`git merge 병합할브랜치`
##### '메인 브랜치'에 '병합할 브랜치'를 merge 한다.
<br>

### 11. 이전 커밋으로 되돌리기
   >`git revert 최신커밋ID` : 최신 커밋 1개 상쇄

   >`git revert 과거커밋ID .. 최신커밋ID` : 여러 커밋 상쇄

   > `git reset --hard 커밋ID` : 삭제

<br>

### 12. 원격저장소(GitHub) 연결
   >`git remote add origin 원격저장소URL.git`

   >`git remote -v` : 연결 상태 확인

<br>

### 13. 원격저장소(GitHub)로 올리기
   >`git push -u 원격저장소별칭 브랜치` : 최초 push할 때

   >`git push 원격저장소명 로컬브랜치`

   >`git push` : 인자를 생략할 수 있음

<br>

### 14. 원격저장소(GitHub)에서 다운받기
   >`git clone 원격저장소URL` : 최초에 다운받을 때

   >`git pull` : 최신변경사항만 다운받을 때

<br>

### 15. 최초 설정 이후 작업 순서
1. pull : 먼저 원격의 최신 버전을 다운 받는다.
2. 작업 : 로컬에서 작업을 한다
3. commit : 작업 내용을 버전으로 등록한다.
4. push : 원격에 올린다.
5. 충돌 해결: 파일에서 충돌난 부분을 직접 수정한다.(쫄지 말자.)