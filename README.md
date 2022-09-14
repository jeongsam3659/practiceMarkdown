
마크다운 markdown
======================

> markdown 사용해보자  
> [**출처**]: (https://gist.github.com/ihoneymon/652be052a0727ad59601)

****

# 2. 마크다운 사용법 (문법)
## 2-1. 헤더Headers
* 큰제목: 문서 제목
  ```
  This is an H1
  =============
  ```
  This is an H1
  =============
  
* 작은제목 : 문서 부제목
  ```
  This is an H2
  -------------
  ```
  This is an H2
  -------------

* 글머리: 1 ~ 6까지만 
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
####### H7부턴 지원하지 않음.
   
## 2-2. BlockQuote
이메일에서 사용하는 ```>``` 블럭인용문자를 사용한다.
```
> This is a first blockqute.
>	> This is a second blockqute.
>	>	> This is a third blockqute.
```
> This is a 첫번째 블록.
> > This is a 두번째 블록.
> > > Thiis is a 세번째 블록.


종합적 결합
> ### This is a H3
> * List
> ```
> code
> ```
  
## 2-3. 목록
### - 순서있는 목록(번호)
순서있는 목록은 숫자와 점을 사용한다.
```
1. 첫번째
2. 두번째
3. 세번째
```
1. 첫번째
2. 두번째
3. 세번째

현재까지는 어떤 번호 입력해도 순서는 내림차순으로 정의된다. 
  
### - 순서있는 목록(글머리 기호: `호`, `+`, `-` 지원)
* 빨강
  * 녹색
    * 파랑

+ 빨강
  + 녹색
    + 파랑

- 빨강
  - 녹색
    - 파랑
```
* 빨강
  * 녹색
    * 파랑

+ 빨강
  + 녹색
    + 파랑

- 빨강
  - 녹색
    - 파랑
    
```
혼합해서 사용하는 것도 가능하다(내가 선호하는 방식)

```
* 1단계
  - 2단계
    + 3단계
      + 4단계
```
  
* 1단계
  - 2단계
    + 3단계
       + 4단계

## 2-4. 코드
4개의 공백 또는 하나의 탭으로 들여쓰기를 만나면 변환되기 시작하여 들여쓰지 않은 행을 만날때까지 변환이 계속된다.

### 2-4-1. 들여쓰기
```
This is a normal paragraph:

    This is a code block.
    
end code block.
```
적용예:

*****
일반적으로 작성하는 부분

   Tab을 사용하여 들여쓴 부분

끝부분을 
*****
