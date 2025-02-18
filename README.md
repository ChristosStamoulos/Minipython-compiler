# Mini Python Compiler

## Description
This project is a **Mini Python Compiler** built using **SableCC** and Java. It consists of two phases: **Lexical & Syntax Analysis** and **AST & Symbol Table Processing**. The compiler uses a **custom grammar file** to parse Python-like code and perform various compilation tasks.

## Project Structure
The project is divided into two main phases:

### 1. Lexical & Syntax Analysis (Phase A)
- Uses **SableCC** to define and process a Python-like syntax.
- Implements **lexical and syntax analysis** based on `minipython.grammar`.
- Key files:
  - `minipython.grammar`: Defines the language grammar.
  - `1_Lexical.html`: Documentation for lexical analysis.
  - `2_Syntax.html`: Documentation for syntax analysis.

### 2. AST & Symbol Table Processing (Phase B)
- Constructs an **Abstract Syntax Tree (AST)**.
- Implements **symbol table management** for variables and functions.
- Key files:
  - `ASTPrinter.java`: Prints the AST structure for debugging.
  - `ASTTest1.java`: Test file for AST implementation.
  - `ParserTest1.java`: Parser testing file.
  - `tableFillVisitor.java`: Handles symbol table population.
  - `Visitor.java`: Implements tree traversal for AST analysis.
  - `SymTableClasses/` (Symbol Table Classes):
    - `SymFunction.java`: Represents function symbols.
    - `SymItem.java`: Base class for symbol items.
    - `SymVariable.java`: Represents variable symbols.
  - `Report.pdf`: Detailed report on the project.
  - `lib/sablecc.jar`: SableCC library used for grammar processing.

## Installation
### Prerequisites
- **Java Development Kit (JDK)** installed.
- **SableCC** installed and configured.

### Steps
1. Clone this repository:
   ```sh
   git clone https://github.com/your-username/mini-python-compiler.git
   cd mini-python-compiler
   ```
2. Compile the SableCC grammar:
   ```sh
   java -jar lib/sablecc.jar Project/Project 2-Phase B/minipython.grammar
   ```
3. Compile the Java files:
   ```sh
   javac -d bin Project/Project\ 2-Phase\ B/*.java Project/Project\ 2-Phase\ B/SymTableClasses/*.java
   ```
4. Run the compiler:
   ```sh
   java -cp bin MainClass input.py
   ```

## Usage
- Provide a Python-like script as input.
- The compiler will parse and analyze the syntax.
- Errors, if any, will be displayed in the console.

## Contributing
Feel free to fork this repository, create a new branch, and submit a pull request with improvements.

## License
This project is licensed under the MIT License. See `LICENSE` for details.

## Authors
[Your Name] - [Your GitHub Profile]
