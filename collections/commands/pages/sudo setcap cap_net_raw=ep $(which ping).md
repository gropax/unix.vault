---
command: "sudo setcap cap_net_raw=ep $(which ping)"
description: "Set `cat_ne_raw` capability of the `ping` command with value 'ep'"
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
const programLink = "[[collections/cli-programs/items/" + program + "|" + program + "]]";

dv.el("div", "Program: " + programLink);
```