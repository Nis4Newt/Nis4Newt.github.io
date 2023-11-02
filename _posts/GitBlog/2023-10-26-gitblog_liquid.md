---
title: "[Gitblog][Liquid] Gitblog에서 Liquid 사용"
# layout: single
categories: gitblog
tag: 
  - gitblog
  - liquid

last_modified_at: 2023-10-26T00:00:00-00:00
---

gitblog에서 Liquid를 사용해 동적구성하는 방법

원인
---

내 블로그의 대문에서 이전에 작성한 post들을 보여주고 싶었는데   
뭔가 꼬였는지 초반에 작성한 post들만 노출되고 최신화가 안되고 있었다.

index.html을 확인해보니 초반 post만 가져오는게 아니라 초반 post의 내용이 그냥 하드코딩되어 있었다??

그래서 Liquid를 사용해서 post를 가져오고 싶었는데   
Liquid 문법을 추가해도 jekyll에서 Liquid를 읽지 못하고 그냥 string으로 노출되고 있었다.

여러가지로 찾아보니 yaml파일에 `front matter`가 있어야 되는 듯하다.

해결
---

- index.html 최상단에 front matter를 추가

__front matter(머리말)란?__   
`frpmt matter`를 포함하는 모든 `YAML`파일은 Jekyll에서 특수 파일로 처리된다.   
`front matter`는 두 `---` 로 표현되며, `---` 사이에 유효한 변수들을 설정 할 수 있다.

``` yaml
---
layout: post
title: 해당 변수들은 1개 이상일 수도 아예 없을 수도 있다.
custom: 만들 수도 있다.
---
```

최상단에 front matter를 추가함으로써 Liquid 문법 적용가능한 yaml로 인식되는 것 같다.

결말
---
  
아무것도 모르는 초반에 index.html 정리한답시고 지워버렸던것 같기도 하고.. 원래 없었던것 같기도 하고.. 그렇다.

\<부록\>    
--- 

[jekyll FrontMatter](https://jekyllrb.com/docs/front-matter/)

![img](../../assets/img/thumbnail/gitblog5.jpg){: .align-center}
<div align="center">  
  마무리 짱구
</div>