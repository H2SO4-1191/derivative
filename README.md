# String Derivative Engine

A Java-based symbolic differentiation engine designed to compute algebraic derivatives and evaluate functions using purely custom string manipulation and pattern matching techniques.

## Overview

**String Derivative Engine** is a experimental Java program built to perform mathematical differentiation without using AST (Abstract Syntax Tree) parsers, external math libraries, or calculus evaluation frameworks. By relying on regex splitting, delimiters, and standard string transformations, the program parses user-input mathematical expressions containing $x$, applies standard differentiation rules (Power Rule, Product Rule, Quotient Rule, Chain Rule), and simplifies the resulting mathematical expressions on the fly.

## Features

- **Pure String-Based Parsing:** Evaluates and differentiates functions strictly through custom string operations, regex splitting, and delimiter replacement logic.
- **Calculus Rule Support:** Handles power rules ($x^n$), exponential functions ($e^{f(x)}$), natural logarithms ($\ln(f(x))$), and trigonometric functions ($\sin(x)$, $\cos(x)$).
- **Composite Operator Matching:** Supports product (`&`) and quotient (`\`) syntax to evaluate calculus operations via product and quotient rule transformations.
- **Custom Expression Sanitization:** Implements an automated organizer loop that cleans double operators (`--`, `++`, `+-`), neutral multipliers (`*[1]`), and simplified exponents ($x^1$, $x^0$).
- **Numeric Expression Evaluator:** Built-in array-tokenizing evaluator (`checker`) capable of computing numerical results for both $f(x)$ and $f'(x)$ at any given input $x$.

## Tech Stack

- **Language:** Java (JDK 8+)
- **Build Tool / Runtime:** Standard Java SE Runtime Environment
- **IDE Environment:** IntelliJ IDEA (`.idea` configuration mappings)

## Input Format & Syntax

When entering mathematical expressions, adhere to the following custom syntax rules:

| Operation                 | Custom Syntax | Example              |
| :------------------------ | :------------ | :------------------- |
| Exponents & Powers        | `^[n]`        | `x^[2]`, `(x+2)^[3]` |
| Fractional Powers / Roots | `^[1/n]`      | `x^[1/2]`            |
| Multiplication            | `&`           | `ln(x)&e^[x]`        |
| Division                  | `\`           | `2x^[3]\sin(x)`      |

## Project Structure

```bash
derivative/
├── src/                   # Source files containing the Java application
│   └── Main.java          # Core logic for string parsing, differentiation rules, and numeric evaluation
├── .gitignore             # Git ignore settings
└── README.md              # Project documentation
```

## Installation

- Clone the repository:

  ```bash
  git clone https://github.com/H2SO4-1191/Derivative.git
  ```

- Ensure you have the **Java Development Kit (JDK 8 or higher)** installed on your machine.

- Navigate to the `src` folder:

  ```bash
  cd derivative/src
  ```

- Compile the Java source file:

  ```bash
  javac Main.java
  ```

- Run the application:
  ```bash
  java Main
  ```

## Author

H2SO4-1191 – Software Engineer
