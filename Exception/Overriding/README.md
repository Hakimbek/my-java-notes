# Exception Handling with Method Overriding in Java
There are many rules if we talk about method overriding with exception handling.

## Rule 1
If the superclass method does not declare an exception, subclass overridden method cannot declare the checked exception.

```java
class Parent {
    // defining the method   
    void msg() {  
       System.out.println("parent method");  
    }    
}    
    
public class TestExceptionChild extends Parent {    
   // overriding the method in child class  
   // gives compile time error  
   void msg() throws IOException {    
      System.out.println("TestExceptionChild");    
   }  
  
   public static void main(String args[]) {    
      Parent p = new TestExceptionChild();    
      p.msg();    
   }    
}    
```

### Output:
```
Error
```

```java
class Parent {
    // defining the method   
    void msg() {  
       System.out.println("parent method");  
    }    
}    
    
public class TestExceptionChild extends Parent {    
   // overriding the method in child class  
   // gives compile time error  
   void msg() throws ArithmeticException {    
      System.out.println("TestExceptionChild");    
   }  
  
   public static void main(String args[]) {    
      Parent p = new TestExceptionChild();    
      p.msg();    
   }    
}    
```

### Output:
```
child method
```

## Rule 2
If the superclass method declares an exception, subclass overridden method can declare the same subclass exception or no exception but cannot declare parent exception.

```java
class Parent {    
   void msg() throws ArithmeticException {  
      System.out.println("parent method");  
   }    
}    
    
public class TestExceptionChild extends Parent {    
   void msg() throws Exception {  
      System.out.println("child method");  
   }    
    
   public static void main(String args[]) {    
      Parent p = new TestExceptionChild2();    

      try {    
         p.msg();    
      } catch (Exception e){
     
      }   
      
   }    
}     
```

### Output:
```
Error
```

```java
class Parent {    
    void msg() throws Exception {  
      System.out.println("parent method");  
   }    
}    
    
public class TestExceptionChild extends Parent {    
   void msg() throws Exception {  
      System.out.println("child method");  
   }    
    
   public static void main(String args[]) {    
      Parent p = new TestExceptionChild2();    

      try {    
         p.msg();    
      } catch (Exception e){
     
      }   
      
   }    
}     
```

### Output:
```
child method
```
