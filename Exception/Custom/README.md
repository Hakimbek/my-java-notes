# Java Custom Exception
In Java, we can create our own exceptions that are derived classes of the Exception class. Creating our own Exception is known as custom exception or user-defined exception. Basically, Java custom exceptions are used to customize the exception according to user need.

Consider the example in which InvalidAgeException class extends the Exception class.

Using the custom exception, we can have your own exception and message. Here, we have passed a string to the constructor of superclass i.e. Exception class that can be obtained using getMessage() method on the object we have created.

```java
public class WrongFileNameException extends Exception {  
    public WrongFileNameException(String errorMessage) {  
        super(errorMessage);  
    }  
}  
```

## Note
We need to write the constructor that takes the String as the error message and it is called parent class constructor.
