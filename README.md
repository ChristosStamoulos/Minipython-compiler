
# Mini Python Compiler

## Description

This project is a **Mini Python Compiler** built using **SableCC** and Java. It consists of two phases: **Lexical & Syntax Analysis** and **Semantic Analysis & Symbol Table Processing**. The compiler uses a **custom grammar file** to parse Python-like code and perform various compilation tasks.

## Project Structure

The project is divided into two main phases:

### 1. Lexical & Syntax Analysis (Phase A)

- Uses **SableCC** to define and process a Python-like syntax.

- Implements **lexical and syntax analysis** based on `minipython.grammar`.

- `minipython.grammar`: Defines the language grammar.

### 2. Semantic Analysis & Symbol Table Processing (Phase B)

- Constructs an **Abstract Syntax Tree (AST)**.

- Implements **symbol table management** for variables and functions.

- Constructs **7 key semantic checks** for error detection:
 	- 1 Use of undeclared variable
 	- 2 Undeclared function call
 	- 3 Incorrect argument definition in function call
 	- 4 Using a variable of a different type (eg Integer than String) as an integer
 	- 5 Arithmetic operations in which are used as operators: None
 	- 6 Incorrect way of using a function
 	- 7 Repeating a function declaration with the same number of arguments
  
#### Key files

- `ASTPrinter.java`: Text display of the AST, with (optionally) color output.

- `ASTTest1.java`: Test file for AST implementation.

- `ParserTest1.java`: Parser testing file, central usage of visitors.

- `tableFillVisitor.java`: A visitor that traverses the AST and fills up the methods and variables tables.

- `Visitor.java`: Implements tree traversal for AST analysis in the existing data of the  filled tables.

   #### Symbol Table Classes

- `SymFunction.java`: Represents a function stored in the symbol table.

- `SymItem.java`: A symbol table entity, is the upper class of Symfuction and Symvariable classes.

- `SymVariable.java`: Represents a variable stored in the symbol table.

- `lib/sablecc.jar`: SableCC library used for grammar processing.

## Installation

### Prerequisites

- **Java Development Kit (JDK)** installed.

- **SableCC** installed and configured.

### Steps

1. Clone this repository:

   - then run:
```sh
cd (loacation of the ptoject)/Minpython-compiler\Project\Project 2-Phase B

```

2. Compile the grammar file using SableCC:

```sh

java -jar lib\sablecc.jar minipython.grammar

```

3. Compile the Java files:

```sh

Javac *.java

```

4. Run the compiler:

```sh

java ParserTest1 e.py

```

## Usage

- Provide a Python-like script as input.

- The compiler will parse and analyze the syntax.

- Errors, if any, will be displayed in the console.

## Example of usage
This python script triggers the 7nth check of the compiler because the functions created are duplicates and they have the same number of parameters

![image](https://github.com/user-attachments/assets/5ddd4538-b81a-4f54-b607-2fb11411e5b6)

The outcome:

![image](https://github.com/user-attachments/assets/e9890f32-6554-49a9-a3ee-4da6140c6dde)


## Authors

1. [Maria Schoinaki](<https://github.com/MariaSchoinaki>)

2. [Georgios Andritsos](<https://github.com/Andritsos>)

3. [Anthippi Fatsea](<https://github.com/Anthippi>)

4. [Christos Stamoulos](<https://github.com/ChristosStamoulos>)
