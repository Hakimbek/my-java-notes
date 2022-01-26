# Java throw Exception
In Java, exceptions allows us to write good quality codes where the errors are checked at the compile time instead of runtime and we can create custom exceptions making the code recovery and debugging easier.

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
