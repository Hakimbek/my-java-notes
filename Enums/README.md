# Java Enums
The Enum in Java is a data type which contains a fixed set of constants.

It can be used for days of the week (SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, and SATURDAY) , directions (NORTH, SOUTH, EAST, and WEST), season (SPRING, SUMMER, WINTER, and AUTUMN or FALL), colors (RED, YELLOW, BLUE, GREEN, WHITE, and BLACK) etc. According to the Java naming conventions, we should have all constants in capital letters. So, we have enum constants in capital letters.

Java Enums can be thought of as classes which have a fixed set of constants (a variable that does not change). The Java enum constants are static and final implicitly. It is available since JDK 1.5.

Enums are used to create our own data type like classes. The enum data type (also known as Enumerated Data Type) is used to define an enum in Java. 

Java Enum internally inherits the Enum class, so it cannot inherit any other class, but it can implement many interfaces. We can have fields, constructors, methods, and main methods in Java enum.

# Points to remember for Java Enum
- Enum improves type safety
- Enum can be easily used in switch
- Enum can be traversed
- Enum can have fields, constructors and methods
- Enum may implement many interfaces but cannot extend any class because it internally extends Enum class

```java
class EnumExample {  
   //defining the enum inside the class  
   public enum Season {WINTER, SPRING, SUMMER, FALL}  
   //main method  
   public static void main(String[] args) {  
      //traversing the enum  
      for (Season s : Season.values())  
         System.out.println(s);  
   }
}  
```

### Output:
```
WINTER
SPRING
SUMMER
FALL
```

## Note
Java compiler internally adds values(), valueOf() and ordinal() methods within the enum at compile time. It internally creates a static and final class for the enum.

## What is the purpose of the values() method in the enum?
The Java compiler internally adds the values() method when it creates an enum. The values() method returns an array containing all the values of the enum.

## What is the purpose of the valueOf() method in the enum?
The Java compiler internally adds the valueOf() method when it creates an enum. The valueOf() method returns the value of given constant enum.

## What is the purpose of the ordinal() method in the enum?
The Java compiler internally adds the ordinal() method when it creates an enum. The ordinal() method returns the index of the enum value.

# Defining Java Enum
The enum can be defined within or outside the class because it is similar to a class. The semicolon (;) at the end of the enum constants are optional. For example:
```java
enum Season {WINTER, SPRING, SUMMER, FALL}  
```
Or,
```java
enum Season {WINTER, SPRING, SUMMER, FALL;}  
```

## Java Enum Example: Defined outside class
```java
enum Season { WINTER, SPRING, SUMMER, FALL }  
class EnumExample {  
   public static void main(String[] args) {  
      Season s = Season.WINTER;  
      System.out.println(s);  
   }
}   
```

## Java Enum Example: Defined inside class
```java
class EnumExample {  
   enum Season { WINTER, SPRING, SUMMER, FALL; }  //semicolon(;) is optional here  
   public static void main(String[] args) {  
      Season s = Season.WINTER; //enum type is required to access WINTER  
      System.out.println(s);  
   }
}  
```

# Initializing specific values to the enum constants
The enum constants have an initial value which starts from 0, 1, 2, 3, and so on. But, we can initialize the specific value to the enum constants by defining fields and constructors. As specified earlier, Enum can have fields, constructors, and methods.

## Example of specifying initial value to the enum constants
```java
class EnumExample {  
   enum Season {   
      WINTER(5), SPRING(10), SUMMER(15), FALL(20);   
  
      private int value;  
      private Season(int value) {  
         this.value=value;  
      }  
   }
   
   public static void main(String args[]){  
      for (Season s : Season.values())  
         System.out.println(s + " " + s.value);  
   }
}  
```

### Output:
```
WINTER 5
SPRING 10
SUMMER 15
FALL 20
```

## Can we create the instance of Enum by new keyword?
No, because it contains private constructors only.

## Can we have an abstract method in the Enum?
Yes, Of course! we can have abstract methods and can provide the implementation of these methods.
