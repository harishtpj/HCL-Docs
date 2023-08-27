---
description: General Abilities of a HCL Program
---

# Built-in Functions

This part will discuss about the various statements and native functions of HCL.

## General IO

HCL has two statements for printing to standard output:

1. The `print` statement: prints the given expression to the STDOUT without newline.
2. The `println` statement: prints the given expression to the STDOUT along with newline.

Both the statements has to be used in the following format:

```markup
print <expression>;
# or
println <expression>;
```

For input, the `input(1)` function is used. It is of the format:

```python
input(prompt);
```

where `prompt` is a string which is prompted during input. This function returns a string of user's input.
