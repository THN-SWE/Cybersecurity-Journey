---
week: 2025-W41
start_date: 2025-10-07
end_date: {{date+6d:YYYY-MM-DD}}
---

# 🗓️ Week 2025-W41 Work Hours Tracker

## 📅 Week Info
- **From:** 2025-10-07 → **To:** {{date+6d:YYYY-MM-DD}}
- **Shops:** 🏪 A & 🏪 B

---

## 🧱 Daily Logs

### Tuesday, 2025-10-07

| Shop      | Start | End   | Hours                                                                                                        |
| --------- | ----- | ----- | ------------------------------------------------------------------------------------------------------------ |
| 🏪 A      | 09:00 | 13:00 | `<% tp.user.calc_hours("09:00", "13:00") %>`                                                                 |
| 🏪 B      | 14:00 | 18:30 | `<% tp.user.calc_hours("14:00", "18:30") %>`                                                                 |
| **Total** |       |       | `<% tp.user.calc_day_total([tp.user.calc_hours("09:00", "13:00"), tp.user.calc_hours("14:00", "18:30")]) %>` |

---

## 📆 Weekly Summary

```dataview
TABLE sum(rows.Hours) as "🕓 Total Weekly Hours"
FROM "Work Logs"
WHERE week = this.week