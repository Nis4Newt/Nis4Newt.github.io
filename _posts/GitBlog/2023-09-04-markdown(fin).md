---
title: "[MarkDown] 마크다운 문법"
# layout: single
categories: gitblog
tag: 
  - markdown
  - md
  - gitblog

last_modified_at: 2023-09-04T00:00:00-00:00
---

<p style="color:rgb(200, 200, 200);">- 230904</p>

마크다운에 대해 작성하기 전에 마크업에 대해 알아보자.

## 마크업 언어란? (MarkUp Language)

문서가 화면에 표시되는 형식을 나타내거나, 데이터의 논리적인 구조를 명시하기 위한 규칙들을 정의한 언어의 일종   
태그 등을 사용해 **문서의 구조** 표현   
**데이터를 기술**한 언어   
X<span style="color:red;">ML</span>, HT<span style="color:red;">ML</span>, Y<span style="color:red;">ML</span> 등이 <span style="color:red;">M</span>arkup <span style="color:red;">L</span>anguage 의 일종이다. (+마크다운)


## 마크다운 (Markdown)

  - **Markdown**은 텍스트 기반의 마크업언어의 일종
  - HTML 변환 가능 (모든 HTML)
  - 간단한 문법으로 문서의 구조 표현

### \[기본적인 문법\]
  ---

  마크다운의 문법은 어차피 쉽게 찾을 수 있다. 기본적인건 필요할 때 찾아보자

### \[추가적인 내용\]
  ---

#### 1. md 안에도 html 문법을 사용할 수 있다.

md에서도 글씨를 **강조**하거나 ~~취소~~하는 정도는 가능하지만   
글씨에 색은 넣는건 불가능하다.

하지만 색을 넣고 싶은 경우
```
<p style="color:red;">html 문법을 삽입해 사용할 수 있다 <br>
<span style="color:rgb(167, 82, 199);">rgb방식도 사용 가능하다</span></p>
```
<p style="color:red;">html 문법을 삽입해 사용할 수 있다 <br>
<span style="color:rgb(167, 82, 199);">rgb방식도 사용 가능하다</span></p>

사용할 때는 그냥 md 중간에 띡 넣으면 된다.

부록의 짱구이미지 같은 경우도 html을 사용해 중앙정렬을 맞춰주고 있다
```
![git1](../../assets/img/git0.jpg){: .align-center}
<div align="center">  
  마무리 짱구
</div>
```

---
\<부록\>    

[MarkDown Git](https://gist.github.com/ihoneymon/652be052a0727ad59601)

![git1](../../assets/img/git0.jpg){: .align-center}
<div align="center">  
  마무리 짱구
</div>

