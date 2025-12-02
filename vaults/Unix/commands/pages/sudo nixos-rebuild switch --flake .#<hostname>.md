---
command: "sudo nixos-rebuild switch --flake .#<hostname>"
description: "Rebuild system explicitly from the flake-pinned nixpkgs revision."
---
```dataviewjs
const cmd = dv.current().command ?? "";
const desc = dv.current().description ?? "";
const code = "```bash\n" + "# " + desc + "\n" + cmd + "\n```\n^command";

dv.el("div", code);
```
^command

```dataviewjs
const cmd = dv.current().command ?? "";
const parts = cmd.trim().split(" ");
const program =  parts[0] === "sudo" ? parts[1] : parts[0];
const programLink = "[[cli-programs/pages/" + program + "|" + program + "]]";

dv.el("div", "Program: " + programLink);
```