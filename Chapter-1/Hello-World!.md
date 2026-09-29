# Hello, world!
## How to make a hello world program?
In the last lesson, we learned that `:sys.out` is the function to print something.
So we can give a parameter to it like this:
`:sys.out("hi")`
Now change the parameter to hello world:
`:sys.out("Hello, world!")`
And then we have the output:
**Hello, world!**
## What does it mean?
`:`: The syscall symbol.
`sys`: The System class(actually not a class its just like this for vibe).
`out`: The method of sys called "out" that prints thing.
`()`: No need to explain.
`"Hello, world!"`: Everyone should know it.
## Why?
Because the lexer, parser, codegen collaborate to translate the PufferLang code to a Python code.
- Lexer: Translates these :sys.out,(),"Hello, world!" into tokens.
- Parser: Reads the tokens from the lexer and checks the syntax and assembles it to a dictionary.
- CodeGen: Reads the AST dictionary from the parser and translates it into Python code.
## What is the actual process?
- PufferLang source:
    `:sys.out("Hello, world!")`
- Lexer: received the source, output:
    `[('COLON', ':'), ('ID', 'sys'), ('DOT', '.'),
     ('ID', 'out'), ('LP', '('), ('STR', 'Hello, world!'), ('RP', ')')]`
- Parser: received the tokens, output:
    `{'type': 'print', 'target': {'kind': 'lit', 'value': 'Hello, world!'}}`
- CodeGen: received the AST, output:
    `print('Hello, world!')`
- PufferLang.run() method: received the code, exec(code), output:
    `Hello, world!`