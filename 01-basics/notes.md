# C++ Basics

---

### Statements and the Structure of a program

**Statements**

A computer program is a sequence of instructions that tell the computer what to do.

A **statement** is a type of instruction that causes the program to *perform some action*.

Most statements in C++ end in a semicolon.

**Functions and the ```main``` function**

In C++, statements are typically grouped into units called functions. 
A **function** is a collection of statements that get executed sequentially (in order, from top to bottom).

**RULE:** Every C++ program must have a special function named **main** (all lower case letters).
When the program is run, the statements in ```main``` are executed in sequential order.

The name of a function (or object, type, template, etc...) is called its **identifier**.

**Characters and text**

a **character** is a written symbol or mark, such as a letter, digit, punctuation mark, or mathematical symbol.

The following are all characters: ```a```, ```2```, ```$```, ```=```.

A sequence of characters is called **text** (also called a **string**).

**Control characters** are characters that have a special meaning to the computer system, but either aren't intended to be displayed, 
or display something other than a single visible symbol. 
Examples include "escape" (which doesn't display anything), "tab" (which displays as some number of spaces), 
and "backspace" (which erases the previous character).

**Dissecting Hello World**

```c++
#include <iostream>

int main()
{
   std::cout << "Hello world!";
   return 0;
}
```
The first line is called a preprocessor directive. 
This ```#include``` preprocessor directive indicates that we would like to use the contents of the ```iostream``` library,
which is part of the C++ standard library that allows us to read and write text from/to the console.
We need this line in order to use ```std::cout```.

Blank lines are ignored by the compiler and are only used to make the program more readable to humans.

The next line tells the compiler we are defining a function named ```main```.
Again, every C++ program must have a ```main``` function or it will fail to link.
This function will produce a value whose type is ```int```.

The curly braces ``{`` and ```}``` tell the compiler which lines are part of the ```main``` function. This is called the **function body**.

Inside the function body, ```std::cout``` (which stands for "character output") and the ```<<``` operator allow us to display information on the console.
In this case we are displaying the text ```Hellow world!```.

The final line in the function body is a **return statement**.
When an executable program finishes running, the program sends a value back to the operating system in order to indicate whether it ran successfully or not.

**Syntax and Syntax Errors**

The set of rules that describe how specific words can be arranged to form valid
sentences in a language is called **syntax**.

The C++ language also has a syntax.

For example, most statements are required to end in a ```;```.

If we omit the semicolon in our Hello World program then we would get a compilation error similar to this:
```prog.cc:5:31: error: expected ';' after expression```.


---

### Comments

---

### Introduction to Objects and Variables

---

### Variable Assignment and Initialization

---

### Introduction to iostream: cout, cin, and endl

---

### Uninitialized Variables and Undefined Behavior

---

### Keywords and Naming Identifiers

---

### Whitespace and Basic Formatting

---

### Introduction to Literals and Operators

---

### Introduction to Expressions

---

### Developing your First Program

