# Java Variables
A variable is a container which holds the value while the Java program is executed. A variable is assigned with a data type.

Variable is a name of memory location. There are three types of variables in java: **local, instance** and **static**.

## Types of Variables
There are three types of variables in Java:

### Local variable
A variable declared inside the body of the method is called local variable. You can use this variable only within that method and the other methods in the class aren't even aware that the variable exists.

A local variable cannot be defined with "static" keyword.

### Instance variable
A variable declared inside the class but outside the body of the method, is called an instance variable. It is not declared as static.

It is called an instance variable because its value is instance-specific and is not shared among instances.

### Static variable
A variable that is declared as static is called a static variable. It cannot be local. You can create a single copy of the static variable and share it among all the instances of the class. Memory allocation for static variables happens only once when the class is loaded in the memory.

# Data Types in Java

Data types specify the different sizes and values that can be stored in the variable. There are two types of data types in Java:

## 1. Primitive data types
 The primitive data types include **boolean, char, byte, short, int, long, float** and **double**.

| Data Type |	Default Value |	Default size | Range(inclusive) | 
| --------- | ------------- | ------------ | ----- |
| boolean |	false |	1 bit |  |
| char |	'\u0000' |	2 byte | '\u0000' (or 0) to '\uffff' (or 65,535) |
| byte |	0 |	1 byte | -128 to 127 |
| short |	0 |	2 byte | -32,768 to 32,767 |
| int |	0 |	4 byte | 2,147,483,648 (-2^31) to 2,147,483,647 (2^31 - 1) |
| long |	0L |	8 byte | -9,223,372,036,854,775,808 (-2^63) to 9,223,372,036,854,775,807 (2^63 - 1) |
| float |	0.0f |	4 byte |
| double |	0.0d |	8 byte |

### Unicode System
Unicode is a universal international standard character encoding that is capable of representing most of the world's written languages.

### Why java uses Unicode System?
Before Unicode, there were many language standards:
- ASCII (American Standard Code for Information Interchange) for the United States.
- ISO 8859-1 for Western European Language.
- KOI-8 for Russian.
- GB18030 and BIG-5 for chinese, and so on.

### Problem
This caused two problems:
1. A particular code value corresponds to different letters in the various language standards.
2. The encodings for languages with large character sets have variable length.Some common characters are encoded as single bytes, other require two or more byte.

### Solution
To solve these problems, a new language standard was developed i.e. Unicode System. In unicode, character holds 2 byte, so java also uses 2 byte for characters.

The Boolean data type specifies one bit of information, but its "size" can't be defined precisely.

## 2. Non-primitive data types
The non-primitive data types include **Classes, Interfaces**, and **Arrays**.

# Operators in Java
Operator in Java is a symbol that is used to perform operations. 

There are many types of operators in Java which are given below:

| Operator Type | Precedence |
| ------------- | ---------- |
| Unary | `expr++`  `expr--`  `++expr`  `--expr`  `+expr`  `-expr` `~` `!` |
| Arithmetic | `*`  `/`  `%`  `+`  `-` |
| Shift | `<<`  `>>`  `>>>` |
| Relational | `<`  `>`  `<=`  `>=`  `instanceof`  `==`  `!=` |
| Bitwise | `&`  `^`  `|` |
| Logical | `&&`  `||` |
| Ternary | `?` `:` |
| Assignment | `=` `+=` `-=` `*=` `/=` `%=` `&=` `^=` `|=` `<<=` `>>=` `>>>=` |
