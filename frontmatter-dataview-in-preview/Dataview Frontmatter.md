```dataviewjs
let fm = Object.entries(dv.current().file.frontmatter);
let dfs = fm?.find(p => p[0] == "d-f-show")?.at(1);
let dfsv = dfs?.length>0 && !dfs?.contains(null);
if(dfsv) fm = fm?.filter(p => dfs?.includes(p[0]));
dv.table(null, fm);
dv.container.classList.add("dataview-frontmatter");
```