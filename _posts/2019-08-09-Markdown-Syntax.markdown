---
layout: post
title: "Markdown Syntax"
date: 2019-08-09 11:15:00 +0900
description: 벚나무 아래에서 느꼈던 행복했던 일주일 # Add post description (optional)
img: 2019-08-07-cherry-blossome2.JPG # Add image post (optional)
tags: [Study, Markdown, Syntax]
categories: study
author: DUBUHOLIC # Add name author (optional)
---

마크다운 문법 정리 - 가끔 찾아보는거 넘 귀찮아서 정리해봄

##### Font Size  

| Markdown | Output |
|---|:---:|---:|
| \# 제목 | # 제목 |
| \#\# 제목 | ## 제목 |
| \#\#\# 제목 | ### 제목 |
| \#\#\#\# 제목 | #### 제목 |
| \#\#\#\#\# 제목 | ##### 제목 |
| \#\#\#\#\#\# 제목 | ###### 제목 |

##### 줄바끔
줄바금은 라인 끝에 space 2칸 이상  
한줄 삽입은 enter  

##### 강조
| Markdown | Output |
|---|:---:|---:|
|\*\*text\*\* | **Bold** |  
| \*text\* | *Italic* |  
| \*\*\*text\*\*\* | ***Bold and Italic*** |

##### 인용문
\> 인용문
> 인용문

\> 인용문
\> 인용문
\>\> 중첩된 인용문
> 인용문
> 인용문
>> 중첩된 인용문
 
##### List
1. 순서가 있는  
2. 리스트  

\- Unordered List  
- 순서가 없는
	- 리스트  
	- 리스트  
- 리스트  

##### Code Blocks
소스 코드를 넣고 싶으면 tab 이나 space 4칸
	common.py
	import json

	def Run(FILENAME, matchkey, parent, child):
		with open (BASEDIR + FILENAME, 'r', 'utf8') as f:
		data = json.load(f)
		for key, value in data.items():
		. . .
혹은 \`\`\` 를 소스코드 처음과 끝에 넣어주면
```common.py
import json

def Run(FILENAME, matchkey, parent, child):
	with open (BASEDIR + FILENAME, 'r', 'utf8') as f:
	data = json.load(f)
	for key, value in data.items():
	. . .```

##### Images
\!\[caption\](/assets/imag/test.jpg) 느낌표로 시작해서 대괄호안에 캡션애용을 넣고 괄호안에 이미지 경로를 넣어주면 된다
![dubuholic](/assets/imag/dubuholic.jpg)

##### 가로선
\*\*\*, \-\-\-, \_\_\_ 셋중에 하나를 3개 이상 쓰면 가로선이 만들어진다.
---

reference : https://www.markdownguide.org


![제주 한라수목원 초입]({{site.baseurl}}/assets/img/2019-08-07-cherry-blossome.jpg)
