# Java static keyword
The static keyword in Java is used for memory management mainly. We can apply static keyword with variables, methods, blocks and nested classes. The static keyword belongs to the class than an instance of the class.

The static can be:

## 1. Variable (also known as a class variable)
If you declare any variable as static, it is known as a static variable.

- The static variable can be used to refer to the common property of all objects (which is not unique for each object), for example, the company name of employees, college name of students, etc.
- The static variable gets memory only once in the class area at the time of class loading.
- Java static property is shared to all objects.

### Advantages of static variable
It makes your program memory efficient (i.e., it saves memory).

## 2. Java static method
If you apply static keyword with any method, it is known as static method.

- A static method belongs to the class rather than the object of a class.
- A static method can be invoked without the need for creating an instance of a class.
- A static method can access static data member and can change the value of it.

## 3. Java static block
- Is used to initialize the static data member.
- It is executed before the main method at the time of classloading.
