---
path: /nix/var/nix/profiles/per-user/<user>
type: directory
partOf: NixOS
topics:
- Profiles
description: Profile directory for a specific user, holding environment generations and symlinks.
---
```dataviewjs
const desc = dv.current().description ?? "";
const path = dv.current().path ?? "";
const code = "`" + path.trim() + "`";

const isRelative = path[0] === '<';
const prefix = path.split("/")[0];
const parts = path.split("/").slice(1).filter(Boolean);
const parents = [];
for (let i = 1; i < parts.length; i++) {
    parents.push(prefix + "/" + parts.slice(0, i).join("/"));
}

const partOf = dv.current().partOf ?? "";
const partOfLink = "[[collections/dir-structs/" + partOf + "|" + partOf + "]]";

const page = dv.current();
const dirType = page.dirType;


dv.el("div", "# " + code);

if (desc) {
    dv.el("div", dv.current().description ?? "");
    dv.el("br");
}

dv.el("div", "Part of: " + partOfLink);

if (dirType) {
    let link = "[[collections/dir-structs/" + dirType + "|" + dirType + "]]";
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
    const parentBase = parent[0] === '/' ? parent.slice(1) : parent;
    const parentFile = parentBase.replaceAll("/", "-");
    const parentPage = dv.page(parentFile);
    const parentDesc = parentPage ? parentPage.description : "";

    let line = "[[collections/locations/pages/" + parentFile + "|" + parent + "]]";
    if (parentDesc)
        line = line + ": " + parentDesc;

    dv.el("div", line);
}
```