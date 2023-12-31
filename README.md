# Project Name: HW4
## Authors: Rahul Mohan and Nikul Halai

This project implements a compiler for a simple programming language. The compiler consists of a lexer, parser, and code generator. It processes source code written in the specified language and generates assembly-like code.

### Error Codes:
- **LEX_COMMENT_NEVER_ENDED**: Comment block never ended.
- **LEX_IDENTIFIER_INVALID_START**: Identifier cannot start with a number.
- **LEX_IDENTIFIER_TOO_LONG**: Identifiers can have a maximum of 11 characters.
- **LEX_NUMBER_TOO_LONG**: Numbers can have a maximum of 5 digits.
- **LEX_INVALID_SYMBOL**: Invalid symbol.
- **PCG_PERIOD_EXPECTED**: '.' missing at the end of the program.
- **PCG_EQUAL_EXPECTED_NOT_BECOME**: Use '=' instead of ':='.
- **PCG_IDENTIFIER_EXPECTED**: Expected an identifier.
- **PCG_SYMBOL_IN_USE**: Symbol name has already been declared.
- **PCG_EQUAL_EXPECTED**: Constant identifier must be followed by '='.
- **PCG_VALUE_EXPECTED**: '=' must be followed by a number.
- **PCG_SEMICOLON_COMMA_EXPECTED**: Expected ',' or ';'.
- **PCG_SEMICOLON_EXPECTED**: Expected ';'.
- **PCG_VAR_EXPECTED**: Expected an identifier of type var.
- **PCG_BECOME_EXPECTED**: Var identifiers must be followed by ':='.
- **PCG_RIGHT_PARENTHESIS_EXPECTED**: Right parenthesis missing.
- **PCG_PROCEDURE_EXPECTED**: Only procedure identifiers can be called.
- **PCG_MAX_LEVEL**: Max nested blocks exceeded.
- **PCG_END_EXPECTED**: 'end' expected.
- **PCG_THEN_EXPECTED**: 'then' expected.
- **PCG_DO_EXPECTED**: 'do' expected.
- **PCG_UNDECLARED_SYMBOL**: Identifier never declared.
- **PCG_COMPARISON_OPERATOR_EXPECTED**: Relational operator expected.
- **PCG_INVALID_EXPRESSION**: Arithmetic equations must contain only operands, parentheses, numbers, or symbols.
- **PCG_PROCEDURE_IN_EXPRESSION**: Expression must not contain a procedure identifier.

### Lexer (Tokenization):
The lexer processes the input source code and tokenizes it, identifying different elements such as keywords, identifiers, numbers, and symbols.

### Parser (Syntax Analysis):
The parser analyzes the syntax of the source code to ensure it follows the rules of the specified language. It generates intermediate code and reports any syntax errors.

### Code Generator:
The code generator processes the intermediate code generated by the parser and produces executable code. It handles constants, variables, procedures, and various statements.

### How to Use:
1. **Load Program:**
   - Use the `load_program` function to load the source code from a file.

2. **Tokenization (Lexer):**
   - The `generate_tokens` function tokenizes the source code, populating the `lexeme` array.

3. **Syntax Analysis (Parser):**
   - The `program` function initiates the parsing process, ensuring the correct syntax of the source code.

4. **Code Generation:**
   - The code generation process produces executable code based on the parsed syntax.

5. **Error Handling:**
   - The project includes comprehensive error handling for various scenarios, providing informative error messages.
