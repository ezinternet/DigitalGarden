---
{"dg-publish":true,"permalink":"/0/070-book/library/","tags":"gardenEntry"}
---

# 독서 

## 🟦 읽고 있는 책 


```dataview
TABLE without id 
	status as "상태",
	("![coverimg|50](" + cover_url+ ")") as "북커버",
	file.link as "도서명", 
	category as "카테고리", 
	dateformat(start_read_date, "DD") as "시작일", 
	dateformat(finish_read_date, "DD") as "완료일",
	my_rate as "내 평점",
	book_note as "내 서평"
FROM  #📚독서
       WHERE status = "🟦 진행중" and !contains(file.path, "Templates") 
       sort start_read_date desc 
```



## 🟧 읽을 책 

```dataview 
TABLE without id
		status as "상태", 
		("![coverimg|50](" + cover_url+ ")") as "북커버",
		file.link as "도서명",
		category as "카테고리", 
		 dateformat(start_read_date, "DD") as "시작일",
		dateformat(finish_read_date, "DD") as "완료일", 
		my_rate as "내 평점",
		book_note as "내 서평"
FROM #📚독서
          WHERE status = "🟧 예정" and !contains(file.path, "Templates")  
          SORT start_read_date desc 
``` 


## 🟨 읽다가 미룬 책 
```dataview 
TABLE without id 
	status as "상태", 
	("![coverimg|50](" + cover_url+ ")") as "북커버",
	file.link as "도서명", 
	category as "카테고리",
	
	dateformat(start_read_date, "DD") as "시작일", 
	dateformat(finish_read_date, "DD") as "완료일", 
	my_rate as "내 평점",
	book_note as "내 서평"
FROM #📚독서  
	WHERE status = "🟨 연기" and !contains(file.path, "Templates")  
	SORT start_read_date desc
``` 


## 🟩 다 읽은 책
```dataview 
TABLE without id 
	status as "상태", 
	("![coverimg|50](" + cover_url+ ")") as "북커버",
	file.link as "도서명", 
	category as "카테고리",
	
	dateformat(start_read_date, "DD") as "시작일", 
	dateformat(finish_read_date, "DD") as "완료일", 
	my_rate as "내 평점",
	book_note as "내 서평"
FROM #📚독서  
	WHERE status = "🟩 완료" and !contains(file.path, "Templates")  
	SORT start_read_date desc
``` 




------------------------
  -----------------------
--------------------  


```dataview
 Table description
 from [[#this.file.name]] and
 !outgoing([[#this.file.name]])

```

--------------------
--------------------

출처: [https://olait.tistory.com/31](https://olait.tistory.com/31) [Second Brain with Obsidian]


```
cssClasses : row-alt,table-small,col-lines,row-lines,table-numbers
```

#📚독서  #독서  #library
