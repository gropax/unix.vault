---
command: "nix-store --gc"
description: "Run the garbage collector: remove store paths not reachable from any GC root."
---
```dataviewjs
const cmd = dv.current().command ?? "";
const desc = dv.current().description ?? "";

const code = "```bash\n" + "# " + desc + "\n" + cmd + "\n```";

const parts = cmd.trim().split(" ");
const program =  parts[0] === "sudo" ? parts[1] : parts[0];
    
const programLink = "[[cli-programs/items/" + program + "|" + program + "]]";

dv.el("div", code);

dv.el("div", "Program: " + programLink);
```