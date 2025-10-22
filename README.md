# Arithmetic Expression Interpreter

A simple arithmetic expression interpreter written in Python that can evaluate mathematical expressions with basic operations.

## How the Interpreter Works

## Lexical Analysis
The interpreter starts by breaking down the input string into tokens using the `Lexer` class. It recognizes:
- Integer numbers (sequences of digits)
- Arithmetic operators: `+`, `-`, `*`, `/`
- Parentheses: `(`, `)`
- Whitespace (ignored)

## Syntax Analysis
The `Parser` class builds an Abstract Syntax Tree (AST) from the tokens using recursive descent parsing. The grammar follows standard operator precedence:
- Parentheses have highest precedence
- Multiplication and division have higher precedence than addition and subtraction
- Left associativity for all operations

## AST Structure
The interpreter uses two main node types:
- `Num`: Represents integer literals
- `BinOp`: Represents binary operations with left operand, operator, and right operand

## Evaluation
The `Interpreter` class traverses the AST using the visitor pattern:
- `visit_Num`: Returns the numeric value
- `visit_BinOp`: Performs the operation based on the operator type
- Uses integer division (`//`) to maintain integer results

## Usage
Run the interpreter and enter mathematical expressions. Type "exit" to quit the program.
