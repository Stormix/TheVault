---
videos: <% tp.file.cursor(0) %>
---

# Weekly Review:

%% This template Requires the Templatr plugin and should be run on fridays, if not on friday, the value offsets should be adjusted %%

[[<%tp.date.now("gggg-[W]ww", -7)%>]] <== This Week ==> [[<%tp.date.now("gggg-[W]ww", 7)%>]]

## Notes Created This Week

```dataview
TABLE tags
FROM ""
WHERE file.ctime.year = [[<%tp.file.title%>]].file.ctime.year 
	AND file.ctime.month = [[<%tp.file.title%>]].file.ctime.month
	AND file.ctime.day >= [[<%tp.date.now("gggg-[W]ww", -8)%>]].file.ctime.day
	AND file.ctime.day <= [[<%tp.date.now("gggg-[W]ww")%>]].file.ctime.day
SORT file.name
```

[[<%tp.date.now("gggg-MM-DD", -7)%>]] ==> [[<%tp.date.now("gggg-MM-DD", -1)%>]] 

- [[<%tp.date.now("gggg-MM-DD", -7)%>]] 
	- <% tp.file.cursor(1) %>
- [[<%tp.date.now("gggg-MM-DD", -6)%>]] 
	- <% tp.file.cursor(2) %>
- [[<%tp.date.now("gggg-MM-DD", -5)%>]] 
	- <% tp.file.cursor(3) %>
- [[<%tp.date.now("gggg-MM-DD", -4)%>]] 
	- <% tp.file.cursor(4) %>
- [[<%tp.date.now("gggg-MM-DD", -3)%>]] 
	- <% tp.file.cursor(5) %>
- [[<%tp.date.now("gggg-MM-DD", -2)%>]] 
	- <% tp.file.cursor(6) %>
- [[<%tp.date.now("gggg-MM-DD", -1)%>]] 
	- <% tp.file.cursor(7) %>
