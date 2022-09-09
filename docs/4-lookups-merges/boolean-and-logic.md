---
sidebar_position: 2
---

# D4S2. Booleans in depth

## Boolean values

A Boolean is a value that can only be true or false.

In the computer memory, Booleans are stored as so:

- 0 - **False**
- 1 - **True**

Booleans are really cool as they power conditional statements such as if... elif... else...

Comparison expressions such as `3 > 4` evaluate to Boolean values.

```python
>>> 3==4
False
>>> 3>1
True
>>> 5<1
False
4!=3 #not equal
True
>>> 3<=3 #less or equal
True
```

## Python Comparison Operators

| Operator | Name | Example expression | Example output |
| :- | :- | -: | :-: |
| ==  | Equal  | 3 == 2 | `False` |
| !=  | Not equal | 3 == 2 | `True` |
| >  | Greater than | 3 > 2 | `True` |
| <  | Less than  | 3 < 2 | `False` |
| >=  | Greater than or equal to | 3 >= 3 | `True` |
| <=  | Less than or equal to | 3 <= 2 | `False` |

## Python type coercion

Some languages have type coercion: they convert one data type to another in certain circumstances. By and large, Python does not coerce data type.

```python
>>> True == 'True'
False
>>> 2 == '2'
False
>>> str(2) == 2
False
```

However, a data scientist needs to know that Python does coerce Booleans.

```python
>>> True == 1
True
>>> 0 == False
True
```

## Comparison Expressions

Boolean values, e.g., the results of comparison operations, can be assigned to variables.

```python
>>> x = True
>>> print(x)
True
>>> y = 8>0
>>> print(y)
True
>>> print(y==x)
True
>>> print(y!=x)
False
```

Comparisons follow the BODMAS order.

```python
((3<4)==(4>=4))!=False
```

## Conditional statements

We can use comparisons to write conditional statement such as `if... else.`

<iframe title="Embedded cell output" src="https://embed.deepnote.com/3aa75dcd-4528-457b-ab69-12debd9a9704/2e706d91-e1d8-4313-b5ca-202bf6d1cf2c/00013-7bb6c5eb-6988-4e25-b83a-6c497613fdf4?height=219" height="219" width="500"/>

<iframe title="Embedded cell output" src="https://embed.deepnote.com/3aa75dcd-4528-457b-ab69-12debd9a9704/2e706d91-e1d8-4313-b5ca-202bf6d1cf2c/00014-d63ce94b-43e8-451b-9063-08165b530a5d?height=219" height="219" width="500"/>

## Python Boolean Operators

Boolean or logical operators:

- operate on Boolean values (`True` and `False`)
- return Boolean values (`True` or `False`)

The three main logical operators in Python are:

- `and`
- `or`
- `not`

## Truth tables

The truth tables describe the results of operations using Boolean operators.

### Boolean `and` truth table

| Value 1 | Value 2 | Expression | Result |
| :- | :- | -: | :-: |
| `True`  | `True` | `True and True` | `True` |
| `True`  | `False` | `True and False` | `False` |
| `False`  | `True` | `False and True` | `False` |
| `False`  | `False` | `False and False` | `False` |

### Boolean `or` truth table

| Value 1 | Value 2 | Expression | Result |
| :- | :- | -: | :-: |
| `True`  | `True` | `True or True` | `True` |
| `True`  | `False` | `True or False` | `True` |
| `False`  | `True` | `False or True` | `True` |
| `False`  | `False` | `False or False` | `False` |

### Boolean `not` truth table

Boolean `not` is a unary operator, so it applies to only one value.

| Value | Expression | Result |
| :- | -: | :-: |
| `True`  | `not True` | `False` |
| `False` | `not False` | `True` |

## Filtering in pandas

Pandas allows to filter using Numpy masking arrays. For example, the code below will select only data for films with title "Cinderella" from a dataframe df:

```python
df[df.title == "Cinderella"]
```

However, Numpy does not support Python operators `and`, `or` and `not`.

That does make things complicated, however you can use:

- `&` for and
- `|` for or
- `~` for not

So, you can filter all retired astronauts whose flight was before 1970 this way:

```python
my_df[(my_df['Status']=='Retired') & (my_df['Year']<1970)]
```

## Deepnote

Duplicate the Deepnote below, run or re-run the cells and try the tasks (signposted 🏋️).

[<img
    src="/img/icons/deepnote-logo.svg"
    alt="Deepnote link"
/>](https://deepnote.com/project/Untitled-project-U_ESz8CFQESuCSqlf7MbYQ/%2Fpandas_filters.ipynb/#1d1cff47-b5a7-4fc3-b774-8a401e271c1f)

[Link to Deepnote](https://deepnote.com/project/Untitled-project-U_ESz8CFQESuCSqlf7MbYQ/%2Fpandas_filters.ipynb/#1d1cff47-b5a7-4fc3-b774-8a401e271c1f)
