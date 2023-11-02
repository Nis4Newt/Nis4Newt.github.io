---
title: "[Gitblog] Gitblog 구성"
# layout: single
categories: gitblog
tag: 
  - gitblog
  - gitblog 구조
  - gitblog 구성

last_modified_at: 2023-09-21T00:00:00-00:00
---

<p style="color:rgb(200, 200, 200);">해당 문서는 gitblog를 지속적으로 커스텀해 나가면서 업데이트할 예정입니다.</p>

### 폴더
- .git
  - 프로젝트에서 Git 저장소를 초기화할 때 자동으로 생성되는 숨겨진 Directory.
  - Git이 프로젝트의 변경 사항을 추적하고 버전을 관리하기 위해 사용하는 모든 필요한 파일과 메타데이터가 포함되어 있다.
- .github
  - .github 폴더는 git의 작동에 직접적인 영향은 없음, .github의 파일들은 git에서 무시.
  - .github 폴더는 프로젝트의 설명과 구성을 위한 용도로 폴더내의 파일들은 프로젝트의 문서, 기여가이드, 라이선스 정보, work flow등을 포함하고, 이 파일들은 프로젝트의 기능과 사용성을 향상시킨다.
- .jekyll-cache
  - Jekyll 사이트의 빌드 결과물을 캐싱하는데 사용.
  - Jekyll은 정적 사이트 생성기이기 때문에, 사이트를 빌드할때마다 모든 HTML, CSS, JavaScript 파일을 생성한다.
  - .jekyll-cache 디렉토리를 사용하려면 Jekyll의 config.yml 파일에 다음과 같은 설정을 추가합니다.
  - ```
  cache: true
  ```
  - 설정을 추가하면 빌드할때 .jekyll-cache를 확인하여 이전에 생성된 파일이 있는지 확인, 파일이 있는경우 해당 파일을 재사용하여 빌드 시간을 단축한다.

- _data
- _includes
- _layouts
- _pages
- _posts
- _sass
- _site
- assets

### 파일
- .editorconfig
  - 일종의 formattor로 버전관리에 들어가는 코드스타일을 다양한 코드 편집기에 동일하게 적용시키기 위해 사용
  - editorconfig에
- .gitattributes
- .gitignore
- .travis.yml
- _config.yml
- banner.js
- feed.xml
- Gemfile
- Gemfile.lock
- google89ec9b06539ac70c.html
- index.html
- LICENSE
- minimal-mistakes-jekyll.gemspec
- package.json
- package-lock.json
- Rakefile
- README.md
- robots.txt
- sitemap.xml
- staticman.yml

뭐가 엄청 지저분하게 많다.
하나씩 정리해보자 (계획)

--- 

\<부록\> 
[EditorConfig 로 코딩 스타일 일관성 지키기](https://www.lesstif.com/software-architect/editorconfig-maintain-consistent-coding-styles-129008089.html)


![img](../../assets/img/thumbnail/unity0.png){: .align-center}
<div align="center">  
  마무리 짱구
</div>