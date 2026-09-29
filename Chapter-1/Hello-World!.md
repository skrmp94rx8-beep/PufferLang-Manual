# Hello, world!
## How to make a hello world program?
In the last lesson, we learned that `:sys.out` is the function to print something.
So we can give a parameter to it like this:
`:sys.out("hi")`
Now change the parameter to hello world:
`:sys.out("Hello, world!")`
And then we have the output:
**Hello, world!**
## Why?
Because the lexer and parser and codegen is collaborating to translate the PufferLang code to a Python code.
- Lexer: make these :sys.out,(),"Hello, world!" into tokens
- Parser: read the tokens from the lexer and check the syntax and assemble it to a dictionary.
- CodeGen: read the AST dictionary from the parser and make it translated to Python.
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
- Python interpreter: received the code, output:
    `Hello, world!`