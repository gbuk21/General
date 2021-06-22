---
last_modified_at: 2021-06-22
layout: post
title: How to check which Oracle sql execution plans used a given object in question?
---

<H4>How to check which Oracle sql execution plans used a given object in question?</H4>


The DBA table which shows historical plans is dba_hist_sql_plan. If object_name is known, then the query can be used to find sql_ids that used the object. This object can be an index or a table.

select * from dba_hist_sql_plan where object_name ='&Index_Name';

Following query shows sql_text along with the exeuction plans that used the object in question.

select * from dba_hist_sql_plan h, dba_hist_sqltext s where object_name = '&Index_name' and h.sql_id = s.sql_id;

[Next - Scary lightning during Tornado warning whatsapp status]({{ site.baseurl }}{% link split1/_posts/2021-04-10-Scary lightning during Tornado warning whatsapp status.md %})
