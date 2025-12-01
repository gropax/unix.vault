---
command: "sudo setcap cap_net_raw=ep $(which ping)"
description: "Set `cat_ne_raw` capability of the `ping` command with value 'ep'"
---
```dataviewjs
const cmd = dv.current().command ?? "";
const desc = dv.current().description ?? "";

const code = "```bash\n" + "# " + desc + "\n" + cmd + "\n```";
dv.el("div", code);
```
