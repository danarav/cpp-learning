# Introduction

### Programs and Programming Languages

A **computer program** is a sequence of instructions that directs a computer to perform certain actions in a specified order.

When a computer is performing the actions described by the instructions in a computer program, we say it is **running** or **executing** the program.

**Software** refers to the programs on a system that are designed to be executed on hardware.

The term **platform** refers to a compatible set of hardware and software that provides the environment for software to run on.

A program that can be easily transferred from one platform to another is said to be **portable**.

A computer's CPU is only capable of processing instructions written in **machine language**. 

Here is a sample machine language instruction: ```10110000 01100001```.

Each instruction is composed of a sequence of 1s and 0s. Each individual 0 or 1 is called a **binary digit**, or **bit** for short.

An **assembly language** is a programming language that essentially functions as a more human-readable machine language.

Example machine language ```10110000 01100001``` translated to assembly language ```move al, 0x61```.

An **assembler** is a program that translates assembly language into machine language.

Each CPU family (formally known as an "instruction set architecture" or "ISA") has its own machine language and its own assembly language.

Machine languages and assembly languages are considered **low-level languages**.

**High-level languages** include C, C++, Pascal, and Java.

Much like assembly programs, programs written in a high-level language must be translated into a machine language before they can be run.
There are two primary ways this is done: compiling and interpreting.

C++ programs are usually compiled. A **compiler** is a program that reads the source code of one language and translates it into another language.
For example, a C++ compiler translates C++ source code into machine code.

The machine code output by the compiler can then be packages into an executable file.

An **interpreter** is a program that directly executes the instructions in the source code without requiring them to be compiled first.

Interpreters tend to be more flexible than compilers, but are less efficient when running programs because the interpreting process needs to be done every time the program is run.
This also means the interpreter must be installed on every machine where an interpreted program will be run.

High-level languages allow programmers to write programs without knowing much about the platform it will be run on.

A program that is designed to run on multiple platforms is said to be **cross-platform**.

Programs written in a high-level language are easier to read, write, and learn because their instructions more closely resemble the natural language and mathematics that we use every day.

