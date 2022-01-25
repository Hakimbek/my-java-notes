# Method Overloading in Java
If a class has multiple methods having same name but different in *parameters*, it is known as Method Overloading.

## Advantage of method overloading
 - Method overloading increases the readability of the program.

## There are two ways to overload the method in java

### By changing number of arguments

```java
class Adder {  
   static int add(int a, int b) {
      return a + b;
   }
 
   static int add(int a, int b, int c) {
      return a + b + c;
   }  
}  

class TestOverloading1 {  
   public static void main(String[] args) {  
     System.out.println(Adder.add(11, 11));  
     System.out.println(Adder.add(11, 11, 11));  
   }
} 
```

`Output: 22 33`

### By changing the data type
