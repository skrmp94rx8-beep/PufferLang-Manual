# Hello, world!
## How to make a hello world program?
On last lesson, we knew that `:sys.out` is the function to print something.
So we can give parameter to it like this:
`:sys.out("hi")`
Now change the parameter to hello world:
`:sys.out("Hello, world!")`
And then we have the output:
**Hello, world!**
## Why?
Because the lexer and parser and codegen is collaborating and making the PufferLang code to a Python code.
- Lexer: make these :sys.out,(),"Hello, world!" into tokens
- Parser: read the tokens from the lexer and check the syntax and assemble it to a dictionary.
- CodeGen: read the AST dictionary from the parser and make it translated to Python.