# Java
Java was developed by `Sun Microsystems` (which is now the subsidiary of `Oracle`) in the year 1995. James Gosling is known as the father of Java. Before Java, its name was Oak. Since Oak was already a registered company, so James Gosling and his team changed the name from Oak to Java.

Java is a **programming language** and a **platform**.

### Language
Java is a `high level`, `robust`, `object-oriented` and `secure` programming language.

### Platform
Any hardware or software environment in which a program runs, is known as a platform. Since Java has a runtime environment `JRE` and `API`, it is called a platform.

## Features of Java
The primary objective of Java programming language creation was to make it portable, simple and secure programming language. Apart from this, there are also some excellent features which play an important role in the popularity of this language. The features of Java are also known as Java buzzwords. A list of the most important features of the Java language is given below.

### Simple
Java is very easy to learn, and its syntax is simple, clean and easy to understand. According to Sun Microsystem, Java language is a simple programming language because:

- Java syntax is based on `C++` (so easier for programmers to learn it after `C++`).
- Java has removed many complicated and rarely-used features, for example, explicit pointers, operator overloading, etc.
- There is no need to remove unreferenced objects because there is an Automatic Garbage Collection in Java.

### Object-oriented
Java is an object-oriented programming language. Everything in Java is an object. Object-oriented means we organize our software as a combination of different types of objects that incorporate both data and behavior. Object-oriented programming (OOPs) is a methodology that simplifies software development and maintenance by providing some rules.

Basic concepts of OOPs are:

- Object
- Class
- Inheritance
- Polymorphism
- Abstraction
- Encapsulation

### Platform Independent
Java is platform independent because it is different from other languages like C, C++, etc. which are compiled into platform specific machines while Java is a write once, run anywhere language. A platform is the hardware or software environment in which a program runs.

There are two types of platforms software-based and hardware-based. Java provides a software-based platform.

The Java platform differs from most other platforms in the sense that it is a software-based platform that runs on top of other hardware-based platforms. It has two components:

1. Runtime Environment
2. API(Application Programming Interface)

Java code can be executed on multiple platforms, for example, Windows, Linux, Sun Solaris, Mac/OS, etc. Java code is compiled by the compiler and converted into bytecode. This bytecode is a platform-independent code because it can be run on multiple platforms, i.e., Write Once and Run Anywhere (WORA).

### Secured
Java is best known for its security. With Java, we can develop virus-free systems. Java is secured because:

### Robust
The English mining of Robust is strong. Java is robust because:

- It uses strong memory management.
- There is a lack of pointers that avoids security problems.
- Java provides automatic garbage collection which runs on the Java Virtual Machine to get rid of objects which are not being used by a Java application anymore.
- There are exception handling and the type checking mechanism in Java. All these points make Java robust.

### Architecture-neutral
Java is architecture neutral because there are no implementation dependent features, for example, the size of primitive types is fixed.

In C programming, *int* data type occupies 2 bytes of memory for 32-bit architecture and 4 bytes of memory for 64-bit architecture. However, it occupies 4 bytes of memory for both 32 and 64-bit architectures in Java.

### Portable
Java is portable because it facilitates you to carry the Java bytecode to any platform. It doesn't require any implementation.

### High-performance
Java is faster than other traditional interpreted programming languages because Java bytecode is "close" to native code. It is still a little bit slower than a compiled language (e.g., C++). Java is an interpreted language that is why it is slower than compiled languages, e.g., C, C++, etc.

### Distributed
Java is distributed because it facilitates users to create distributed applications in Java. RMI and EJB are used for creating distributed applications. This feature of Java makes us able to access files by calling the methods from any machine on the internet.

### Multi-threaded
A thread is like a separate program, executing concurrently. We can write Java programs that deal with many tasks at once by defining multiple threads. The main advantage of multi-threading is that it doesn't occupy memory for each thread. It shares a common memory area. Threads are important for multi-media, Web applications, etc.

### Dynamic
Java is a dynamic language. It supports the dynamic loading of classes. It means classes are loaded on demand. It also supports functions from its native languages, i.e., C and C++.

## **Java Core**
 - [JVM, JRE, JDK](Java_Core/JVM_JRE_JDK/README.md)
 - [Variables](Java_Core/Variables/README.md)
 - [Data_Types](Java_Core/Data_Types/README.md)
 - [Operators](Java_Core/Operators/README.md)
 - [Keywords](Java_Core/Keywords/README.md)
 - ### Java Control Statements
   - [Decision-making statements](Java_Core/Control_Statements/Decision_Making_Statements/README.md)
   - [Loop statements](Java_Core/Control_Statements/Loop_Statements/README.md)
   - [Jump statements](Java_Core/Control_Statements/Jump_Statements/README.md) 

 - [Comments](Java_Core/Comments/README.md)
 - [Java Naming Convention](Java_Core/Convention/README.md)
 - [Arrays](Java_Core/Arrays/README.md)

# OOPs (Object-Oriented Programming System)
Object means a real-world entity such as a pen, chair, table, computer, watch, etc. Object-Oriented Programming is a methodology or paradigm to design a program using classes and objects. It simplifies software development and maintenance by providing some concepts:

- Object
- Class
- Inheritance
- Polymorphism
- Abstraction
- Encapsulation

Apart from these concepts, there are some other terms which are used in Object-Oriented design:

- Coupling
- Cohesion
- Association
- Aggregation
- Composition

## Coupling
Coupling refers to the knowledge or information or dependency of another class. It arises when classes are aware of each other. If a class has the details information of another class, there is strong coupling. In Java, we use private, protected, and public modifiers to display the visibility level of a class, method, and field. You can use interfaces for the weaker coupling because there is no concrete implementation.

## Cohesion
Cohesion refers to the level of a component which performs a single well-defined task. A single well-defined task is done by a highly cohesive method. The weakly cohesive method will split the task into separate parts. The java.io package is a highly cohesive package because it has I/O related classes and interface. However, the java.util package is a weakly cohesive package because it has unrelated classes and interfaces.

## Association
Association represents the relationship between the objects. Here, one object can be associated with one object or many objects. There can be four types of association between the objects:

- One to One
- One to Many
- Many to One, and
- Many to Many

Association can be undirectional or bidirectional.

## Aggregation
If a class have an entity reference, it is known as Aggregation. Aggregation represents HAS-A relationship.
Aggregation is a way to achieve Association. Aggregation represents the relationship where one object contains other objects as a part of its state. It represents the weak relationship between objects. It is another way to reuse objects.

### When use Aggregation?
- Code reuse is also best achieved by aggregation when there is no is-a relationship.
- Inheritance should be used only if the relationship is-a is maintained throughout the lifetime of the objects involved; otherwise, aggregation is the best choice.

## Composition
The composition is also a way to achieve Association. The composition represents the relationship where one object contains other objects as a part of its state. There is a strong relationship between the containing object and the dependent object. It is the state where containing objects do not have an independent existence. If you delete the parent object, all the child objects will be deleted automatically.

# Advantage of OOPs over Procedure-oriented programming language
1. OOPs makes development and maintenance easier, whereas, in a procedure-oriented programming language, it is not easy to manage if code grows as project size increases.

2. OOPs provides data hiding, whereas, in a procedure-oriented programming language, global data can be accessed from anywhere.

3. OOPs provides the ability to simulate real-world event much more effectively. We can provide the solution of real word problem if we are using the Object-Oriented Programming language.

## Object Orianted Programming
 - [Class](OOP/Class/README.md)
 - [Object](OOP/Object/README.md)
 - [Difference between Object and Class](OOP/Difference/README.md)
 - [This keyword](OOP/This_Keyword/README.md)
 - [Static keyword](OOP/Static/README.md)
 - [Inheritance](OOP/Inheritance/README.md)
 - ### Polymorphism
   - [Method Overloading](OOP/Polymorphism/Method_Overloading//README.md)
   - [Method Overriding](OOP/Polymorphism/Method_Overriding/README.md)
   - [Difference between Overriding and Overloading](OOP/Polymorphism/Difference/README.md)
   - [Super Keyword](OOP/Polymorphism/Super_Keyword/README.md)
   - [Initializer block](OOP/Polymorphism/Initializer_Block/README.md)
   - [Final Keyword](OOP/Polymorphism/Final_Keyword/README.md)
   - [Casting](OOP/Polymorphism/Casting/README.md)
   - [Binding](OOP/Polymorphism/Binding/README.md)

 - ### Abstraction
   - [Abstract class](OOP/Abstraction/Abstract_Class/README.md)
   - [Interface](OOP/Abstraction/Interface/README.md)
   - [Difference between abstract class and interface](OOP/Abstraction/Difference/README.md)
   
 - ### [Encapsulation](OOP/Encapsulation/Encapsulation/README.md)
   - [Package](OOP/Encapsulation/Package/README.md)
   - [Access modifiers](OOP/Encapsulation/Access_Modifiers/README.md)

### [Object class](Object_Class/README.md)
### [Math class](Math/README.md)
### [Wrapper Class](Wrapper_Class/README.md)
### [Misc](Misc/README.md)

## String
 - [Immutable String](String/Immutable_String/README.md)
 - [String Builder, String Buffer](String/Builder/README.md)
 - [String Methods](String/Methods/README.md)
 - [Immutable class](String/Buffer/README.md)
## [Java Regex](Regex/README.md)

## Exception Handling
 - [Exceptions](Exception/Exceptions/README.md)
 - [Try-catch block](Exception/Try_catch/README.md)
 - [Throw and Throws](Exception/Throw/README.md)
 - [Final, Finally and Finalize](Exception/fff/README.md)
 - [Exception Handling with Method Overriding](Exception/Overriding/README.md)
 - [Custom Exceptions](Exception/Custom/README.md)
## [Inner class](Inner_class/README.md)

## Mutithreading
  - [What is Multithreading?](Multithreading/What_is_multithreading/README.md)
  - [Life Cycle of Thread](Multithreading/Cycle/README.md)
  - [How to create Thread in Java](Multithreading/Create/README.md)
  - ### Methods
      - [sleep()](Multithreading/Methods/Sleep/README.md)
      - [run()](Multithreading/Methods/Run/README.md)
      - [join()](Multithreading/Methods/Join/README.md)
      - [name](Multithreading/Methods/Name/README.md)
      - [priority](Multithreading/Priority/README.md)
      - [deamon](Multithreading/Deamon/README.md)
      - [pool](Multithreading/Pool/README.md)
### [Synchronization](Synchronization/README.md)
  - [notify(), notifyAll(), wait()](Synchronization/Methods/README.md)

### [Garbage Collection](GC/README.md)

## Java Networking
 - [Networking Concepts](Network/Consept/README.md)
 - [URL class](Network/URL/README.md)
 - [URLConnection class](Network/Connection/README.md)
 - [HttpURLConnection class](Network/HTTP/README.md)
 
## Java I/O
 - [Java Input/Output](IO/JavaIO/README.md)
 - [File Input/Output Stream](IO/FileIOStream/README.md)
 - [Buffered Input/Output Stream](IO/BufferedIOStream/README.md)
 - [Writer/Reader](IO/WriterReader/README.md)
 - [File Writer/Reader](IO/FileWR/README.md)
 - [Buffered Writer/Reader](IO/BufferedWR/README.md)
 - [File](IO/File/README.md)
 - [Serialization](IO/Serialization/README.md)
  
## Java Collections
 - [Collection Framework](Collections/CollectionFramework/README.md)
 - [List](Collections/List/README.md)
 - [Set](Collections/Set/README.md)
 - [Queue, Deque](Collections/Queue/README.md)
 - [Map](Collections/Map/README.md)
 - [Collections class](Collections/Collections/README.md)
 - [Iterator](Collections/Iterator/README.md)

## New Features
 - [Generics](New_Features/Generics/README.md)
 - [Annotations](New_Features/Annotations/README.md)
 - [Enums](New_Features/Enums/README.md)
 - [Variable Arguments](New_Features/VarArg/README.md)
 - [Lambda Expressions](New_Features/Lambda/README.md)
 - [Java Methods Reference](New_Features/Method_Reference/README.md)
 - [Functional Interfaces](New_Features/Functional_Interfaces/README.md)
 - [Optional class](New_Features/Optional/README.md)
 - [Stream](New_Features/Stream/README.md)
