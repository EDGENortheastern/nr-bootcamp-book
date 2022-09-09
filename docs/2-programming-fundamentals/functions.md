---
sidebar_position: 3
---

# D2S3. Python functions

[Slides](https://hackmd.io/@D3o17PKxQImUPBfYYD6wYg/r178ibSCY#/)

## Anatomy of a function

Functions allow creating reusable code and avoiding code repetition, copying and pasting.

A function in Python is defined with the `def` keyword, followed by the function name, zero or more **arguments** in parenthesis `(),` and a colon `:` to indicate the start of the function's body.

The body of the function is **indented**.

Then, an *optional* `return` statement follows.

The recipe for a function definition in Python:

- `def`: the `def` keyword, telling Python we're about to start a function definition
- a name for the function
- `(`: opening parenthesis
- (optional) the **names** of one or more arguments, separated with `,`
- (optional) the **names** and **values** of one or more default arguments, separated with (`,`) *note: we'll see these in the next section*
- `)` closing parenthesis
- `:` a colon

### Examples of function definitions

```python
# A basic function that accepts no arguments and returns nothing.
def hello_world():
    print("Hello, World!")


# A function that accepts two arguments, and returns a value
def add_numbers(x, y):
    return x + y
```

If you do not follow the recipe above function wrong, Python throws a `SyntaxError.`

For example, trying to create a function without the colon `:`:

```python
>>> def hello_world()
  File "<stdin>", line 1
    def hello_world()
                    ^
SyntaxError: invalid syntax
```

Python produces meaningful error messages; read them carefully when debugging.

### Indentation

Python knows what code is related to a function by its indentation. In Python, whitespace is a part of the syntax.

If you get an `IndentationError,` that means that you didn't correctly indent your code after your function definition. To fix an indentation error, use backspace to get to the colon and start a new line. Most Python IDEs will automatically indent correctly.

```python
# The error you'll see if you didn't indent your function correctly.
>>> def add_numbers(x, y):
... return x + y
File "<stdin>", line 2
    return x + y
        ^
IndentationError: expected an indented block
```

## Calling a function

Once you have defined a function, you must call it by its name from the main program.

⚠️ Code inside a function is not executed until the function is called.

---

### Without arguments

<iframe src="https://trinket.io/embed/python/f6da745d10" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

### With arguments

```python
>>> def add_numbers(x, y):
...     return x + y
...
>>> add_numbers(3, 5)
8
>>>
```

<iframe src="https://trinket.io/embed/python/be11570685" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

## Coding with functions

https://replit.com/@missPunter/function-start#main.py