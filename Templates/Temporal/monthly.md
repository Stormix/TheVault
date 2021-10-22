---
read_book: 
good_reads_review: 
roth_ira: 
youtube_collab: 
ulfar_event: 
social_outing: 
---

# Monthly Review:
%% This template Requires the Templater plugin %%
[[<% tp.date.now("YYYY-[M]MM", "P-1M") %>]] <== <button class="date_button_today">This Month</button> ==> [[<% tp.date.now("YYYY-[M]MM", "P+1M") %>]]

---

## Notes Created This Month

```dataview
TABLE tags
FROM ""
WHERE file.ctime.year = [[<%tp.file.title%>]].file.ctime.year 
	AND file.ctime.month = [[<%tp.file.title%>]].file.ctime.month
SORT file.name
```

---


- [[<% tp.date.weekday("YYYY-[W]ww", 0, tp.file.title, "YYYY-[M]MM") %>]]
- [[<% tp.date.weekday("YYYY-[W]ww", 7, tp.file.title, "YYYY-[M]MM") %>]]
- [[<% tp.date.weekday("YYYY-[W]ww", 14, tp.file.title, "YYYY-[M]MM") %>]]
- [[<% tp.date.weekday("YYYY-[W]ww", 21, tp.file.title, "YYYY-[M]MM") %>]]
- [[<% tp.date.weekday("YYYY-[W]ww", 28, tp.file.title, "YYYY-[M]MM") %>]]
