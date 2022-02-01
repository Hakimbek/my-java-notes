# Java Method References
Java provides a new feature called method reference in Java 8. Method reference is used to refer method of functional interface. It is compact and easy form of lambda expression. Each time when you are using lambda expression to just referring a method, you can replace your lambda expression with method reference.

## Types of Method References

- Reference to a static method.
- Reference to an instance method.
- Reference to a constructor.

# 1) Reference to a Static Method
You can refer to static method defined in the class. Following is the syntax and example which describe the process of referring static method in Java.

```java
interface Sayable {  
    void say();  
}  

public class MethodReference {  
    public static void saySomething() {  
        System.out.println("Hello, this is static method.");  
    }  
    
    public static void main(String[] args) {  
        // Referring static method  
        Sayable sayable = MethodReference::saySomething;  
        // Calling interface method  
        sayable.say();  
    }  
}  
```

### Output:
```
Hello, this is static method.
```

# 2) Reference to an Instance Method
like static methods, you can refer instance methods also. In the following example, we are describing the process of referring the instance method.

```java
interface Sayable {  
    void say();  
}  

public class InstanceMethodReference {  
    public void saySomething() {  
        System.out.println("Hello, this is non-static method.");  
    }  
    
    public static void main(String[] args) {  
        InstanceMethodReference methodReference = new InstanceMethodReference(); // Creating object  
        // Referring non-static method using reference  
        Sayable sayable = methodReference::saySomething;  
        // Calling interface method  
        sayable.say();  
        // Referring non-static method using anonymous object  
        Sayable sayable2 = new InstanceMethodReference()::saySomething; // You can use anonymous object also  
        // Calling interface method  
        sayable2.say();  
    }  
}  
```

### Output:
```
Hello, this is non-static method.
Hello, this is non-static method.
```

# 3) Reference to a Constructor
You can refer a constructor by using the new keyword. Here, we are referring constructor with the help of functional interface.

```java
interface Messageable {  
    Message getMessage(String msg);  
}  

class Message {  
    Message(String msg) {  
        System.out.print(msg);  
    }  
}  

public class ConstructorReference {  
    public static void main(String[] args) {  
        Messageable hello = Message::new;  
        hello.getMessage("Hello");  
    }  
}  
```

### Output:
```
Hello
```
