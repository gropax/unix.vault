---
path: /nix/var/nix/profiles/system-<genid>-link
partOf: NixOS
dirType: system profile
topic: Profiles
description: ""
---
```dataviewjs
const path = dv.current().path ?? "";
const code = "`" + path.trim() + "`";

const parts = path.split("/").filter(Boolean);
const parents = [];
for (let i = 1; i < parts.length; i++) {
    parents.push("/" + parts.slice(0, i).join("/"));
}

const partOf = dv.current().partOf ?? "";
const partOfLink = "[[dir-structs/" + partOf + "|" + partOf + "]]";

const page = dv.current();
const dirType = page.dirType;


dv.el("div", "# " + code);

dv.el("div", "Part of: " + partOfLink);

if (dirType) {
    let link = "[[dir-structs/" + dirType + "|" + dirType + "]]";
    if (page.isPathSymlink) {
        link = "symlink to " + link + " in nix path";
    }
    dv.el("div", "Type: " + link);
}

if (parents.length > 0) {
    dv.el("div", "Parents:");
}
for (let i = 0; i < parents.length; i++) {
    const parent = parents[i];
    const parentFile = parent.slice(1).replaceAll("/", "-");
    const parentPage = dv.page(parentFile);
    const parentDesc = parentPage ? parentPage.description : "";

    let line = "[[locations/items/" + parentFile + "|" + parent + "]]";
    if (parentDesc)
        line = line + ": " + parentDesc;

    dv.el("div", line);
}
```
