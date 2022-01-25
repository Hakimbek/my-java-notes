# Method Overriding in Java
If subclass (child class) has the same method as declared in the parent class, it is known as method overriding in Java.

## Usage of Java Method Overriding
- Method overriding is used to provide the specific implementation of a method which is already provided by its superclass.
- Method overriding is used for runtime polymorphism

## Rules for Java Method Overriding
- The method must have the same name as in the parent class
- The method must have the same parameter as in the parent class.
- There must be an *IS-A* relationship (inheritance).

```java
//Creating a parent class. 
class Vehicle {  
  //defining a method  
  void run() {
      System.out.println("Vehicle is running");
  }  
} 

//Creating a child class  
class Bike extends Vehicle {  
  //defining the same method as in the parent class  
  void run() { 
      System.out.println("Bike is running safely");
  }  
  
  public static void main(String args[]) {  
      Bike obj = new Bike();  //creating object  
      obj.run();  //calling method  
  }  
}  
```

### Output:
```
Bike is running safely
```

## Can we override static method?
No, a static method cannot be overridden. It is because the static method is bound with class whereas instance method is bound with an object. Static belongs to the class area, and an instance belongs to the heap area.

## Can we override java main method?
No, because the main is a static method.

# Covariant Return Type
The covariant return type specifies that the return type may vary in the same direction as the subclass.

Before Java5, it was not possible to override any method by changing the return type. But now, since Java5, it is possible to override method by changing the return type if subclass overrides any method whose return type is Non-Primitive but it changes its return type to subclass type.

```java
class A {    
    A get() {
        return this;
    }    
}    
    
class B extends A {    
    @Override  
    B get() {
        return this;
    }   
    
    void message() { 
        System.out.println("welcome to covariant return type");
    }    
    
    public static void main(String args[]) {    
        new B1().get().message();    
    }    
}    
```

### Output:
```
welcome to covariant return type
```

## Advantages of Covariant Return Type
- Covariant return type assists to stay away from the confusing type casts in the class hierarchy and makes the code more usable, readable, and maintainable.

- In the method overriding, the covariant return type provides the liberty to have more to the point return types.

- Covariant return type helps in preventing the run-time *ClassCastExceptions* on returns.
