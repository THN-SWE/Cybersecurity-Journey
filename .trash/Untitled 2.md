---
title: "Week <% tp.date.now("WW") %> Work Log"
week: <% tp.date.now("WW") %>
year: <% tp.date.now("YYYY") %>
tags: [work, hours, week<% tp.date.now("WW") %>]
---

# 🗓️ Week <% tp.date.now("WW") %> - <% tp.date.now("MMMM YYYY") %>

## 💼 Work Hours Tracker

> Track your hours for both shops. Times are 24h format (e.g., 09:00–13:30).  
> Total hours auto-calc below 👇

### 🧮 Daily Logs

```dataview
table day, shopA_start, shopA_end, shopB_start, shopB_end, 
(round((date(shopA_end) - date(shopA_start)) * 24, 2)) + 
(round((date(shopB_end) - date(shopB_start)) * 24, 2)) as "Total Hours"
from "Work Logs"
where week = this.week and year = this.year
sort day asc