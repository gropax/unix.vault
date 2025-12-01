---
command: "which ping"
description: "Print the location of the `ping` executable."
---
```dataviewjs
const cmd = dv.current().command ?? "";
const desc = dv.current().description ?? "";

const code = "```bash\n" + "# " + desc + "\n" + cmd + "\n```";
dv.el("div", code);
```
