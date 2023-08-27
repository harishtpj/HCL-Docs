---
description: Introduction to the syntax of HCL
---

# Coding in HCL

Every programming language has its own syntax and semantics, and HCL too has them. Being a Turing-Complete language, this language supports

1. General Input/Output
2. Type Conversion
3. Conditionals and Loops
4. Functions
5. Object-Oriented Programming
6. Modular Programming

and many more.... Let's see each of them in detail

## General Syntax

* Statements in HCL ends with a `;`(semicolon) character.
* Blocks in HCL are enclosed within `{` and `}` characters.
* Function are called with its name followed by `()` (parentheses) and contains arguments separated by `,` (comma)
* Other than these, HCL supports the following operators:

<table><thead><tr><th width="127">Operator</th><th>Name</th><th data-hidden></th></tr></thead><tbody><tr><td><code>+</code></td><td>Addition</td><td></td></tr><tr><td><code>-</code></td><td>Subtraction</td><td></td></tr><tr><td><code>*</code></td><td>Multiplication</td><td></td></tr><tr><td><code>/</code></td><td>Division</td><td></td></tr><tr><td><code>^</code></td><td>Exponent</td><td></td></tr><tr><td><code>=</code></td><td>Equals</td><td></td></tr><tr><td><code>!=</code></td><td>Not Equals</td><td></td></tr><tr><td><code>></code></td><td>Greater than</td><td></td></tr><tr><td><code>>=</code></td><td>Greater than or Equal to</td><td></td></tr><tr><td><code>&#x3C;</code></td><td>Less than</td><td></td></tr><tr><td><code>&#x3C;=</code></td><td>Less than or Equal to</td><td></td></tr></tbody></table>

* Strings can be concatenated using `+` operator and strings can be repeated `n` times using the `*` operator

## Comments

HCL supports single and Multi-line comments.

1. Single-line comments start with a `#` character
2. Multi-line comments starts with `#[` character and ends with `]`

There is also support for nested comments, wherein the user can nest comments in their program. Note that while nesting, there is no need in using `#` before the `[`. Instead directly use the `[]` characters.

Proper usage of comments is encouraged in HCL. Most of the code is self-explanatory. Thus, programs must not be filled up with comments. Use comments before functions and blocks of code where explanation is necessary. This makes your code neat and readable for other programmers.

## Data types in HCL

HCL has 4 simple data types:

1. `Number` data type: This data type stores integers as well as decimals. This data type can store values in the range $$-(2 - 2 ^{-52})\cdot2^{1023}$$ to $$(2 - 2 ^{-52})\cdot2^{1023}$$
2. `String` data type: This data type stores strings and supports **Unicode** encoding.
3. `Boolean` data type: This data type stores two values `true` and `false` . This data type is returned during comparison operations
4. The `Null` value: Although it is not an data type, this value is returned when a uninitiated object's value is requested.

Other than these, there are many other **Complex data types** which are available at `structures` module.

## Variables

The above datatypes are stored in a constant form called literals. These values need to be stored in computer's memory to use them. These are stored in memory as **Variables**.&#x20;

Variables must be declared using the `let` keyword in HCL to use them.

```javascript
let variable_name;
```

By default, the declared variable carried `null`. To assign a value to the declared variable, we use the `:=` (assignment) operator.

```ada
variable := 10
```

Note that the variable can be reassigned to a new value using the same operator

```javascript
let x;
x := 10;
x := "Hello";
```

As HCL is a dynamically-typed language, a variable can carry value of any type(like in Python but not as in C/Java). As the declaration and assignment is so common, this can be combined to a single line.

```javascript
let variable := 1997;
```
