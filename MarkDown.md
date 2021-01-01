**\# MarkDown 문법 정리**
===
#### [깃허브 마크다운 가이드 링크](https://guides.github.com/features/mastering-markdown/ "링크 이동")

---

<br><br>

# **1. 샵(#)**
### 샵(#)을 여러개 써서 헤더 태그를 표현할 수 있다.
### 밑줄 표현 여부는 뷰어에 따라 다른듯 하다.
<br>

#### &nbsp; <span style="color:skyblue"><마크다운><span>
```
# 의 갯수에 따라 헤더 문장 크기가 달라진다.

# 샵 1개: h1 + 밑줄
## 샵 2개: h2 + 밑줄
### 샵 3개: h3
#### 샵 4개: h4
##### 샵 5개: h5
###### 샵 6개: h6
```
<br>

#### &nbsp; <span style="color:skyblue"><결과><span>
# 샵 1개: h1 + 밑줄
## 샵 2개: h2 + 밑줄
### 샵 3개: h3
#### 샵 4개: h4
##### 샵 5개: h5
###### 샵 6개: h6

<br><br>


# **2. 제목**
### 제목은 문장 밑에 ===, --- 을 쓰면 된다.
<br>

#### &nbsp; <span style="color:skyblue"><마크다운><span>
```
문장 밑에 ===, --- 를 쓰면 제목으로 표기된다.

제목 1
===

제목 2
---
```
<br>

#### &nbsp; <span style="color:skyblue"><결과><span>
제목 1
===

제목 2
---

<br><br>

# **3. 수평선**
### 수평선은 하이픈(-), 별표(*), 언더바(_)를 3번 이상 연달아 쓰면 된다.
<br>

#### &nbsp; <span style="color:skyblue"><마크다운><span>
```
--- (하이픈 3개)
*** (별표 3개)
___ (언더바 3개)
```
<br>

#### &nbsp; <span style="color:skyblue"><결과><span>
---
***
___

<br><br>

# **4. 폰트**
### 볼드체, 이탤릭체, 취소선, 밑줄을 표현할 수 있다.
### 글자 색상은 지원되지 않으며, HTML태그로 글자 색깔을 지정할 순 있다.(Git hub에선 안 먹는듯...)
<br>

#### &nbsp; <span style="color:skyblue"><마크다운><span>

```
**볼드체**

*이탤릭체*

_이탤릭체_

***볼드이탤릭***

**_볼드이탤릭_**

~~취소선~~

<u>밑줄은 뷰어 마다 지원 여부가 다르다.</u>

<p style='color:blue'>파란색 글씨 색 문장 안의 <span style='color:green'>초록색</span><p>
```
<br>

#### &nbsp; <span style="color:skyblue"><결과><span>
**볼드체**

*이탤릭체*

_이탤릭체_

***볼드이탤릭***

**_볼드이탤릭_**

~~취소선~~

<u>밑줄은 뷰어 마다 지원 여부가 다르다.</u>

<p style='color:blue'>파란색 글씨 색 문장 안의 <span style='color:green'>초록색</span><p>

<br><br>

# **5. 목록**
### : 순서가 있는 목록은 숫자를 차례로 표기하여 만든다.
### : 순서가 없는 목록은 하이픈(-), 별표(*), 더하기(+)로 만든다.
### : 탭을 먹여서 내부 삽입 목록으로 만들 수 있다.

<br>

#### &nbsp; <span style="color:skyblue"><마크다운><span>
```
1. 숫자 목록
2. 숫자 목록
    1) 괄호 숫자 록록
    2) 괄호 숫자 목록

- 하이픈 목록
* 별표 목록
+ 더하기 목록
    - 하이픈 목록
        * 별표 목록
        * 별표 목록
            1. 숫자 목록
            2. 숫자 목록
```
<br>

#### &nbsp; <span style="color:skyblue"><결과><span>
1. 숫자 목록
2. 숫자 목록
    1) 괄호 숫자 록록
    2) 괄호 숫자 목록

- 하이픈 목록
* 별표 목록
+ 더하기 목록
    - 하이픈 목록
        * 별표 목록
        * 별표 목록
            1. 숫자 목록
            2. 숫자 목록
          
<br><br>

# **6. 코드**
### 백틱(`) 1개로 앞뒤로 감싸면, 감싼 부분이 인라인 코드로 표현 된다.
### 백틱(`) 3개를 앞뒤로 감싸면, 감싼 부분이 블럭 코드로 표현 된다.
### 첫번째 백틱 3개 다음에 언어를 명시해주면 문법에 따라 강조 표시가 된다. 
> #### javascript(js), typescript(ts), python, java, go, swift, c, c#, c++, ruby 등

<br>

#### &nbsp; <span style="color:skyblue"><마크다운><span>
```
`console.log('hello world');`


```javascript
let myName = 'curryyou;

console.log(myName);
``'
```
<br>

#### &nbsp; <span style="color:skyblue"><결과><span>
`console.log('hello world');`


```javascript
let myName = 'curryyou;

console.log(myName);
```

<br><br>

# **7. 인용문**
### > 를 사용하면 인용문으로 표현된다.
### > 를 연달아 사용해 인용문의 깊이를 조정할 수 있다.

<br>

#### &nbsp; <span style="color:skyblue"><마크다운><span>
```
> 첫번째 인용문
>> 두번째 인용문
>>> 세번째 인용문
```

<br>

#### &nbsp; <span style="color:skyblue"><결과><span>
> 첫번째 인용문
>> 두번째 인용문
>>> 세번째 인용문

<br><br>

# **8. 링크**
### 형식 : ***\[표시할 글자](URL "툴팁 도움말")***
### 단순히 링크만 삽입할 경우엔, <URL>, URL 형태로 표기해도 된다.
<br>


#### &nbsp; <span style="color:skyblue"><마크다운><span>
```
[구글](https://www.google.com)

[네이버](https://www.google.com "네이버로 이동합니다")

<https://www.daum.net>

https://www.daum.net
```
<br>

#### <span style="color:skyblue"><결과><span>
 [구글](https://www.google.com)

 [네이버](https://www.google.com "네이버로 이동합니다")

 <https://www.daum.net>

 https://www.daum.net

<br><br>

# **9. 이미지**
### 형식 : ***![대체 텍스트](이미지 경로 URL "툴팁 도움말")*** 
### 이미지 크기(사이즈)를 조정하려면, HTML 태그를 사용해야 한다.
#### &nbsp;&nbsp; \<img src = "URL" width="크기" alt="대체 텍스트">

<br>

#### &nbsp; <span style="color:skyblue"><마크다운><span>
```
![대체 텍스트](https://xxx "마우스 오버시 도움말 노출")

![대체 텍스트](https://curryyou.github.io/profile.jpeg "마우스 오버시 도움말 노출")

<img src = "https://curryyou.github.io/profile.jpeg" width="100px" alt="대체 텍스트">
```

<br>

#### &nbsp; <span style="color:skyblue"><결과><span>

![대체 텍스트](https://xxx "마우스 오버시 도움말 노출")

![대체 텍스트](https://curryyou.github.io/profile.jpeg "마우스 오버시 도움말 노출")

<img src = "https://curryyou.github.io/profile.jpeg" width="100px" alt="대체 텍스트">

<br><br>

# **10. 테이블**
### 테이블은 아래의 형식으로 표현한다.
### |제목 1|제목2|제목3|
### |-----|----|----|
### |내용 1|내용2|내용3|
### 내용의 정렬은 콜론(:)을 좌, 우, 양옆에 표시하여 설정한다.
### 테이블의 내용엔 링크나 이미지도 넣을 수 있다.
### 맨 앞과 맨 뒤의 | 는 생략 가능하며, ---의 갯수도 모두 같을 필요는 없다.
<br>

#### &nbsp; <span style="color:skyblue"><마크다운><span>
```
|항목1|항목2|항목3|항목4|항목5|항목6|
|---|---|---|:---|---:|:---:|
|내용1|내용2|내용3|왼쪽|오른쪽|가운데|
|내용1|내용2|내용3|왼쪽|오른쪽|가운데|


|첫번째 항목|두번째 항목|
:---------:|:-----:
<a href='https://www.google.com' alt='구글'>구글</a> | <img width='100px' src='https://curryyou.github.io/profile.jpeg' alt='카레유 이미지'>
```
<br>

#### &nbsp; <span style="color:skyblue"><결과><span>
|항목1|항목2|항목3|항목4|항목5|항목6|
|---|---|---|:---|---:|:---:|
|내용1|내용2|내용3|왼쪽|오른쪽|가운데|
|내용1|내용2|내용3|왼쪽|오른쪽|가운데|

<br>

|첫번째 항목|두번째 항목|
:---------:|:-----:
<a href='https://www.google.com' alt='구글'>구글</a>|<img width='100px' src='https://curryyou.github.io/profile.jpeg' alt='카레유 이미지'>

<br><br><br>

# **11. HTML태그**
### HTML태그를 입력하면 대부분 작동한다.(안 되는 것도 있는듯)
#### &nbsp; <span style="color:skyblue"><마크다운><span>
```
<a href='https://www.google.com'>구글 링크</a>

<img width='200px' src='https://curryyou.github.io/profile.jpeg'>

<p style='color:blue'>초록색 글씨 색 문장<p>
```

<br>

#### &nbsp; <span style="color:skyblue"><결과><span>

<a href='https://www.google.com'>구글 링크</a>

<img width='200px' src='https://curryyou.github.io/profile.jpeg'>

<p style='color:green'>초록색 글씨 색 문장<p>



<br><br>

# **12. 띄어쓰기, 줄 바꿈**

### **1) 띄어쓰기**
&nbsp;&nbsp; : 스페이스 바 여러 번 먹여도 딱 한칸만 띄움

&nbsp;&nbsp; : \&nbsp; 를 연달아 써서, 여러 칸을 띄울 수 있음

#### &nbsp; <span style="color:skyblue"><마크다운><span>
```
여러 칸 띄워도       한 칸만 띄워진다.

\&nbsp;를 쓰면 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 여러 칸을 띄울 수 있다.
```
#### <span style="color:skyblue"><결과><span>
여러 칸 띄워도       한 칸만 띄워진다.

\&nbsp;를 쓰면 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 여러 칸을 띄울 수 있다.

<br><br>

### **2) 줄 바꿈**
&nbsp;&nbsp; : 엔터 여러 번 먹여도 한 줄만 띄움

&nbsp;&nbsp; : \<br> 태그를 여러 개 써서 여러 줄을 띄울 수 있음

#### &nbsp; <span style="color:skyblue"><마크다운><span>
```
아래 엔터 여러번 쳐도



줄 바꿈은 한 번만 된다.

<br><br><br>

<br>을 쓰면 여러줄을 바꿈이 가능하다.
```

#### <span style="color:skyblue"><결과><span>
아래 엔터 여러번 쳐도



줄 바꿈은 한 번만 된다.

<br><br><br>

\<br>을 쓰면 여러줄을 바꿈이 가능하다.


<br><br>

# 목차 링크
### `[목차](#이동할곳)`
### 링크 작성 주의 사항
    1. #으로 시작
    2. 띄어쓰기는 하이픈(-)으로 표기
    3. 특수문자는 생략
### 예시
#### 1. `첫번째 목록 1` : 띄어쓰기는 하이픈(-)으로 표기
##### - `[제목](첫번째-목록-1)`
#### 2. `첫번째+목록 1` : 특수기호 생략
##### - `[제목](첫번째목록)`
#### 3. `첫번째 + 목록 + 1` : 특수기호 생략, 띄어쓰기 두개는 하이픈(-) 2개로 표기
##### - `[제목](첫번째--목록--1)`
<br><br>

# **참고 항목**
### 마크다운 문법이 먹지 않게 하려면 앞에 역슬래시(\)를 붙여 준다.
#### &nbsp; <span style="color:skyblue"><마크다운><span>
```
\### 이스케이프
```

#### <span style="color:skyblue"><결과><span>
\### 이스케이프