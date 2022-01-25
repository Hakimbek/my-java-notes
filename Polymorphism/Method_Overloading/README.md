# Method Overloading in Java
If a class has multiple methods having same name but different in *parameters*, it is known as Method Overloading.

## Advantage of method overloading
 - Method overloading increases the readability of the program.

# There are two ways to overload the method in java

## 1. By changing number of arguments

```java
class Adder {  
   static int add(int a, int b) {
      return a + b;
   }
 
   static int add(int a, int b, int c) {
      return a + b + c;
   }  
}  

class TestOverloading {  
   public static void main(String[] args) {  
     System.out.println(Adder.add(11, 11));  
     System.out.println(Adder.add(11, 11, 11));  
   }
} 
```
### Output:
``` 
22 
33
```

## 2. By changing the data type

```java
class Adder {  
   static int add(int a, int b) {
      return a + b;
   }
   
   static double add(double a, double b) {
      return a + b;
   }  
}  

class TestOverloading {  
   public static void main(String[] args) {  
       System.out.println(Adder.add(11, 11));  
       System.out.println(Adder.add(12.3, 12.6));  
   }
}  
```

### Output: 
```
22
24.9
```

## Note
In java, method overloading is not possible by changing the return type of the method only because of ambiguity. 

```java
class Adder {  
   static int add(int a, int b){
       return a + b;
   }  
   
   static double add(int a, int b){
       return a + b;
   }  
}  

class TestOverloading {  
    public static void main(String[] args) {  
       System.out.println(Adder.add(11, 11)); //ambiguity  
    }
}  
```

### Output:
```
Compile Time Error: method add(int, int) is already defined in class Adder
```

## Can we overload java main() method?
You can have any number of main methods in a class by method overloading. But JVM calls *main()* method which receives string array as arguments only.

```java
class TestOverloading {  
   public static void main(String[] args){
       System.out.println("main with String[]");
   }
   
   public static void main(String args){
       System.out.println("main with String");
   }
   
   public static void main(){
       System.out.println("main without args");
   }  
}  
```

### Output:
```
main with String[]
```

# Method Overloading and Type Promotion

![Type Promotion](/Polymorphism/Method_Overloading/image/char.png)

## Example of Method Overloading with TypePromotion

```java
class OverloadingCalculation {  
  void sum(int a, long b){
     System.out.println(a + b);
  }  
  
  void sum(int a, int b, int c){
     System.out.println(a + b + c);
  }  
  
  public static void main(String args[]) {  
     OverloadingCalculation obj = new OverloadingCalculation();  
     obj.sum(20, 20);  //now second int literal will be promoted to long  
     obj.sum(20, 20, 20);  
  }  
}  
```

### Output:
```
40
60
```

## Example of Method Overloading with Type Promotion if matching found

```java
class OverloadingCalculation {  
  void sum(int a, int b){
      System.out.println("int arg method invoked");
  }  
  
  void sum(long a, long b){
      System.out.println("long arg method invoked");
  }  
  
  public static void main(String args[]) {  
      OverloadingCalculation obj = new OverloadingCalculation();  
      obj.sum(20, 20);   //now int arg sum() method gets invoked  
  }  
}  
```

### Output:
```
int arg method invoked
```
