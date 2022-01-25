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
