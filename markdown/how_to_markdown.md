# Markdown 작성법

## 1. markdown에 관하여

## 1.1. markdown 이란?

마크다운(markdown)은 일반 텍스트 기반의 경량 마크업 언어다. 일반 텍스트로 서식이 있는 문서를 작성하는 데 사용되며, 일반 마크업 언어에 비해 문법이 쉽고 간단한 것이 특징이다. HTML과 리치 텍스트(RTF) 등 서식 문서로 쉽게 변환되기 때문에 응용 소프트웨어와 함께 배포되는 README 파일이나 온라인 게시물 등에 많이 사용된다.

### 1.2. 마크다운의 장단점

#### 장점

```markdown
1. 간결하다
2. 별도의 도구 없이 작성 가능하다
3. 용량이 적어 보관이 용이하다
4. 지원하는 프로그램과 플랫폼이 다양하다
```

#### 단점

```markdown
1. 표준이 없다
2. 표준이 없기때문에 도구에 따라서 변환방식, 생성물이 다르다
3. 모든 HTML 마크업을 대신하지 못한다
```

## 2. markdown 사용법 (문법)

### 2.1 헤더 Header

- 글머리: 1~6

```markdown
# This is a H1

## This is a H2

### This is a H3

#### This is a H4

##### This is a H5

###### This is a H6
```

---

# This is a H1

## This is a H2

### This is a H3

#### This is a H4

##### This is a H5

###### This is a H6

---

### 2.2 BlockQuote

이메일에서 사용하는 `>` 블럭인용문자를 이용한다

```markdown
> This is a first
>
> > This is a second
> >
> > > this is a third
```

---

> This is a first
>
> > This is a second
> >
> > > this is a third

---

### 2.3 목록

#### 순서가 있는 목록(Ordered list)

```markdown
1. 첫번째
2. 두번째
3. 세번째
4. 네번째
```

---

1. 첫번째
2. 두번째
3. 세번째
4. 네번째

---

#### 순서가 없는 목록(Unordered list)

(\*, +, - 지원)

```markdown
- 나이키
  - 에어맥스
    - 에어맥스 90
    - 에어맥스 95
    - 에어맥스 97
```

---

- 나이키
  - 에어맥스
    - 에어맥스 90
    - 에어맥스 95
    - 에어맥스 97

---

### 2.4 코드

#### 인라인(inline) 코드강조

```markdown
`const array = [1, 2, 3]` 배열을 한번 만들어 보아요
```

---

`const array = [1, 2, 3]` 배열을 한번 만들어 보아요

---

#### 블록(block) 코드 강조

언어별로 highlight 가능합니다

````markdown
```html
<div>html을 강조 하고 싶어요</div>
```

```css
div {
  background-color: black;
}
```

```javascript
1 < 3 ? console.log(true) : console.log(false);
```
````

---

```html
<div>html을 강조 하고 싶어요</div>
```

```css
div {
  background-color: black;
}
```

```javascript
1 < 3 ? console.log(true) : console.log(false);
```

---

### 2.5 링크

```markdown
[Google](https://www.google.com)
[Naver](https://www.naver.com)
[Github](https://www.github.com)

Google: <https://www.google.com>
Naver: <https://www.naver.com>
Github: <https://www.github.com>
```

---

[Google](https://www.google.com)  
[Naver](https://www.naver.com)  
[Github](https://www.github.com)

---

Google: <https://www.google.com>  
Naver: <https://www.naver.com>  
Github: <https://www.github.com>

---

### 2.6 강조

```markdown
_강조 합시다_
**강조 합시다**
~~강조 합시다~~
```

---

_강조 합시다_  
**강조 합시다**  
~~강조 합시다~~

---

### 2.8 줄바꿈

3칸 이상 띄어쓰기

```markdown
안녕하세요. 개행해보겠습니다

안녕하세요.  
개행해보겠습니다
```

### 2.9 이미지

```markdown
1. ![대체 텍스트(alternative text)](이미지 URL "링크 설명(title)을 작성하세요.")
2. <img> 태그를 사용하는방법(사이즈 조절가능)

![NIKE](https://user-images.githubusercontent.com/48668927/157815811-8daa8227-2f8d-40ba-8bcc-10221741dd03.jpg "nike box")

<img src="https://user-images.githubusercontent.com/48668927/157815811-8daa8227-2f8d-40ba-8bcc-10221741dd03.jpg" width="40%" height="30%" title="px(픽셀) 크기 설정" alt="NIKE"></img>
```

---

![NIKE](https://user-images.githubusercontent.com/48668927/157815811-8daa8227-2f8d-40ba-8bcc-10221741dd03.jpg "nike box")

<img src="https://user-images.githubusercontent.com/48668927/157815811-8daa8227-2f8d-40ba-8bcc-10221741dd03.jpg" width="320px" height="auto" title="px(픽셀) 크기 설정" alt="RubberDuck"></img>

---
