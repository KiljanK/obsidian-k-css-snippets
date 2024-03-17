```dataviewjs
let result = await dv.query(`
TABLE WITHOUT ID
	fm
FROM ""
FLATTEN file.frontmatter as fm
WHERE file.name = this.file.name
`)
if(result.successful) {
	dv.table(null, result.value.values)
	dv.container.classList.add("dataview-frontmatter")
	let rli = dv.container.querySelectorAll(".dataview-result-object-li");
	rli.forEach(li => {
		let text = li.textContent;
		let span = document.createElement("span");
		span.textContent = text;
		span.classList.add("d-f-key");
		
		let child = li.lastChild;
		child.classList.add("d-f-value");
		
		if(text.contains("tags: ") && child.tagName == "UL") {
			child.querySelectorAll("li").forEach(cli => {
				cli.classList.add("multi-select-pill");
				cli.classList.add("d-f-value-tag");
			});
		}
		
		li.textContent = "";
		li.appendChild(span);
		li.appendChild(child);
	});
} else {
	dv.paragraph("Error")
}
```