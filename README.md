# Crafting Interpreters — Lox

A hands-on implementation of the **Lox programming language** while working through [*Crafting Interpreters* by Robert Nystrom](https://craftinginterpreters.com/).

This repository contains my implementations, experiments, exercises, and notes as I work through the book and build a programming language from the ground up.

The goal isn't just to follow the tutorial—it is to understand **how programming languages work internally**, from source code all the way to execution.

## What I'm Building

The project implements **jlox**, a tree-walk interpreter for Lox written in Java.

The interpreter is being built incrementally through the major stages of language implementation:

```text
Source Code
    │
    ▼
   Lexer
    │
    ▼
  Tokens
    │
    ▼
  Parser
    │
    ▼
   AST
    │
    ▼
Interpreter
    │
    ▼
  Output
```

As the project progresses, the language gains support for expressions, statements, variables, scopes, control flow, functions, classes, and other language features.

## Current Progress

* [x] Lexical analysis / Scanner
* [x] Tokens and token types
* [x] Context-free grammar fundamentals
* [x] Abstract Syntax Trees (AST)
* [x] AST generation
* [x] Visitor pattern
* [x] AST printer
* [x] Expression parsing
* [x] Expression evaluation
* [x] Statements
* [x] Variables and state
* [x] Environments
* [ ] Control flow
* [ ] Functions
* [ ] Classes
* [ ] Inheritance
* [ ] Complete tree-walk interpreter

Progress will continue as I work through the remaining chapters.

## Example

Lox code:

```lox
var x = 10;
print x + 5;
```

Output:

```text
15
```

The project also includes an AST printer used to visualize the structure of expressions.

For example:

```text
(* (- 123) (group 45.67))
```

This makes the nesting and structure of an expression explicit.

## Concepts I'm Learning

This repository explores more than just syntax. It covers fundamental programming language implementation concepts including:

* Lexical analysis
* Tokenization
* Context-free grammars
* Recursive-descent parsing
* Abstract syntax trees
* Tree traversal
* Visitor pattern
* Object-oriented design
* Expression evaluation
* Environments and variable state
* Scope
* Runtime errors
* Interpreter architecture
* Language design

## Project Structure

The structure follows the implementation developed throughout the book:

```text
.
├── com/
│   └── craftinginterpreters/
│       ├── lox/
│       │   ├── AstPrinter.java
│       │   ├── Expr.java
│       │   ├── Parser.java
│       │   ├── Scanner.java
│       │   ├── Token.java
│       │   ├── TokenType.java
│       │   └── ...
│       │
│       └── tool/
│           └── GenerateAst.java
│
└── README.md
```

The exact structure will evolve as more language features are implemented.

## Running the Interpreter

Compile the project:

```bash
javac com/craftinginterpreters/lox/*.java
```

Run the Lox interpreter:

```bash
java com.craftinginterpreters.lox.Lox
```

The REPL allows Lox expressions and statements to be entered interactively.

Example:

```text
> var x = 10;
> print x;
10
> print x + 5;
15
```

## Learning Approach

I'm treating this repository as a **working implementation and learning journal**, not simply a copy of the book's source code.

For each major part of the interpreter, the focus is on understanding:

1. **Why the component exists**
2. **What problem it solves**
3. **How it connects to the previous stage**
4. **How the implementation works**
5. **What happens when Lox code passes through it**

The objective is to eventually be able to design and implement language features independently rather than merely reproduce an existing implementation.

## Reference

This project is based on:

**Crafting Interpreters**
Robert Nystrom

https://craftinginterpreters.com/

The book is an excellent practical introduction to interpreters, parsing, language design, and programming language implementation.

## Status

🚧 **Work in Progress**

I'm building this interpreter chapter by chapter and committing the implementation as I learn.

More features coming as the journey continues.
