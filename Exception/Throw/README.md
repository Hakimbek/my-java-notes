# Java throw Exception
In Java, exceptions allows us to write good quality codes where the errors are checked at the compile time instead of runtime and we can create custom exceptions making the code recovery and debugging easier.

# Java throws keyword
The Java throws keyword is used to declare an exception. It gives an information to the programmer that there may occur an exception. So, it is better for the programmer to provide the exception handling code so that the normal flow of the program can be maintained.

Exception Handling is mainly used to handle the checked exceptions. If there occurs any unchecked exception such as NullPointerException, it is programmers' fault that he is not checking the code before it being used.

## Advantage of Java throws keyword
Now Checked Exception can be propagated (forwarded in call stack).

### Syntax of Java throws
```java
return_type method_name() throws exception_class_name {  
     //method code  
}  
```

# Java throws Example
```java
class Testthrows {  
    void m() throws IOException {  
        throw new IOException("device error");  //checked exception  
    }  
    
    void n() throws IOException {   
        m();  
    }  
    
    void p() {  
        try {  
            n();  
        } catch(Exception e) {
            System.out.println("exception handled");
        }  
    }
    
    public static void main(String args[]) {  
        Testthrows1 obj = new Testthrows1();  
        obj.p();  
        System.out.println("normal flow...");  
    }  
}  
```

### Output:
```
exception handled
normal flow...
```

## Rule
If we are calling a method that declares an exception, we must either caught or declare the exception.

# There are two cases
## Case 1: Handle Exception Using try-catch block
## Case 2: Declare Exception
- In case we declare the exception, if exception does not occur, the code will be executed fine.
- In case we declare the exception and the exception occurs, it will be thrown at runtime because throws does not handle the exception.

# Java throw keyword
The Java throw keyword is used to throw an exception explicitly.

We specify the exception object which is to be thrown. The Exception has some message with it that provides the error description. These exceptions may be related to user inputs, server, etc.

We can throw either checked or unchecked exceptions in Java by throw keyword. It is mainly used to throw a custom exception. 

We can also define our own set of conditions and throw an exception explicitly using throw keyword. For example, we can throw ArithmeticException if we divide a number by another number. Here, we just need to set the condition and throw exception using throw keyword.

```java
throw new exception_class("error message");  
```

## Example

```java
public class TestThrow {   
    //function to check if person is eligible to vote or not   
    public static void validate(int age) {  
        if(age < 18) {  
            //throw Arithmetic exception if not eligible to vote  
            throw new ArithmeticException("Person is not eligible to vote");    
        } else {  
            System.out.println("Person is eligible to vote!!");  
        }  
    }  
    
    //main method  
    public static void main(String args[]) {  
        //calling the function  
        validate(13);  
        System.out.println("rest of the code...");    
  }    
}    
```

## Note
- If we throw unchecked exception from a method, it is must to handle the exception or declare in throws clause.
- If we throw a checked exception using throw keyword, it is must to handle the exception using catch block or the method must declare it using throws declaration.
- Every subclass of Error and RuntimeException is an unchecked exception in Java. A checked exception is everything else under the Throwable class.
