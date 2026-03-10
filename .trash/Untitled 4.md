 ---
week_start: 2025-10-01
Monday_Premier: 4
Monday_Vape: 5
Tuesday_Premier: 3
Tuesday_Vape: 4
Wednesday_Premier: 5
Wednesday_Vape: 3
Thursday_Premier: 4
Thursday_Vape: 4
Friday_Premier: 5
Friday_Vape: 5
Saturday_Premier: 3
Saturday_Vape: 2
Sunday_Premier: 0
Sunday_Vape: 0
---

```dataview
table 
  (this.Monday_Premier + this.Monday_Vape) as "Monday",
  (this.Tuesday_Premier + this.Tuesday_Vape) as "Tuesday",
  (this.Wednesday_Premier + this.Wednesday_Vape) as "Wednesday",
  (this.Thursday_Premier + this.Thursday_Vape) as "Thursday",
  (this.Friday_Premier + this.Friday_Vape) as "Friday",
  (this.Saturday_Premier + this.Saturday_Vape) as "Saturday",
  (this.Sunday_Premier + this.Sunday_Vape) as "Sunday",
  ((this.Monday_Premier + this.Monday_Vape) +
   (this.Tuesday_Premier + this.Tuesday_Vape) +
   (this.Wednesday_Premier + this.Wednesday_Vape) +
   (this.Thursday_Premier + this.Thursday_Vape) +
   (this.Friday_Premier + this.Friday_Vape) +
   (this.Saturday_Premier + this.Saturday_Vape) +
   (this.Sunday_Premier + this.Sunday_Vape)
  ) as "Weekly Total"`