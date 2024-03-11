---
title: "[git] .editorconfig"
# layout: single
categories: git
tag: 
  - .editorconfig

last_modified_at: 2023-09-28T00:00:00-00:00
---

\<개요\> 
---

일종의 formattor로 다양한 코드편집기환경에서 동일한 스타일의 코드를 유지하기 위한 파일

버전관리에 추가하면 push할때 해당 스타일로 변경해준다

간단한 예로 들여쓰기를 space 2로 지정했다면 코드 작성시 tab을 사용하더라도 space 2로 formatting 해준다

\<예시\> 
---

```
# top-most EditorConfig file
root = true

# Unix-style newlines with a newline ending every file 
[*]
charset = utf-8
end_of_line = lf
insert_final_newline = true
indent_style = space
indent_size = 4
trim_trailing_whitespace = true

[*.{yml,yaml}]
indent_size = 2
```

| 설정 | 설명 |
| --- | --- |
|**`root = true`** | 최상위 EditorConfig 파일이라는 의미, 현재 디렉토리와 그 하위 디렉토리의 모든 파일에 적용 |

| 설정 | 설명 |
| --- | --- |
| **`charset = utf-8`** | 편집기가 모든 파일에 UTF-8 인코딩을 사용하도록 설정 |
| **`end_of_line = lf`** | 모든 파일에 Unix 스타일 줄 바꿈 (\n)을 사용하도록 설정 |
| **`insert_final_newline = true`** | 모든 파일의 끝에 줄 바꿈 문자를 추가하도록 설정 |
| **`indent_style = space`** | 모든 파일에 (탭 대신)공백을 사용하여 들여쓰기하도록 설정 |
| **`indent_size = 4`** | 모든 파일에 4개의 공백을 사용하여 들여쓰기하도록 설정 |
| **`trim_trailing_whitespace = true`** | 모든 줄의 끝에서 공백을 제거하도록 설정 |

파일에는 일반 설정 외에도 YAML 파일에 대한 특정 설정이 포함되어 있음   

| 설정 | 설명 |
| --- | --- |
| **`[*.{yml,yaml}]`** | 편집기가 현재 디렉토리와 그 하위 디렉토리의 모든 YAML 파일에 다음 설정을 적용하도록 설정 |
| **`indent_size = 2`** | YAML 파일에 2개의 공백을 사용하여 들여쓰기하도록 설정 |

`EditorConfig` 파일은 {편집기 또는 IDE에 관계없이} 파일을 열 때,   
현재 디렉토리와 그 하위 디렉토리의 모든 파일이 일관된 방식으로 형식화되도록 보장한다.

\<부차적 설명\> 
---

| 설정 | 설명 |
| --- | --- |
| **charset** | 편집기의 인코딩을 지정 (주로 UTF-8 인코딩이 사용됨) |
| **end_of_line** | 편집기가 사용할 줄 바꿈 문자를 지정(Unix 스타일 줄 바꿈(\n)이 일반적인 유형) |
| **insert_final_newline** | 모든 파일의 끝에 줄 바꿈 문자를 추가해야 하는지 여부를 지정 => 모든 파일이 동일한 유형의 줄 바꿈으로 끝나도록 보장 |   
| **indent_style** | 들여쓰기에 공백을 사용해야 하는지 탭을 사용해야 하는지 여부를 지정 => 주로 공백이 사용 (일관되고 읽기 쉽기 때문) |
| **indent_size** | 들여쓰기에 사용할 공백 수를 지정 |
| **trim_trailing_whitespace** | 줄의 끝에서 공백을 제거해야 하는지 여부를 지정 |

이외에도 여러가지 있음

\<부록\> 
--- 

[EditorConfig 로 코딩 스타일 일관성 지키기](https://www.lesstif.com/software-architect/editorconfig-maintain-consistent-coding-styles-129008089.html)

![img](../../assets/img/thumbnail/git2.jpg){: .align-center}
<div align="center">  
  마무리 짱구
</div>