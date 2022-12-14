
마크다운 markdown
======================

> markdown 사용해보자  
> [**출처**](https://gist.github.com/ihoneymon/652be052a0727ad59601)
> 출저 작성자의 출처
> ## ○ 참고문서
* [78 Tools for writing and previewing Markdown](http://mashable.com/2013/06/24/markdown-tools/)
* [John gruber 마크다운 번역](http://nolboo.github.io/blog/2013/09/07/john-gruber-markdown/)
* [깃허브 취향의 마크다운 번역](http://nolboo.github.io/blog/2014/03/25/github-flavored-markdown/)
* [허니몬의 마크다운 작성법](http://www.slideshare.net/ihoneymon/ss-40575068)
* Notion.so(<https://www.notion.so/product>)
* Atom(<https://atom.io/>)
* Visual Studio Code(<https://code.visualstudio.com/>)
* Notepad++(<https://notepad-plus-plus.org/>)

****
****
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
일반적으로 작성한 구간

    한줄을 띄운 뒤 TAB을 두번 작성하기

끝부분 표시
*****

> 한줄 띄어쓰지 않으면 인식이 제대로 안되는 문제가 발생합니다.
적용예:
```
This is a normal paragraph:
    This is a code block.
end code block.
```

### 2-4-2. 코드블럭
코드블럭은 다음과 같이 2가지 방식을 사용할 수 있습니다:

* `<pre><code>{code}</code></pre>` 이용방식.

```
<pre>
<code>
public class Application1 {
  public static void main(String []args){
     System.out.println("Hi Java!");
  }
}
</code>
</pre>
```
<pre>
<code>
public class Application1 {
  public static void main(String []args){
     System.out.println("Hi Java!");
  }
}
</code>
</pre>
* 코드블럭코드("\```") 을 이용하는 방법

<pre>
<code>
```
public class Application1 {
  public static void main(String []args){
     System.out.println("Hi Java!");
  }
}
```
</code>
</pre>

```
public class Application1 {
  public static void main(String []args){
     System.out.println("Hi Java!");
  }
}
```

**깃헙**에서는 코드블럭코드("\```") 시작점에 사용하는 언어를 선언하여 [문법강조(Syntax highlighting)](https://docs.github.com/en/github/writing-on-github/creating-and-highlighting-code-blocks#syntax-highlighting)이 가능하다.

<pre>
<code>
```java
public class Application1 {
  public static void main(String []args){
     System.out.println("Hi Java!");
  }
}
```
</code>
</pre>

```java
public class Application1 {
  public static void main(String []args){
     System.out.println("Hi Java!");
  }
}

```

## 2-5. 수평선 ```<hr/>```
아래 줄은 모두 수평선을 만든다.

마크다운 문서를 미리보기로 출력할 때 페이지 나누기 용도로 많이 사용한다.
```
* * *
***
*****
- - -
---------------------------------------
```

* 적용예

* * *

***

*****

- - -

---------------------------------------

## 2-6. 링크
* 참조링크
```
// 1
[link keyword][id]

[id]: URL "Optional Title here"

// 2 code
Link: [Google][googlelink]

[googlelink]: https://google.com "Go google"
[네이버link]: https://naver.com "Go naver"
```

Link: [Google][googlelink]

Link: [Naver][네이버link]

[googlelink]: https://google.com "Go google"

[네이버link]: https://www.naver.com "네이버로 이동"


 외부링크
```
사용문법: [Title](link)
적용예: [Google](https://google.com, "google link")
```
Link: [Google](https://google.com, "google link")
Link: [유튜브](https://youtube.com, "google link")

* 자동연결
```
일반적인 URL 혹은 이메일주소인 경우 적절한 형식으로 링크를 형성한다.

* 외부링크: <http://example.com/>
* 이메일링크: <address@example.com>
```

* 외부링크: <http://example.com/>
* 이메일링크: <address@example.com>


## 2-7. 강조
```
*single asterisks*
_single underscores_
**double asterisks**
__double underscores__
~~취소선~~
```

* *single asterisks*
* _single underscores_
* **double asterisks**
* __double underscores__
* ~~cancelline~~

> ```문장 중간에 사용할 경우에는 **띄어쓰기** 를 사용하는 것이 좋다.```   
> 문장 중간에 사용할 경우에는 띄어쓰기를 사용하는 것이 좋다.

## 2-8. 이미지


## 2-9. 줄바꿈
3칸 이상 띄어쓰기(` `)를 하면 줄이 바뀐다.

```
* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸이상을 띄어쓰기해야 한다. 
이렇게

* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸이상을 띄어쓰기해야 한다.___\\ 띄어쓰기
이렇게
```

* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸이상을 띄어쓰기해야 한다. 이렇게

* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸이상을 띄어쓰기해야 한다.    \
이렇게
