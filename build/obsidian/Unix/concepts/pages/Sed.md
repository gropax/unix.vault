# Concepts

- _Input stream_
- _Input cursor_
- _Pattern space_
- _Hold space_
- _Address block_ (e.g. `/foo/ { … }`)
- _Commands_
    - _Address_ : line selector, local filter to single command
        - None (all lines)
        - Single line: `5`, `$`
        - Single regex: `/abc/`
        - Range: `10,20`, `/begin/,/end/`
        - Step: `1~2`
    - _Action_
        - _Interrupting actions_ : end a cycle
        - _Non interrupting actions_
- _Auto-print mode_ (`-n` option)
- _Cycle_ : one pass through all commands sequentially
