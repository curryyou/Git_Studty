Git Branch
===


## **1. 브랜치란?**
### : Git을 통해 하나의 파일을 A버전, B버전 등으로 다양한 분기하여 만들 수 있다. ***각 버전들을 브랜치라고 한다.***
### : 즉, 특정 시점의 커밋(Base)부터 분기하여 독립적으로 관리하는 버전들의 갈래
### : 공통적인 작업을 하다가 새로운 시도를 해보거나, 다양한 버전을 만들어볼 필요가 있을 때, 브랜치를 만들어서 관리한다.

<br><br>

## **2. 브랜치 확인 : branch**
### : 현재 생성되어 있는 브랜치 목록 확인
> `git branch`

<br><br>

## **3. 브랜치 생성 : branch**
### : 현재 커밋(버전)부터 브랜치 생성
> `git branch 브랜치명`
##### 브랜치를 생성하기만 한다(해당 브랜치로의 전환은 별도로 해주어야 한다.)
##### 분기의 시작점이 되는 버전을 Base라고 한다.

<br><br>

## **4. 브랜치 전환 : checkout**
### : HEAD가 가르키고 있는 브랜치를 다른 브랜치로 변경한다.
### : 브랜치가 전환되면, Working Tree 도 해당 브랜치 환경으로 전환된다.
> `git checkout 브랜치명`

### : 브랜치 생성과 전환을 동시에 하려면 다음 명령어를 쓴다.
> `git checkout -b 브랜치명`


<br><br>

## **5. 브랜치 삭제: branch -D**
> `git branch -D 브랜치명`
#### 주의) 대문자 D로 써야한다.

<br><br>

## **6. 브랜치 병합 : merge**
### 여러 브랜치들을 병합하면, Git이 자동으로 적절하게 병합해준다.
### 병합이 불가한 경우, 어떤 부분 때문인지 알려주며, 직접 수정해주면 된다.(conflict)

<br>

### **# 병합 작업 순서**
### 1 step : 메인 브랜치로 전환
> `git checkout master`

### 2 step : 브랜치 병합 (메인 브랜치에 다른 브랜치를 병합)
> `git merge 병합할브랜치`

##### 병합도 커밋(merge commit)이므로 커밋 메시지 작성 필요.

<br>

### **# 병합 케이스**
### 1. 서로 다른 파일 수정 후, 병합 : Git이 자동으로 병합해줌
### 2. 같은 파일의 다른 위치 수정 후, 병합 : Git이 자동으로 병합해줌
### 3. ***같은 파일의 같은 위치 수정 후, 병합 : 충돌(CONFLICT) 발생***
1. 충돌난 파일 열기: git이 충돌난 부분을 파일에 표시해준다.
2. 직접 파일 수정: 충돌난 부분을 직접 수정한다.
3. 스테이징 등록: `git add 파일명`
4. 커밋: `git commit`  
5. 해결 완료!

<br><br>

## **7. 충돌과 3-way merge**
### 특정 분기점에서 시작한 두개의 브랜치를 병합할 경우,
### 1. 분기점(base)에서의 상태
### 2. 첫번째 브랜치의 상태
### 3. 두번째 브랜치의 상태
### 를 비교하여, base 기준으로 수정된 내용을 우선으로 병합한다.
##### (특정 부분을 수정한 브랜치와, 수정하지 않은 브랜치가 있다면, 수정된 내용을 우선 반영한다는 의미.)
### 만약 여러 브랜치가 '같은 파일의 같은 부분'을 수정한 경우, Conflict 발생
### => 이 부분은 수동 수정 필요


<br><br>

## **8. Branch, HEAD, checkout 정리**

> ## ***HEAD -> 브랜치 -> 최신커밋ID***

### **# Branch**
1. Repository 생성시, Master브랜치가 만들어진다.
2. 브랜치는 마지막 커밋을 가르키고(pointing) 있다.
3. checkout 명령어로 작업중인 브랜치를 전환할 수 있다.

### **# HEAD**
1. Respository 생성시, HEAD도 만들어진다.(.git폴더 내부에 파일로도 생성됨)
2. 현재 작업 중인 브랜치를 가르키며(pointing), 최초에는 Master브랜치를 가르킨다.
3. checkout 명령어로 HEAD가 가르키는 브랜치를 변경할 수 있다.

### **# checkout**
1. HEAD가 가르키는 브랜치를 전환하는 명령어이다.
2. HEAD가 다른 커밋ID를 가르키게도 할 수도 있다


