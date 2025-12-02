---
command: "nix-store --query --roots /nix/store/<hash>-<name>"
description: "Show what GC roots protect a specific store path from deletion."
legacy: true
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
const programLink = "[[cli-programs/ + program + "|" + program + "]]";

dv.el("div", "Program: " + programLink);
```