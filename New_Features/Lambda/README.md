# Java Lambda Expressions
Lambda expression is a new and important feature of Java which was included in Java SE 8. It provides a clear and concise way to represent one method interface using an expression. It is very useful in collection library. It helps to iterate, filter and extract data from collection.

The Lambda expression is used to provide the implementation of an interface which has functional interface. It saves a lot of code. In case of lambda expression, we don't need to define the method again for providing the implementation. Here, we just write the implementation code.

Java lambda expression is treated as a function, so compiler does not create .class file.

# Functional Interface
Lambda expression provides implementation of functional interface. An interface which has only one abstract method is called functional interface. Java provides an anotation @FunctionalInterface, which is used to declare an interface as functional interface.

# Why use Lambda Expression
- To provide the implementation of Functional interface.
- Less coding.

## Java Lambda Expression Syntax
```java
(argument-list) -> {body}  
```

## Java lambda expression is consisted of three components.

1. **Argument-list:** It can be empty or non-empty as well.

2. **Arrow-token:** It is used to link arguments-list and body of expression.

3. **Body:** It contains expressions and statements for lambda expression.

### No Parameter Syntax
```java
() -> {  
  //Body of no parameter lambda  
} 
```
### One Parameter Syntax
```java
(p1) -> {  
  //Body of single parameter lambda  
}  
```
### Two Parameter Syntax
```java
(p1, p2) -> {  
  //Body of multiple parameter lambda  
}  
```

# Without Lambda Expression
Let's see a scenario where we are not implementing Java lambda expression. Here, we are implementing an interface without using lambda expression.

```java
interface Drawable {  
    public void draw();  
}  

public class LambdaExpressionExample {  
    public static void main(String[] args) {  
        int width = 10;  
  
        //without lambda, Drawable implementation using anonymous class  
        Drawable d = new Drawable() {  
            public void draw() {
               System.out.println("Drawing " + width);
            }  
        };  
        d.draw();  
    }  
}  
```

### Output:
```
Drawing 10
```

# Java Lambda Expression Example
Now, we are going to implement the above example with the help of Java lambda expression.

```java
@FunctionalInterface  //It is optional  
interface Drawable {  
    public void draw();  
}  
  
public class LambdaExpressionExample {  
    public static void main(String[] args) {  
        int width = 10;  
          
        //with lambda  
        Drawable d2 = () -> {  
            System.out.println("Drawing " + width);  
        };  
        d2.draw();  
    }  
}  
```

### Output:
```
Drawing 10
```

# Java Lambda Expression Example: No Parameter
A lambda expression can have zero or any number of arguments. Let's see the examples:

```java
interface Sayable {  
    public String say();  
}  

public class LambdaExpressionExample {  
   public static void main(String[] args) {  
      Sayable s = () -> {  
          return "I have nothing to say.";  
      };  
      System.out.println(s.say());  
   }  
}  
```

### Output:
```
I have nothing to say.
```

# Java Lambda Expression Example: Single Parameter

```java
interface Sayable {  
    public String say(String name);  
}  
  
public class LambdaExpressionExample {  
    public static void main(String[] args) {  
        // Lambda expression with single parameter.  
        Sayable s1 = (name) -> {  
            return "Hello, " + name;  
        };  
        System.out.println(s1.say("Sonoo"));  
          
        // You can omit function parentheses    
        Sayable s2 = name -> {  
            return "Hello, " + name;  
        };  
        System.out.println(s2.say("Sonoo"));  
    }  
}  
```

### Output:
```
Hello, Sonoo
Hello, Sonoo
```

# Java Lambda Expression Example: Multiple Parameters

```java
interface Addable {  
    int add(int a, int b);  
}  
  
public class LambdaExpressionExample {  
    public static void main(String[] args) {  
        // Multiple parameters in lambda expression  
        Addable ad1 = (a, b) -> (a + b);  
        System.out.println(ad1.add(10, 20));  
          
        // Multiple parameters with data type in lambda expression  
        Addable ad2 = (int a, int b) -> (a + b);  
        System.out.println(ad2.add(100, 200));  
    }  
}  
```

### Output:
```
30
300
```

# Java Lambda Expression Example: with or without return keyword
In Java lambda expression, if there is only one statement, you may or may not use return keyword. You must use return keyword when lambda expression contains multiple statements.

```java
interface Addable{  
    int add(int a,int b);  
}  
  
public class LambdaExpressionExample  {  
    public static void main(String[] args) {  
        // Lambda expression without return keyword.  
        Addable ad1 = (a, b) -> (a + b);  
        System.out.println(ad1.add(10, 20));  
          
        // Lambda expression with return keyword.    
        Addable ad2 = (int a, int b) -> {  
              return (a + b);   
        };  
        System.out.println(ad2.add(100, 200));  
    }  
}  
```

### Output:
```
30
300
```
