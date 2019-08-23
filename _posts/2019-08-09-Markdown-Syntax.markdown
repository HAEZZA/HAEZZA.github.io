---
layout: post
title: "Markdown Syntax"
date: 2019-08-09 11:15:00 +0900
description: 마크다운 문법 간단 정리 # Add post description (optional)
img: 2019-08-09-markdown.JPG # Add image post (optional)
tags: [Study, Markdown, Syntax]
categories: study
author: DUBUHOLIC # Add name author (optional)
---


#### <span style="color:#ff7f00">**Font Size**</span>  

	# 제목
	## 제목
	### 제목
	#### 제목
	##### 제목
	###### 제목

# 제목     
## 제목    
### 제목   
#### 제목  
##### 제목 
###### 제목

#### <span style="color:#ff7f00">**줄바꿈**</span>  
줄바꿈은 라인 끝에 space 2칸 이상  
한줄 삽입은 enter로 빈 라인을 만들면 된다. 

#### <span style="color:#ff7f00">**강조**</span>  

	**Bold**   
	*Italic*   
	***Bold and Italic***   

**Bold**   
*Italic*   
***Bold and Italic***   

#### <span style="color:#ff7f00">**인용문**</span>  

	> 인용문

> 인용문

	> 인용문  
	> 인용문  
	>> 중첩된 인용문  

> 인용문  
> 인용문  
>> 중첩된 인용문  
 
#### <span style="color:#ff7f00">**List**</span>  
```
1. 순서가 있는  
1. 리스트
```

1. 순서가 있는  
2. 리스트  

```
- 순서가 없는
	- 리스트  
	- 리스트  
- 리스트
```

- 순서가 없는
	- 리스트  
	- 리스트  
- 리스트  

#### <span style="color:#ff7f00">**Task List**</span>  

	- [x] 완료  
	- [ ] 미완료  

- [x] 완료  
- [ ] 미완료  

#### <span style="color:#ff7f00">**Code Blocks**</span>  
소스 코드를 넣고 싶으면 들여쓰기로 tab 이나 space 4칸을 하고 코드를 넣거나 \`\`\` 코드 \`\`\` 로 하면된다. 

	common.py

	import json
	def Run(FILENAME, matchkey, parent, child):
		with open (BASEDIR + FILENAME, 'r', 'utf8') as f:
		data = json.load(f)
		for key, value in data.items():
		. . .

#### <span style="color:#ff7f00">**Images**</span>  

	![caption](/assets/imag/test.jpg) 기본형  
	![caption](/assets/imag/test.jpg "dubuholic") 마우스 오버시 타이틀 나오게  
	![caption](/assets/imag/test.jpg "dubuholic"){: width="10%" height="10%"} 사이즈 조절  


![dubuholic]({{site.baseurl}}/assets/img/dubuholic.jpg "d2019-08-09ubuholic"){: width="10%" height="10%"}

#### <span style="color:#ff7f00">**가로선**</span>  

	***
	----
	_____
	3개 이상이면 됨

\***  

***

\----  

----

\_____  

_____

#### <span style="color:#ff7f00">**Tables**</span>  

	| 어제 | 오늘 |
	| :---: | :---: |
	| 그리고 |내일 |
	| 반복되는 |삶 |

| 어제 |오늘 |
| :-----: | :-----: |
| 그리고 | 내일 |
| 반복되는 | 삶 |

#### <span style="color:#ff7f00">**지우기 라인**</span>  

	~~지워보자~~ 

~~지웠다~~  

reference : *[https://www.markdownguide.org](https://www.markdownguide.org "Markdown Syntax")*

