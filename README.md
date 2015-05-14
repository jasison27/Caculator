Caculator
=========
Use flex & bison to implement a simple calculator.
## Dependencies:
  - bison
  - flex

## Ubuntu Installation
  1. Install flex and bison
```
sudo apt-get install flex bison
 ```
  2-(1) Make it in the current directory
```
make
./calculator
```
  2-(2) Install it in /home/bin
```
sudo make install
caculator
```
3. Uninstall it
```
sudo make uninstall

## Using the Calculator
Example Usage:
```
1.4+2*(2+3);
sin(3.141592653/2);
ac=log(1024);
if (ac>0) then {ac=-1;} else {ac=1; ac=2*ac;}
b=sqrt(100);
while (b>0) do {b=b-1; print(b);}
def myfunc(a,b,c) {(a+b+c)/3;}
myfunc(1,2,3);
myfunc(1,2);
|-1|;
do=-1;
```
## Directory
  - calculator.l: flex file
  - calculator.y: bison file
  - funcs.c & funcs.h: AST kernel
  - Makefile: make | make clean | make install | make uninstall
