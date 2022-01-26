# Call by Value and Call by Reference in Java
There is only call by value in java, not call by reference. If we call a method passing a value, it is known as call by value. The changes being done in the called method, is not affected in the calling method.

## Example of call by value in java
```java
class Operation {  
  int data = 50;  
  
  void change(int data) {  
     data = data + 100;  //changes will be in the local variable only  
  }  
     
  public static void main(String args[]) {  
     Operation op = new Operation();  
  
     System.out.println("before change " + op.data);  
     op.change(500);  
     System.out.println("after change " + op.data);  
  }  
}  
```

### Output:
```
before change 50
after change 50		
```

## Another Example of call by value in java
In case of call by reference original value is changed if we made changes in the called method.
```java
class Operation {  
   int data = 50;  
  
   void change(Operation op) {  
      op.data = op.data + 100;  //changes will be in the instance variable  
   }  
     
    
   public static void main(String args[]) {  
      Operation op = new Operation();  
  
      System.out.println("before change " + op.data);  
      op.change(op); //passing object  
      System.out.println("after change " + op.data);  
   }  
}  
```

### Output:
```
before change 50
after change 150		
```

# Java Strictfp Keyword
Java strictfp keyword ensures that you will get the same result on every platform if you perform operations in the floating-point variable. The precision may differ from platform to platform that is why java programming language have provided the strictfp keyword, so that you get same result on every platform. So, now you have better control over the floating-point arithmetic.

The strictfp keyword cannot be applied on abstract methods, variables or constructors.

# Java Command Line Arguments
The java command-line argument is an argument i.e. passed at the time of running the java program.

The arguments passed from the console can be received in the java program and it can be used as an input.

So, it provides a convenient way to check the behavior of the program for the different values. You can pass N (1,2,3 and so on) numbers of arguments from the command prompt.
