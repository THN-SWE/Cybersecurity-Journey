---
week: {{date:YYYY-[W]ww}}
start_date: {{date:YYYY-MM-DD}}
end_date: {{date+6d:YYYY-MM-DD}}
---

# 🗓️ Week {{date:YYYY-[W]ww}} Work Hours Tracker

## 📅 Week Info
- **From:** {{date:YYYY-MM-DD}} → **To:** {{date+6d:YYYY-MM-DD}}
- **Shops:** 🏪 A & 🏪 B

---

## 🧱 Daily Logs

### {{date:dddd, YYYY-MM-DD}}

| Shop | Start | End | Hours |
|------|--------|-----|-------|
| 🏪 A | 09:00 | 13:00 | `<% tp.user.calc_hours("09:00", "13:00") %>` |
| 🏪 B | 14:00 | 18:30 | `<% tp.user.calc_hours("14:00", "18:30") %>` |
| **Total** |  |  | `<% tp.user.calc_day_total([tp.user.calc_hours("09:00", "13:00"), tp.user.calc_hours("14:00", "18:30")]) %>` |

---

## 📆 Weekly Summary

```dataview
TABLE sum(rows.Hours) as "🕓 Total Weekly Hours"
FROM "Work Logs"
WHERE week = this.week