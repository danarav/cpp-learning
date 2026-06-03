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

A **comment** is a programmer-readable note that is inserted directly into the source code of a program.
Comments are ignored by the compiler.

In C++, there are two different styles of comments:

**Single-line comments**

The ```//``` symbol begins a C++ single-line comment.
This tells the compiler to ignore everything from the ```//``` to the end of the line.

```C++
std::cout << "Hello world!"; // Everything from here to the end of the line is ignored
```

Typically, the single-line comment is used to make a quick comment about a single line of code.
Single-line comments are often placed above the line it is commenting:

```c++
// std::cout lives in the iostream library
std::cout << "Hello world!\n";

// this is much easier to read
std::cout << "It is very nice to meet you!\n";

// don't you think so?
std::cout << "Yeah!\n";
```

**Multi-line comments**

The ```/*``` and ```*/``` pair of symbols denotes a C-style multi-line comment.
Everything in between the symbols is ignored.

```c++
/* This is a multi-line comment.
   This line will be ignored.
   So will this one. */
```

Often programmers will "beautify" their multi-line comments like so:

```c++
/* This is a multi-line comment.
 * the matching asterisks to the left
 * can make this easier to read
 */
```

Multi-line style comments can not be nested. For example, the following would have unexpected results:

```c++
/* This is a multi-line /* comment */ this is not inside the comment */
// The above comment ends at the first */, not the second */
```

**Warning:** Do not use multi-line comments inside other multi-line comments.
Wrapping single-line comments inside a multi-line comment is okay.

Comments should be used for three things in accord with a given library, program, or function:
1. to describe *what* it does
```c++
// This program calculates the student's final grade based on their test and homework scores.
```
```c++
// This function uses Newton's method to approximate the root of a given equation.
```
```c++
// The following lines generate a random item based on rarity, level, and a weight factor.
```

2. to describe *how* it will accomplish its goal
```c++
/* To calculate the final grade, we sum all the weighted midterm and homework scores
and then divide by the number of scores to assign a percentage, which is
used to calculate a letter grade. */
```
```c++
// To generate a random item, we're going to do the following:
// 1) Put all of the items of the desired rarity on a list
// 2) Calculate a probability for each item based on level and weight factor
// 3) Choose a random number
// 4) Figure out which item that random number corresponds to
// 5) Return the appropriate item
```

3. to describe *why* it is doing something

```c++
// The player just drank a potion of blindness and can not see anything
sight = 0;
```
```c++
// We need to multiply quantity by 2 here because they are bought in pairs
cost = quantity * 2 * storePrice;
```
```c++
// We decided to use a linked list instead of an array because
// arrays do insertion too slowly.
```

**Best practice:** Comment your code liberally, and write your comments as if speaking to someone who has no idea what the code does.
Don't assume you'll remember why you made specific choices.

Converting one or more lines of code into a comment is called **commenting out** your code.
This provides a convenient way to temporarily exclude parts of your code from being included in your compiled program.

---

### Introduction to Objects and Variables

In computing, **data** is any information that can be moved, processed, or stored by a computer.

A program can acquire data to work with many ways:
- from a file
- from a database
- over a network
- from the user providing input on a keyboard
- from the programmer putting data directly into the source code of the program itself

A single piece of data is called a **value**.

Examples include:
- Numbers
- Characters
- Text

**Random Access Memory**

The main memory in a computer is called **Random Access Memory**. When we run a program, 
the operating system loads the program into RAM. Any data that is hardcoded into the program itself is loaded at this point.

The operating system also reserves some additional RAM for the program to use while it is running.
Common uses for this memory are to store values entered by the user, to store data read in from a file or network,
or to store values calculated while the program is running so they can be used again later.

You can think of RAM as a series of numbered boxes that can be used to store data while the program is running.

**Objects and Variables**

In C++, we access memory indirectly through an object. An **object** represents a region of storage (typically RAM or a CPU register)
that can hold a value.

Rather than say "go get the value stored in mailbox number 7532", we can say,
"go get the value stored by this object" and let the compiler figure out where and how to retrieve the value.

Objects in C++ can be unnamed but more often we name our objects using an identifier.
An object with a name is called a **variable**.

A **definition** statement can be used to tell the compiler that we want to use a variable in our program.

An example of defining a variable:

```c++
// define a variable named x (of type int)
int x; 
```

At **compile time** (when the program is being compiled), when encountering this statement, 
the compiler makes a note to itself that we want a variable with the name ```x```, and that the variable
has the data type ```int```. From that point forward whenever we use the identifier ```x``` in our code,
the compiler will know that we are referring to this variable.

At **runtime** (when the program is loaded into memory and run), each object is given an actual storage location
(such as RAM, or a CPU register) that it can use to store values. The process of reserving storage for an object's
use is called **allocation**. Once allocation has occurred, the object has been created and can be used.

**Data Types**

A **data type** determines what kind of value (number, letter, text, etc...) the object will store.

In C++, the type of an object must be known at compile-time. 
That type can not be changed without recompiling the program.

**Defining Multiple Variables**

It is possible to define multiple variables of the same type in a single statement by separating
the names with a comma. The following code snippet:

```c++
int a;
int b;
```

is effectively the same as this one:

```c++
int a, b;
```

**Best Practice:** Avoid defining multiple variables of the same type in a single statement.
Instead, define each variable in a separate statement on its own line. 

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

