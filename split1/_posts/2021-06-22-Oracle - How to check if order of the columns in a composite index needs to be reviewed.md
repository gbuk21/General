---
last_modified_at: 2021-06-22
layout: post
title: Oracle - How to check if order of the columns in a composite index needs to be reviewed?
---

<H4>How to check if order of the columns in a composite index needs to be reviewed?</H4>


If majority of the reads for the index shows skip scan then the column order may be an issue. dba_hist_sql_plan.options shows the type of the read.

select options, sql_text from dba_hist_sql_plan h, dba_hist_sqltext s where object_name = '&Index_name' and h.sql_id = s.sql_id;

[Next - How to check which Oracle sql execution plans used a given object]({{ site.baseurl }}{% link split1/_posts/2021-06-22-How to check which Oracle sql execution plans used a given object.md %})
