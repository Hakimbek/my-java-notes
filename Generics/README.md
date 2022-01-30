# Generics in Java
The Java Generics programming is introduced in J2SE 5 to deal with type-safe objects. It makes the code stable by detecting the bugs at compile time.

Before generics, we can store any type of objects in the collection, i.e., non-generic. Now generics force the java programmer to store a specific type of objects.

# Advantage of Java Generics
## Type-safety
We can hold only a single type of objects in generics. It does not allow to store other objects.

```java
List list = new ArrayList();    
list.add(10);  
list.add("10");  

// With Generics, it is required to specify the type of object we need to store.  

List<Integer> list = new ArrayList<Integer>();    
list.add(10);  
list.add("10"); // compile-time error  
```

## Type casting is not required
There is no need to typecast the object.

```java
List list = new ArrayList();    
list.add("hello");    
String s = (String) list.get(0); //typecasting    

// After Generics, we don't need to typecast the object.  

List<String> list = new ArrayList<String>();    
list.add("hello");    
String s = list.get(0);    
```

## Compile-Time Checking
It is checked at compile time so problem will not occur at runtime. The good programming strategy says it is far better to handle the problem at compile time than runtime.

```java
List<String> list = new ArrayList<String>();    
list.add("hello");    
list.add(32); //Compile Time Error    
```

# Generic class
A class that can refer to any type is known as a generic class. Here, we are using the *T* type parameter to create the generic class of specific type.

```java
class MyGen<T> {  
  T obj;  

  void add(T obj) {
     this.obj = obj;
  }  
  
  T get() {
     return obj;
  }  
}  
```

The T type indicates that it can refer to any type (like String, Integer, and Employee). The type you specify for the class will be used to store and retrieve the data.

```java
class TestGenerics {  
   public static void main(String args[]) {
      MyGen<Integer> m = new MyGen<Integer>();  
      m.add(2);  
      //m.add("vivek");  //Compile time error  
      System.out.println(m.get());  
   }
}  
```

### Output:
```
2
```

# Type Parameters
The type parameters naming conventions are important to learn generics thoroughly. The common type parameters are as follows:
- T - Type
- E - Element
- K - Key
- N - Number
- V - Value

# Generic Method
Like the generic class, we can create a generic method that can accept any type of arguments. Here, the scope of arguments is limited to the method where it is declared. It allows static as well as non-static methods.

```java
public class TestGenerics {  
   public static <E> void printArray(E[] elements) {  
        for ( E element : elements) {          
            System.out.println(element );  
        }  
        System.out.println();  
   }
   
   public static void main(String args[]) {  
        Integer[] intArray = {10, 20, 30, 40, 50};  
        Character[] charArray = {'J', 'A', 'V', 'A', 'T', 'P', 'O', 'I', 'N', 'T'};  
  
        System.out.println("Printing Integer Array");  
        printArray(intArray);   
  
        System.out.println("Printing Character Array");  
        printArray(charArray);   
   }   
} 
```

### Output:
```
Printing Integer Array
10
20
30
40
50
Printing Character Array
J
A
V
A
T
P
O
I
N
T
```

# Wildcard in Java Generics
The ? (question mark) symbol represents the wildcard element. It means any type. If we write \<? extends Number>, it means any child class of Number, e.g., Integer, Float, and double. Now we can call the method of Number class through any child class object.

We can use a wildcard as a type of a parameter, field, return type, or local variable. However, it is not allowed to use a wildcard as a type argument for a generic method invocation, a generic class instance creation, or a supertype.

```java
abstract class Shape {  
   abstract void draw();  
}  

class Rectangle extends Shape {  
   void draw() {
      System.out.println("drawing rectangle");
   }  
}  

class Circle extends Shape {  
   void draw() {
      System.out.println("drawing circle");
   }  
}  

class GenericTest {  
   //creating a method that accepts only child class of Shape  
   public static void drawShapes(List<? extends Shape> lists) {  
      for(Shape s : lists) {  
         s.draw(); //calling method of Shape class by child class instance  
      }  
   }  
   
   public static void main(String args[]) {  
      List<Rectangle> list1 = new ArrayList<Rectangle>();  
      list1.add(new Rectangle());  
  
      List<Circle> list2 = new ArrayList<Circle>();  
      list2.add(new Circle());  
      list2.add(new Circle());  
  
      drawShapes(list1);  
      drawShapes(list2);  
   }
}  
```

### Output:
```
drawing rectangle
drawing circle
drawing circle
```

# Upper Bounded Wildcards
The purpose of upper bounded wildcards is to decrease the restrictions on a variable. It restricts the unknown type to be a specific type or a subtype of that type. It is used by declaring wildcard character ("?") followed by the extends (in case of, class) or implements (in case of, interface) keyword, followed by its upper bound.

### Syntax
```
List<? extends Number>  
```

```java
public class UpperBoundWildcard { 
    private static Double add(ArrayList<? extends Number> num) {
        double sum = 0.0;   
        for (Number n : num) {  
            sum = sum + n.doubleValue();  
        } 
        return sum;  
    }  
  
    public static void main(String[] args) {  
        ArrayList<Integer> l1 = new ArrayList<Integer>();  
        l1.add(10);  
        l1.add(20);  
        System.out.println("displaying the sum =" + add(l1));  
          
        ArrayList<Double> l2 = new ArrayList<Double>();  
        l2.add(30.0);  
        l2.add(40.0);  
        System.out.println("displaying the sum =" + add(l2));  
    }  
}  
```
### Output:
```
displaying the sum = 30.0
displaying the sum = 70.0
```

# Unbounded Wildcards
The unbounded wildcard type represents the list of an unknown type such as List\<?>. This approach can be useful in the following scenarios: -

When the given method is implemented by using the functionality provided in the Object class.
When the generic class contains the methods that don't depend on the type parameter.

```java
public class UnboundedWildcard {  
  public static void display(List<?> list) {  
        for (Object o : list) {  
           System.out.println(o);  
        }  
  }  
  
  public static void main(String[] args) {        
     List<Integer> l1 = Arrays.asList(1, 2, 3);  
     System.out.println("displaying the Integer values");  
     display(l1);  
     List<String> l2 = Arrays.asList("One", "Two", "Three");  
     System.out.println("displaying the String values");  
     display(l2);  
  }  
}  
```

### Output:
```
displaying the Integer values
1
2
3
displaying the String values
One
Two
Three
```

# Lower Bounded Wildcards
The purpose of lower bounded wildcards is to restrict the unknown type to be a specific type or a supertype of that type. It is used by declaring wildcard character ("?") followed by the super keyword, followed by its lower bound.

### Syntax
```
List<? super Integer>  
```

```java
public class LowerBoundWildcard {  
    public static void addNumbers(List<? super Integer> list) {  
        for(Object n : list) {  
            System.out.println(n);  
        }  
    }  
    
    public static void main(String[] args) {    
       List<Integer> l1 = Arrays.asList(1, 2, 3);  
       System.out.println("displaying the Integer values");  
       addNumbers(l1);  
      
       List<Number> l2 = Arrays.asList(1.0, 2.0, 3.0);  
       System.out.println("displaying the Number values");  
       addNumbers(l2);  
   }  
}  
```

### Output:
```
displaying the Integer values
1
2
3
displaying the Number values
1.0
2.0
3.0
```
