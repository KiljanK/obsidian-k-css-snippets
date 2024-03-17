```dataviewjs
let fm = Object.entries(dv.current().file.frontmatter);
let dfs = fm?.find(p => p[0] == "d-f-show")?.at(1);
let dfh = fm?.find(p => p[0] == "d-f-hide")?.at(1);
let show = dfs?.length>0 && !dfs?.contains(null);
let hide = dfh?.length>0 && !dfh?.contains(null);
if(show) fm = fm?.filter(p => dfs?.includes(p[0]));
if(hide) fm = fm?.filter(p => !dfh?.includes(p[0]));
dv.table(null, fm);
dv.container.classList.add("dataview-frontmatter");
```