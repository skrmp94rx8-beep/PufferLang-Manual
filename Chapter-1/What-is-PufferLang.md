#What is PufferLang?
**PufferLang** is a *Turing-Complete* programming *language* using **Python** code as *interpreter*.
It is like Python, but like a translation of it.
Every program in PufferLang is actually a *Python* program.
The interpreter translates it into **Python**.
---
## Syntaxes and grammars
| Features | Syntax |
|---|---|
| Variable with type | `asg var<type> => val` |
| Print message | `:sys.out(msg)` |
| Get variable value usage | `?var` |
| Store input to variavle | `:sys.in(var)` |
| Create owner (OOBV) | `+O name` |
| Create field of owner (OOBV) | `+OOBV owner,field,type,value` |
| Return something | `:sys.return<<(thing)` |
| If what do something if else do something | `+C (condition) +> [ code ] !> [ elsecode ]` |
| While what do something | `+R (condition) +> [ code ]` |
| Create function | `+& name(params) [ logics ]` |
| Import PDL library | `+M libname` |
| Insert raw Python | `NTCP(pythoncode)` |
---
## Hello, world!
**PufferLang**
`:sys.out("Hello, world!")`
**Result**
Hello, world!
---
## Get variable value usage
**PufferLang**
:sys.out(?var)
:sys.out(?func())
**Result**
the value of variable var(fail if var not defined)
the returned value of function func(fail too if func not defined)
---
## Why it is PufferLang?
Because I just like pufferfish and I compounded pufferfish and lang together.
---
## File Formats
| Format | Description |
|---|---|
| .pl | Normal PufferLang |
| .pdl | PufferLang Dynamic Library |