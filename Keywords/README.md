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

# Java Keywords
Java keywords are also known as reserved words. Keywords are particular words that act as a key to a code. These are predefined words by Java so they cannot be used as a variable or object name or class name.

| Key word | Description |
| -------- | ----------- |
| abstract | Java abstract keyword is used to declare an abstract class. An abstract class can provide the implementation of the interface. It can have abstract and non-abstract methods. |
| boolean | Java boolean keyword is used to declare a variable as a boolean type. It can hold True and False values only. |
| break | Java break keyword is used to break the loop or switch statement. It breaks the current flow of the program at specified conditions. |
| byte | Java byte keyword is used to declare a variable that can hold 8-bit data values. |
| case | Java case keyword is used with the switch statements to mark blocks of text. |
| catch | Java catch keyword is used to catch the exceptions generated by try statements. It must be used after the try block only. |
| char | Java char keyword is used to declare a variable that can hold unsigned 16-bit Unicode characters |
| class | Java class keyword is used to declare a class. |
| continue | Java continue keyword is used to continue the loop. It continues the current flow of the program and skips the remaining code at the specified condition. |
| default | Java default keyword is used to specify the default block of code in a switch statement. |
| do | Java do keyword is used in the control statement to declare a loop. It can iterate a part of the program several times. |
| double | Java double keyword is used to declare a variable that can hold 64-bit floating-point number. |
| else |  Java else keyword is used to indicate the alternative branches in an if statement. |
| enum | Java enum keyword is used to define a fixed set of constants. Enum constructors are always private or default. |
| extends | Java extends keyword is used to indicate that a class is derived from another class or interface. |
| final | Java final keyword is used to indicate that a variable holds a constant value. It is used with a variable. It is used to restrict the user from updating the value of the variable. |
| finally | Java finally keyword indicates a block of code in a try-catch structure. This block is always executed whether an exception is handled or not. |
| float | Java float keyword is used to declare a variable that can hold a 32-bit floating-point number. :
| for | Java for keyword is used to start a for loop. It is used to execute a set of instructions/functions repeatedly when some condition becomes true. If the number of iteration is fixed, it is recommended to use for loop. |
| if | Java if keyword tests the condition. It executes the if block if the condition is true. |
| implements | Java implements keyword is used to implement an interface. |
| import | Java import keyword makes classes and interfaces available and accessible to the current source code. |
| instanceof | Java instanceof keyword is used to test whether the object is an instance of the specified class or implements an interface. |
| int | Java int keyword is used to declare a variable that can hold a 32-bit signed integer. |
| interface | Java interface keyword is used to declare an interface. It can have only abstract methods. |
| long | Java long keyword is used to declare a variable that can hold a 64-bit integer. |
| native | Java native keyword is used to specify that a method is implemented in native code using JNI (Java Native Interface). |
| new | Java new keyword is used to create new objects. |
| null | Java null keyword is used to indicate that a reference does not refer to anything. It removes the garbage value. |
| package | Java package keyword is used to declare a Java package that includes the classes. |
| private | Java private keyword is an access modifier. It is used to indicate that a method or variable may be accessed only in the class in which it is declared. |
| protected | Java protected keyword is an access modifier. It can be accessible within the package and outside the package but through inheritance only. It can't be applied with the class. |
| public | Java public keyword is an access modifier. It is used to indicate that an item is accessible anywhere. It has the widest scope among all other modifiers. |
| return | Java return keyword is used to return from a method when its execution is complete. |
| short | Java short keyword is used to declare a variable that can hold a 16-bit integer. |
| static | Java static keyword is used to indicate that a variable or method is a class method. The static keyword in Java is mainly used for memory management. |
| strictfp | Java strictfp is used to restrict the floating-point calculations to ensure portability. |
| super | Java super keyword is a reference variable that is used to refer to parent class objects. It can be used to invoke the immediate parent class method. |
| switch | The Java switch keyword contains a switch statement that executes code based on test value. The switch statement tests the equality of a variable against multiple values. |
| synchronized | Java synchronized keyword is used to specify the critical sections or methods in multithreaded code. |
| this | Java this keyword can be used to refer the current object in a method or constructor. |
| throw | The Java throw keyword is used to explicitly throw an exception. The throw keyword is mainly used to throw custom exceptions. It is followed by an instance. |
| throws | The Java throws keyword is used to declare an exception. Checked exceptions can be propagated with throws. |
| transient | Java transient keyword is used in serialization. If you define any data member as transient, it will not be serialized. |
| try | Java try keyword is used to start a block of code that will be tested for exceptions. The try block must be followed by either catch or finally block. |
| void | Java void keyword is used to specify that a method does not have a return value. |
| volatile | Java volatile keyword is used to indicate that a variable may change asynchronously. |
| while | Java while keyword is used to start a while loop. This loop iterates a part of the program several times. If the number of iteration is not fixed, it is recommended to use the while loop. |