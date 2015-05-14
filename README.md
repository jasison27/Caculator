Caculator
=========
Use lex & bison to implement a simple calculator.
## Dependencies
  - `lex`: lexical analyzer, "scanner" or "lexer"
  - `bison`: parser generator

## Ubuntu Installation
  1. Install flex and bison
```
sudo apt-get install flex bison
 ```
  2. Make it in the current directory
```
make
./calculator
```
  3. (optional) Install it in `/home/bin`
```
sudo make install
caculator
```
  4. Uninstall it
```
sudo make uninstall
```
## Functions
  - basic arithmetic: addition, subtraction, multiplication, division, MINUS, ABS.
  - Custom variables.
  - Common mathematical functions: sqrt, exp, log, sin, cos.
  - Function for console printing: print.
  - Branch statement: if-then-else, while-do.
  - User-defined functions.
## TODO
  - Storage for last result.
  - Make user-defined functions more robust (such as add return).
  - Add error recovery.
  - Memory to user-defined functions.
  - Not limited in float number caculation (Casio fraction).

## Sample Usage
```
> 1.4 + 2*(2+3);
= 11.4
> sin(3.141592653/2);
=    1
> ac=log(1024);
= 6.931
> if (ac>0) then {ac=-1;} else {ac=1; ac=2*ac;} 
=   -1
> b=sqrt(100);
=   10
> while (b>0) do {b=b-1; print(b);}
=    9
=    8
=    7
=    6
=    5
=    4
=    3
=    2
=    1
=    0
=    0
> def myfunc(a,b,c) {(a+b+c)/3;}
Function Defined myfunc
> myfunc(1,2,3);
=    2
> myfunc(1,2);
error: too few args in call to myfunc
=    0
> |-1|;
=    1
> do=-1;
error: syntax error
> 
```
## Directory
  - `calculator.l`: flex file
  - `calculator.y`: bison file
  - `funcs.c` & `funcs.h`: AST kernel
  - `Makefile`: make | make clean | make install | make uninstall

