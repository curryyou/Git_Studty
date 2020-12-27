MarkDown 정리
===
#### [깃허브 마크다운 가이드 링크](https://guides.github.com/features/mastering-markdown/ "링크 이동")

---

<br><br>

# 1. 샵(#)
### <마크 다운>
```
# 의 갯수에 따라 헤더 문장 크기가 달라진다.

# 샵 1개: 가장 큰 글씨 + 밑줄
## 샵 2개: 두번째 큰 글씨 + 밑줄
### 샵 3개 : 세번째부턴 밑줄 X
#### 샵 4개
##### 샵 5개
###### 샵 6개
```

### <결과>
# 샵 1개: 가장 큰 글씨 + 밑줄
## 샵 2개: 두번째 큰 글씨 + 밑줄
### 샵 3개 : 세번째부턴 밑줄 X
#### 샵 4개
##### 샵 5개
###### 샵 6개

<br><br>


# 2. 제목
### <마크다운>
```
문장 밑에 ===, --- 를 쓰면 제목으로 표기된다.

제목 1
===

제목 2
---
```

### <결과>
제목 1
===

제목 2
---

<br><br>

# 3. 수평선
### <마크다운>
```
아래의 표기법은 동일한 수평선을 그린다.

--- (하이픈 3개)
*** (별표 3개)
___ (언더바 3개)
```

### <결과>
---
***
___

<br><br>

# 4. 폰트
**볼드체**

*이탤릭체*

_이탤릭체_

***볼드이탤릭***

**_볼드이탤릭_**

~~취소선~~ㅡ

<u>밑줄은 안됨</u>

<br><br>

# 5. 목록
1. 순서 목록
2. 순서 목록
3. 순서 목록

- 그냥 목록
- 그냥 목록
* 그냥 목록
* 그냥 

<br><br>

# 6.  코드
`console.log('hello world');`

```js
let myName = 'curryyou;
console.log(myName);
```

<br><br>

# 7. 인용문
> 첫번째 인용문
>> 두번째 인용문
>>> 세번째 인용문

<br><br>

#8.  줄바꿈
안녕<br>나는 카레유야<br>화이팅

<br><br>

# 8. 링크
[구글](https://www.google.com)

[네이버](https://www.google.com "네이버로 이동합니다")

<https://www.daum.net>

https://www.daum.net

<br><br>

# 9.  이미지
![대체 텍스트](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fc7RuJZ%2FbtqPJMdXrM7%2F6NuTv0yW26mt6WouYzRq8K%2Fimg.png "카레유 블로그 이미지")

<br><br>

# 10. 테이블
|항목1|항목2|항목3|항목4|항목5|항목6|
|---|---|---|:---|---:|:---:|
|내용1|내용2|내용3|왼쪽|오른쪽|가운데|

|첫번째 항목|두번째 항목|
:---------:|:---------:
<a href='https://www.google.com' alt='구글'>구글</a>|<img width='200px' src='https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fc7RuJZ%2FbtqPJMdXrM7%2F6NuTv0yW26mt6WouYzRq8K%2Fimg.png' alt='카레유 블로그 이미지'>

<br><br>

# 11. HTML태그
<a href='https://www.google.com' alt='구글'>구글</a>

<img width='200px' src='https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fc7RuJZ%2FbtqPJMdXrM7%2F6NuTv0yW26mt6WouYzRq8K%2Fimg.png' alt='카레유 블로그 이미지'>

<br><br>

# 12. 칸 띄움, 줄 바꿈
\&nbsp;를 쓰면 한칸씩 띄울 수 있음

안 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;녕

<br><br>
