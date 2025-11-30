---
path: /run/current-system
parent: run
partOf: NixOS
dirType: system profile
isPathSymlink: true
topic: Profiles
description: ""
content: "test"
---
```dataviewjs
const path = dv.current().path ?? "";
const code = "# `" + path.trim() + "`";
dv.el("div", code);
```
```dataviewjs
const partOf = dv.current().partOf ?? "";
const link = "[[dir-structs/" + partOf + "|" + partOf + "]]";

dv.span("Part of: " + link);
```
```dataviewjs
const parentFile = dv.current().parent ?? "";
const parentPath = dv.page("locations/items/" + parentFile).path ?? "";
const link = "[[" + parentFile + "|" + parentPath + "]]";

dv.span("Parent: " + link);
```
```dataviewjs
const page = dv.current();
const dirType = page.dirType;

if (dirType) {
    let link = "[[dir-structs/" + dirType + "|" + dirType + "]]";
    if (page.isPathSymlink) {
        link = "symlink to " + link + " in nix path";
    }
    dv.span("Type: " + link);
}
```

`= this.content `

