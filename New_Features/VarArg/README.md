# Variable Argument (Varargs):
The varrags allows the method to accept zero or muliple arguments. Before varargs either we use overloaded method or take an array as the method parameter but it was not considered good because it leads to the maintenance problem. If we don't know how many argument we will have to pass in the method, varargs is the better approach.

## Advantage of Varargs:
We don't have to provide overloaded methods so less code.

## Syntax of varargs:
```java
return_type method_name(data_type... variableName){}  
```

```java
class VarargsExample {  
  static void display(String... values) {  
     System.out.println("display method invoked ");  
  }  
  
  public static void main(String args[]) {   
     display(); //zero argument   
     display("my", "name", "is", "varargs"); //four arguments  
  }   
}  
```

### Output:
```
display method invoked
display method invoked
```

# Rules for varargs:
- There can be only one variable argument in the method.
- Variable argument (varargs) must be the last argument.
