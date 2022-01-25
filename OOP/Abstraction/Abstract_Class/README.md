# Abstraction
Hiding internal details and showing functionality is known as abstraction. For example phone call, we don't know the internal processing.

## Ways to achieve Abstraction
1. Abstract class (0 to 100%)
2. Interface (100%)

# Abstract class in Java

A class which is declared as abstract is known as an abstract class. It can have abstract and non-abstract methods. It needs to be extended and its method implemented. It cannot be instantiated.

## Points to Remember
- An abstract class must be declared with an abstract keyword.
- It can have abstract and non-abstract methods.
- It cannot be instantiated.
- It can have constructors and static methods also.
- It can have final methods which will force the subclass not to change the body of the method.

### Abstract class

```java
abstract class A{

}  
```

# Abstract Method in Java
A method which is declared as abstract and does not have implementation is known as an abstract method.

### Abstract method

```java
abstract void printStatus();//no method body and abstract  
```

```java
abstract class Bike {  
    abstract void run();  
}  

class Honda extends Bike {  
    void run(){System.out.println("running safely");}  
    
    public static void main(String args[]) {  
        Bike obj = new Honda();  
        obj.run();  
    }   
}  
```

### Output:
```
running safely
```

## Rule
- If there is an abstract method in a class, that class must be abstract.
- If you are extending an abstract class that has an abstract method, you must either provide the implementation of the method or make this class abstract.
