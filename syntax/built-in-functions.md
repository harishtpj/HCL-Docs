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

For **input**, the `input(1)` function is used. It is of the format:

```python
input(prompt);
```

where `prompt` is a string which is prompted during input. This function returns a string of user's input.

## Datatype Conversion

The `input(1)` function always return the result as a string. To convert it into other types, the following functions are used:

1. `num(1)`: This function converts a given string to a valid number
2. `bool(1)`: This function converts a given string to a boolean value

Other than these, there is also a need to convert the `num` and `bool` datatypes to **string.** The native function `str(1)` converts the values in the above datatypes into string.

## Formatted strings

More often, you will have to interpolate a string with various values generated during programming. For such cases, the native function `fmt()` function is used. It is of the form

```java
fmt(fmtString, subs...)
```

Where: `fmtString` is a string containing string with format specifiers and `subs...` is a Variadic argument whose length depend upon the specifiers in the `fmtString`.

For example, here is a simple program to greet user(the same `greet.hcl` program:

```javascript
# Program to Input and print username

let name := input("Enter you name: ");
println fmt("Hi, %s!", name);
```

Here, the `fmt()` function replaces the `"%s"` in the string with the value stored in the variable `name`. The format string specifiers are the same as in [Java](https://www.baeldung.com/java-printstream-printf#1-format-rules).
