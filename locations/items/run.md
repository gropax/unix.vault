---
path: /run
parent: /
partOf: "NixOS"
description: ""
content: |
---
```dataviewjs
const path = dv.current().path ?? "";
const code = "# `" + path.trim() + "`";
dv.el("div", code);
```

Parent: `= this.parent`
Part of: `= this.partOf`
Structure: `= this.structure`

`= this.structure`

`= this.content`

