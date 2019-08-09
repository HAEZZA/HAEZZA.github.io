---
layout: post
title: "Markdown Syntax"
date: 2019-08-09 11:15:00 +0900
description: 벚나무 아래에서 느꼈던 행복했던 일주일 # Add post description (optional)
img: 2019-08-09-markdown.JPG # Add image post (optional)
tags: [Study, Markdown, Syntax]
categories: study
author: DUBUHOLIC # Add name author (optional)
---

마크다운 문법 정리 - 가끔 찾아보는거 넘 귀찮아서 정리해봄

### Font Size  

| Markdown | Output |
|:---:|:---:|
|\# 제목| # 제목  |
|\#\# 제목|  ## 제목  |
|\#\#\# 제목|  ### 제목 |  
|\#\#\#\# 제목|  #### 제목 |  
|\#\#\#\#\# 제목|  ##### 제목 |  
|\#\#\#\#\#\# 제목|  ###### 제목 |  

### 줄바꿈
줄바꿈은 라인 끝에 space 2칸 이상  
한줄 삽입은 enter  

### 강조
| Markdown | Output |
|:---:|:---:|
|\*\*text\*\* | **Bold** |  
| \*text\* | *Italic* |  
| \*\*\*text\*\*\* | ***Bold and Italic*** |

### 인용문
\> 인용문
> 인용문

\> 인용문  
\> 인용문  
\>\> 중첩된 인용문  
> 인용문  
> 인용문  
>> 중첩된 인용문  
 
### List
1. 순서가 있는  
2. 리스트  

\- Unordered List  
- 순서가 없는
	- 리스트  
	- 리스트  
- 리스트  

### Task List
\-\[x] 완료  
\-\[] 미완료  

-[x] 완료  
-[] 미완료  

### Code Blocks
소스 코드를 넣고 싶으면 tab 이나 space 4칸  

	common.py
	import json
	def Run(FILENAME, matchkey, parent, child):
		with open (BASEDIR + FILENAME, 'r', 'utf8') as f:
		data = json.load(f)
		for key, value in data.items():
		. . .

\`\`\` 코드 \`\`\`을 이용한 방법

```
common.py
import json
def Run(FILENAME, matchkey, parent, child):
	with open (BASEDIR + FILENAME, 'r', 'utf8') as f:
	data = json.load(f)
	for key, value in data.items():
	. . .
```

### Images
\!\[caption\](/assets/imag/test.jpg) 느낌표로 시작해서 대괄호안에 캡션애용을 넣고 괄호안에 이미지 경로를 넣어주면 된다.  
![dubuholic]({{site.baseurl}}/assets/img/dubuholic.jpg "Dubuholic")

### 가로선
\*\*\*, \-\-\-, \_\_\_ 셋중에 하나를 3개 이상 쓰면 가로선이 만들어진다.  
------  

### Tables
	\|어제\|오늘\|
	\|---\|---\|
	\|그리고\|내일\|
	\|반복되는\|삶\|

|어제|오늘|
|---|---|
|그리고|내일|
|반복되는|삶|

### 지우기 라인
\~\~지우기\~\~ ~~지우기~~  

이정도면 굳굳~

reference : *[https://www.markdownguide.org](https://www.markdownguide.org "Markdown Syntax")*

