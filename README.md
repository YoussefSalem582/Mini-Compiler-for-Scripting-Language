# ScriptLang Compiler 🛠️

A mini compiler for a custom scripting language, built for educational purposes.  
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)

## Overview 📜
This project implements a compiler for a scripting language with three core phases:  
1. **Lexical Analysis**: Tokenizes input code into meaningful lexemes.  
2. **Syntax Analysis**: Validates code structure and builds a parse tree.  
3. **Semantic Analysis (WIP)**: Performs type checks and scope validation.  

Developed as part of a university course, this compiler emphasizes understanding compiler design principles without relying on external libraries.

## Features ✨
- Tokenization of keywords, identifiers, numbers, and operators.  
- Parse tree generation for visual code structure representation.  
- Symbol table for tracking variables and functions.  
- Error handling for invalid syntax and undeclared variables.  
- Support for loops, conditionals, function calls, and list operations.  

## Installation 🚀
1. Clone the repository:  
   ```bash
   git clone https://github.com/yourusername/ScriptLang-Compiler.git
   ```
2. Navigate to the project directory:  
   ```bash
   cd ScriptLang-Compiler
   ```
3. Run the compiler (Jupyter Notebook or Python script):  
   ```bash
   jupyter notebook Compiler_Project.ipynb
   ```

## Usage 🖥️
### Example Input:
```python
LET a = 5
LET b = 10
IF a < b THEN
    LET c = a + b
ELSE
    LET e = a - b
ENDIF
CALL myFunc(a, b)
```

### Output:
- **Tokens**:  
  ```
  [('LET', 'LET'), ('IDENTIFIER', 'a'), ('=', '='), ('NUMBER', '5'), ...]
  ```
- **Parse Tree**:  
  ```
  Program
  ├── LET a = 5
  ├── IF a < b
  │   ├── THEN
  │   │   └── LET c = a + b
  │   └── ELSE
  │       └── LET e = a - b
  └── CALL myFunc(a, b)
  ```
- **Symbol Table**:  
  | Name | Type    | Value |
  |------|---------|-------|
  | a    | INTEGER | 5     |
  | b    | INTEGER | 10    |

## Project Structure 📂
```
ScriptLang-Compiler/
├── Compiler_Project.ipynb  # Jupyter notebook with implementation
├── docs/                   # Project documentation
├── examples/              # Sample scripts for testing
└── README.md
```

## Contributing 🤝
Contributions are welcome! Open an issue or submit a pull request for improvements.  
**Note**: This is an academic project. Adhere to your institution's collaboration guidelines.
