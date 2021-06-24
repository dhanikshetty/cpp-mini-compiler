# cpp-mini-compiler
A mini CPP compiler ehich complied the looping constructs.

 The following C++ constructs have been implemented :
  - while loops
  - nested while loops
  - simple if 
  - if else ladders.
  - for loop

## Phase1

**Generating Symbol Table**
  From the input cpp program a lexer generates tokens using the Context-Free-Grammar. The symbol table is generated with variable name, line number, scope, type and value.

## Phase2

**Generating Abstract Syntax Tree**
In this phase syntax tree is constructed from the given input program.The Abstract syntax tree is diplayed is prefix notation.


## Phase3

**Intermediate Code Generation and Optimization**
From the given input program Thrre-Adress-Code and Quadruplets is generated and displayed.Error Handling is also taken care of here.Run the `optimisation.py` file with  the quadruplets as input to optimise the code

#### Code optimization techniques used:
  - Dead Code Elimination.
  - Constant Folding.
  - common Subexpression Elimination


## To Run

Run the following commands in each of the phases.

```zsh
yacc -d --warning=none Yacc.ylex lex.lgcc y.tab.c lex.yy.c
lex lex.l
gcc -w y.tab.c lex.yy.c

```

