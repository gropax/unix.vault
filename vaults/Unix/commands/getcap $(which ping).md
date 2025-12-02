---
command: "getcap $(which ping)"
description: "Get all capabilities of the `ping` command"
topics:
- Capabilities
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