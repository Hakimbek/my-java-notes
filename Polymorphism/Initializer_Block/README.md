# Instance initializer block
Instance Initializer block is used to initialize the instance data member. It run each time when object of the class is created.

```java
class Bike{  
    int speed;  
      
    Bike() {
      System.out.println("speed is "+speed);
    }  
   
    {speed=100;}  
       
    public static void main(String args[]) {  
      Bike b1 = new Bike();  
      Bike b2 = new Bike();  
    }      
}  
```

### Output:
```
speed is 100
speed is 100
```

## Rules for instance initializer block
- The instance initializer block is created when instance of the class is created.
- The instance initializer block is invoked after the parent class constructor is invoked (i.e. after super() constructor call).
- The instance initializer block comes in the order in which they appear.

```java
class A {  
  A() {  
    System.out.println("parent class constructor invoked");  
  }  
}  

class B extends A {  
  B() {  
    super();  
    System.out.println("child class constructor invoked");  
  }  
  
  {System.out.println("instance initializer block is invoked");}  
  
  public static void main(String args[]) {  
    B b = new B();  
  }  
}  
```

### Output:
```
parent class constructor invoked
instance initializer block is invoked
child class constructor invoked
```
