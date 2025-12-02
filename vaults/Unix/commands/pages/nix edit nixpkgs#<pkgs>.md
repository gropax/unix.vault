---
command: "nix edit nixpkgs#<pkgs>"
description: "Open the Nix expression of the specified package from nixpkgs in editor."
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