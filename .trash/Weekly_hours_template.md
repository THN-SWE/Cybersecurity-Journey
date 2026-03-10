# Week: {{date:YYYY-MM-DD}} → {{date+6d:YYYY-MM-DD}}

> Fill times as **HH:MM** (24-hour) — e.g. `09:00` or `14:30`.
> Leave blank if you didn't work that shift.

Monday_A_start:: 2 : 0
Monday_A_end:: 3 : 30
Monday_B_start:: 3
Monday_B_end:: 5

Tuesday_A_start:: 
Tuesday_A_end:: 
Tuesday_B_start:: 
Tuesday_B_end:: 

Wednesday_A_start:: 
Wednesday_A_end:: 
Wednesday_B_start:: 
Wednesday_B_end:: 

Thursday_A_start:: 
Thursday_A_end:: 
Thursday_B_start:: 
Thursday_B_end:: 

Friday_A_start:: 
Friday_A_end:: 
Friday_B_start:: 
Friday_B_end:: 

Saturday_A_start:: 
Saturday_A_end:: 
Saturday_B_start:: 
Saturday_B_end:: 

Sunday_A_start:: 
Sunday_A_end:: 
Sunday_B_start:: 
Sunday_B_end:: 

```dataviewjs
// ---- dataviewjs: computes hours per shop, per day, and weekly total ----
const days = ['Monday','Tuesday','Wednesday','Thursday','Friday','Saturday','Sunday'];

function toMinutes(t){
  if(!t) return null;
  const m = String(t).trim().match(/^(\d{1,2}):(\d{2})$/);
  if(!m) return null;
  const h = Number(m[1]), mm = Number(m[2]);
  if(h < 0 || h > 23 || mm < 0 || mm > 59) return null;
  return h * 60 + mm;
}

function hoursBetween(s, e){
  const sm = toMinutes(s), em = toMinutes(e);
  if(sm === null || em === null) return null;
  let diff = em - sm;
  if(diff < 0) diff += 24 * 60; // handles overnight shifts (end next day)
  return +(diff / 60).toFixed(2);
}

let rows = [];
let weeklyTotal = 0;

for (const day of days){
  const aS = dv.current()[`${day}_A_start`];
  const aE = dv.current()[`${day}_A_end`];
  const bS = dv.current()[`${day}_B_start`];
  const bE = dv.current()[`${day}_B_end`];

  const aH = hoursBetween(aS, aE);
  const bH = hoursBetween(bS, bE);
  const daily = ( (aH || 0) + (bH || 0) );

  if (!Number.isNaN(daily) && daily > 0) weeklyTotal += daily;

  rows.push([
    day,
    aS || '',
    aE || '',
    aH === null ? '' : aH.toFixed(2),
    bS || '',
    bE || '',
    bH === null ? '' : bH.toFixed(2),
    daily ? daily.toFixed(2) : ''
  ]);
}

rows.push(['**Weekly Total**','','','','','','', weeklyTotal.toFixed(2)]);

// header: Day | A start | A end | A hrs | B start | B end | B hrs | Daily total
dv.table(['Day','A start','A end','A hrs','B start','B end','B hrs','Daily total'], rows);