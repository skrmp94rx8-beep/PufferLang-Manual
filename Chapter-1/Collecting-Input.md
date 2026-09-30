# Collecting user input
On the last lesson, we learned `:sys.out` prints thing, now, let's learn input.
---
## How to collect input from user?
Use the `:sys.in` function.
## H! O! W!?
`:sys.in(target)`[^2]
## What does it mean?
It means `target = input()`.
## Explain it properly!
`:sys` means syscall.
`.in` means method.
`()` means the space to give parameter for :sys.in.
`target` means the variable that the user input is stored in.[^1]
## What's the process?
PufferLang:    :sys.in(name)
Lexer:         [('COLON', ':'), ('ID', 'sys'), ('DOT', '.'),('ID', 'in'), ('LP', '('), ('ID', 'name'), ('RP', ')')]
Parser:        {'type': 'input', 'name': 'name'}
CodeGen:       name = input()
Python:        name = input()
User types:    puffer
Stored in:     name = "puffer"
---
## Footnotes
[^1]: Caution:the hine feature is not implemented yet, if need hint, please use NTCP.
[^2]: Caution:the `:sys.in` always return a string, but type parsing is not implemented yet, if type parsing needed, please use NTCP.