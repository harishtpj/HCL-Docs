---
description: Welcome to the HCL programming language, a High-level Computing Language
---

# The HCL Programming Language

HCL is a programming language created for **simple** usage but packed with **advanced** features. The programming language is inspired from the Lox Interpreter and its syntax from Python and Java. This programming language is intended for educational use, as mastering this language would make the learners easier to enter the arena of computer programming. Also, the programming language is made in such a way that it can be **Platform Independent.**

## How to get started?

To install and configure HCL interpreter, please refer to the project's [README](https://github.com/harishtpj/HCL).

## Introduction to the Interpreter

HCL has two modes:

1. The **REPL** mode: The infamous **R**ead **E**val **P**rint **L**oop mode. This Opens up an interactive session in which you can execute simple commands.
2. The **Execution** mode: You'll pass an `.hcl` file to the interpreter, and it will be interpreted.

For simple programs, the REPL mode is enough. But if you want to use the language for complex tasks, you need to use the interpreter.

## The REPL mode

To start the REPL, run

```bash
$ hcl
```

You'll be greeted with the following message

```
The HCL programming language REPL v1.0.0
Copyright (c) 2023, Harish Kumar

HCL .>> 
```

In the prompt, you can execute different commands of HCL

```clike
HCL .>> println "Hello, REPL";
Hello, REPL
```

To execute expressions, don't type the semicolon at the end.

```clike
HCL .>> 3 + 2;
HCL .>> 3 + 2
:= 5
```

## The Execution mode

For simple programs, the REPL is good enough. But if you want to write large programs,  the execution mode is best. Most of the time, this mode is used

Let's assume that you need to get input from the user and greet him/her with a message. To implement it, you need to follow these steps:

* Create a `greet.hcl` file and add the following content:&#x20;

```clike
# Simple program to greet user

let userName := input("Enter your name: ");
println fmt("Hello, %s! Hope you're fine.", userName);
```

* Having saved the file, run

```
$ hcl greet.hcl
```

You'll see the following result:

```
Enter your name: Harish
Hello, Harish! Hope you're fine.
```

🥳 Yay! You just ran your first HCL program.

