---
command: "getcap $(which ping)"
description: "Get all capabilities of the `ping` command"
---
```dataviewjs
const cmd = dv.current().command ?? "";
const desc = dv.current().description ?? "";

const code = "```bash\n" + "# " + desc + "\n" + cmd + "\n```";
dv.el("div", code);
```
