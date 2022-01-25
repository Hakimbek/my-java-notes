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
