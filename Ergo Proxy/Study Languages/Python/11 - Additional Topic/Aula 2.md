# Python Keywords and Identifiers

## Python Keywords

Keywords are predefined, reserved words used in Python programming that have special meanings to the compiler.

We cannot use a keyword as a variable name, function name, or any other identifier. They are used to define the syntax and structure of the Python language.

All the keywords except `True`, `False` and `None` are in lowercase and they must be written as they are. The list of all the keywords is given below.

|   |   |   |   |   |
|---|---|---|---|---|
|||Python Keywords List|||
|`False`|`await`|`else`|`import`|`pass`|
|`None`|`break`|`except`|`in`|`raise`|
|`True`|`class`|`finally`|`is`|`return`|
|`and`|`continue`|`for`|`lambda`|`try`|
|`as`|`def`|`from`|`nonlocal`|`while`|
|`assert`|`del`|`global`|`not`|`with`|
|`async`|`elif`|`if`|`or`|`yield`|

Looking at all the keywords at once and trying to figure out what they mean might be overwhelming.

If you want to have an overview, here is the complete [list of all the keywords](https://www.programiz.com/python-programming/keyword-list) with examples.

---

## Python Identifiers

Identifiers are the name given to variables, [classes](https://www.programiz.com/python-programming/class), methods([functions](https://www.programiz.com/python-programming/function)), etc. For example,

```
language = 'Python'
```

Here, `language` is a variable (an identifier) which holds the value `'Python'`.

We cannot use keywords as variable names as they are reserved names that are built-in to Python. For example,

```
continue = 'Python'
```

The above code is wrong because we have used `continue` as a variable name.

To learn more about variables, visit [Python Variables](https://www.programiz.com/python-programming/variables-constants-literals).

---

## Rules for Naming an Identifier

- Identifiers cannot be a keyword.
- Identifiers are case-sensitive.
- It can have a sequence of letters and digits. However, it must begin with a letter or `_`. The first letter of an identifier cannot be a digit.
- It's a convention to start an identifier with a letter rather `_`.
- Whitespaces are not allowed.
- We cannot use special symbols like **!**, **@**, **#**, **$**, and so on.

---

### Some Valid and Invalid Identifiers in Python

|Valid Identifiers|Invalid Identifiers|
|---|---|
|score|@core|
|return_value|return|
|highest_score|highest score|
|name1|1name|
|convert_to_string|convert to_string|

---

## Things to Remember

Python is a case-sensitive language. This means, `Variable` and `variable` are not the same.

Always give the identifiers a name that makes sense. While `c = 10` is a valid name, writing `count = 10` would make more sense, and it would be easier to figure out what it represents when you look at your code after a long gap.

Multiple words can be separated using an underscore, like `this_is_a_long_variable`.