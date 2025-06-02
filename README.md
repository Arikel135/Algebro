# Algebro Programming Language Specification

## 1. Introduction

Algebro is a new programming language designed with a focus on readability and a blend of mathematical and traditional programming constructs. It supports both interpreted and compiled execution.

**Development Status:** Algebro is currently under active development.

## 2. Control Flow

### 2.1 Conditional Statements

Algebro uses `if`, `elif`, and `else` for conditional execution:
```
if condition:
    #action
elif condition:
    #action
else:
    #action
```

### 2.2 Loops

#### 2.2.1 While Loop

The `while` loop executes a block of code repeatedly as long as a condition is true:
```
while condition:
    #action
```

#### 2.2.2 For Loop

The `for` loop iterates over a range of numbers:
```
for v in range(start, end):
    #action
```
### 2.3 Loop Control Statements

`break` and `continue` statements function identically to their counterparts in other common programming languages.

* `break`: Terminates the current loop and resumes execution at the statement immediately following the loop.

* `continue`: Skips the rest of the current iteration of the loop and proceeds to the next iteration.

### 2.4 Error Handling

Algebro provides `try-except` blocks for handling exceptions:
```
try:
    #code that might raise an error
except ZeroDivisionError:
    print("Cannot divide by zero")
except:
    print("An error occurred")
```

## 3. Functions

### 3.1 Mathematical Function Definition

Mathematical functions can be defined using a concise syntax:
```
f(x) = operation
```

### 3.2 General Function Definition

General-purpose functions are defined using the `func` keyword:
```
func square(y):
    #action
    x = y²
    print(y, x)
    return x
```

## 4. Operators

### 4.1 Arithmetic Operators

| Operator | Description | Example |
| :------- | :--------------- | :------------ |
| `+`      | Addition         | `a + b`       |
| `-`      | Subtraction      | `a - b`       |
| `*`      | Multiplication   | `a * b`       |
| `⋅`      | Multiplication   | `a ⋅ b`       |
| `×`      | Multiplication   | `a × b`       |
| `x y`    | Implicit Multiplication | `x y` (x times y) |
| `/`      | Division         | `a / b`       |
| `÷`      | Division         | `a ÷ b`       |
| `⅔`      | Fraction (Two-thirds) | `⅔`           |
| `^`      | Exponentiation   | `a ^ b`       |
| `²`      | Square           | `x²`          |
| `³`      | Cube             | `x³`          |
| `^½`     | Square Root      | `x^½`         |
| `²√x`    | Square Root      | `²√x`         |
| `³√y`    | Cube Root        | `³√y`         |
| `x!`     | Factorial        | `x!`          |
| `%`      | Modulo           | `a % b`       |
| `mod`    | Modulo           | `a mod b`     |

### 4.2 Comparison Operators

| Operator | Description              | Example           |
| :------- | :----------------------- | :---------------- |
| `==`     | Equal to                 | `a == b`          |
| `a == b == c` | Chained Equality (a equals b AND b equals c) | `a == b == c`     |
| `!=`     | Not equal to             | `a != b`          |
| `≠`      | Not equal to             | `a ≠ b`           |
| `>`      | Greater than             | `a > b`           |
| `<`      | Less than                | `a < b`           |
| `>=`     | Greater than or equal to | `a >= b`          |
| `≥`      | Greater than or equal to | `a ≥ b`           |
| `<=`     | Less than or equal to    | `a <= b`          |
| `≤`      | Less than or equal to    | `a ≤ b`           |

### 4.3 Logical Operators

| Operator | Symbol (Alternative) | Description | Example |
| :------- | :------------------- | :---------- | :------------ |
| `&&`     | `∧`                  | Logical AND | `A && B`      |
| `‖`     | `∨`                  | Logical OR  | `A ‖ B`      |
| `!`      | `¬`                  | Logical NOT | `!A`          |

## 5. Type System

Algebro features a flexible type system with automatic type compatibility:

* **Numeric Types:** `int`, `float`, and `double` are fully compatible with each other. Explicit type conversion is not required for operations involving these types.
* **String Types:** `char` and `string` types are also compatible. They can be concatenated directly without explicit type conversion.

## 6. Memory Management

Algebro handles memory management automatically:

* **Automatic Memory Allocation:** Memory for variables and data structures is allocated automatically by the runtime.
* **Automatic Garbage Collection:** The language includes a garbage collector that automatically reclaims memory that is no longer in use, simplifying memory management for developers.

## 7. Constants

Algebro includes built-in mathematical constants:

* `e`: Represents Euler's number (approximately 2.71828).
* `π` or `pi`: Represents Pi (approximately 3.14159).

## 8. Execution Model

Algebro is primarily an **interpreted** language, allowing for rapid development and execution. However, it also supports **compilation**, which can be utilized for performance optimization in deployment scenarios.
