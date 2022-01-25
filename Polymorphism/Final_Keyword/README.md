# Final Keyword in Java
The final keyword in java is used to restrict the user. The java final keyword can be used in many context. Final can be:

## 1. Java final variable
If you make any variable as final, you cannot change the value of final variable(It will be constant).

```java
class Bike {  
    final int speedlimit = 90;  //final variable  
    
    void run() {  
        speedlimit=400;  
    }  
    
    public static void main(String args[]) {  
        Bike obj = new  Bike();  
        obj.run();  
    }  
}
```

### Output:
```
Compile Time Error
```

## 2. Java final method
If you make any method as final, you cannot override it.

```java
class Bike {  
    final void run(){
        System.out.println("running");
    }  
}  
     
class Honda extends Bike {  
    void run() {
        System.out.println("running safely with 100kmph");
    }  
     
    public static void main(String args[]) {  
        Honda honda = new Honda();  
        honda.run();     
    }  
}  
```

### Output:
```
Compile Time Error
```

## 3. Java final class
If you make any class as final, you cannot extend it.

```java
final class Bike{

}  
  
class Honda extends Bike {  
    void run() {
        System.out.println("running safely with 100kmph");
    }  
    
    public static void main(String args[]) {  
        Honda honda = new Honda();  
        honda.run();  
    }  
}  
```


### Output:
```
Compile Time Error
```

## Is final method inherited?
Yes, final method is inherited but you cannot override it.

## What is blank or uninitialized final variable?
What is blank or uninitialized final variable?
A final variable that is not initialized at the time of declaration is known as blank final variable.

If you want to create a variable that is initialized at the time of creating object and once initialized may not be changed, it is useful. 

It can be initialized only in constructor.

## Static blank final variable
A static final variable that is not initialized at the time of declaration is known as static blank final variable. It can be initialized only in static block.

## Can we declare a constructor final?
No, because constructor is never inherited.
