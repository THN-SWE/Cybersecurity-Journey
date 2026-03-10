---
title: "Week {{date:WW}} Work Log"
date: {{date:YYYY-MM-DD}}
tags: [#work, #hours, #week{{date:WW}}]
---

# 🗓️ Week {{date:WW}} - {{date:MMMM YYYY}}

## 📅 Work Hours Log

```dataview
table day, shopA_start, shopA_end, shopB_start, shopB_end, round(((date(shopA_end) - date(shopA_start)) + (date(shopB_end) - date(shopB_start))) * 24, 2) as "Total Hours"
from "Work Hours"
where week = {{date:WW}}