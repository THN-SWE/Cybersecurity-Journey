# 🗓️ Work Hours — Week of <% tp.date.now("dddd, DD MMM YYYY") %>

> Enter your **week start date** below 👇 (any day — doesn’t have to be Monday!)
>
> Example → `week_start:: 2025-10-07`

week_start:: 

---

```dataviewjs
// ✅ Dynamic auto-week generator with safer date handling

const rawStart = dv.current().week_start;

// Check if user entered a valid date (YYYY-MM-DD)
const startDate = (() => {
  if (!rawStart) return null;
  const d = new Date(rawStart);
  return isNaN(d) ? null : d;
})();

if (!startDate) {
  dv.paragraph("⚠️ Please fill in `week_start:: YYYY-MM-DD` above (like 2025-10-07).");
} else {
  const days = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
  let rows = [];
  let weeklyTotal = 0;

  function toMinutes(t){
    if(!t) return null;
    const m = String(t).trim().match(/^(\d{1,2}):(\d{2})$/);
    if(!m) return null;
    return Number(m[1])*60 + Number(m[2]);
  }

  function hoursBetween(s,e){
    const sm=toMinutes(s), em=toMinutes(e);
    if(sm==null||em==null) return null;
    let diff=em-sm;
    if(diff<0) diff+=24*60;
    return +(diff/60).toFixed(2);
  }

  for(let i=0;i<7;i++){
    const d = new Date(startDate);
    d.setDate(startDate.getDate()+i);
    const iso = d.toISOString().split('T')[0];
    const label = `${days[d.getDay()]} (${iso})`;
    const keyBase = iso.replace(/-/g,'');

    const aS = dv.current()[`${keyBase}_A_start`];
    const aE = dv.current()[`${keyBase}_A_end`];
    const bS = dv.current()[`${keyBase}_B_start`];
    const bE = dv.current()[`${keyBase}_B_end`];

    const aH = hoursBetween(aS,aE);
    const bH = hoursBetween(bS,bE);
    const daily = (aH||0)+(bH||0);
    if(daily>0) weeklyTotal+=daily;

    rows.push([label,aS||'',aE||'',aH||'',bS||'',bE||'',bH||'',daily||'']);
  }

  rows.push(["**Weekly Total**","","","","","","",weeklyTotal.toFixed(2)]);
  dv.table(["Day","A start","A end","A hrs","B start","B end","B hrs","Daily total"],rows);
}