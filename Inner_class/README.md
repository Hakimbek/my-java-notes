# Java Inner Classes (Nested Classes)
Java inner class or nested class is a class that is declared inside the class or interface.

## Advantage of Java inner classes
1. Nested classes represent a particular type of relationship that is it can access all the members (data members and methods) of the outer class, including private.
2. Nested classes are used to develop more readable and maintainable code because it logically group classes and interfaces in one place only.
3. Code Optimization: It requires less code to write.

# Types of Nested classes

| Type |	Description |
| ---- | ----------- |
| Member Inner Class |	A class created within class and outside method. |
| Anonymous Inner Class |	A class created for implementing an interface or extending class. The java compiler decides its name. |
| Local Inner Class |	A class was created within the method. |
| Static Nested Class |	A static class was created within the class. |
| Nested Interface |	An interface created within class or interface. |

# Java Member Inner class
A non-static class that is created inside a class but outside a method is called member inner class. It is also known as a regular inner class. It can be declared with access modifiers like public, default, private, and protected.

```java
class Outer {  
   //code  
   class Inner {  
      //code  
   }  
}  
```

## How to instantiate Member Inner class in Java?
An object or instance of a member's inner class always exists within an object of its outer class. The new operator is used to create the object of member inner class with slightly different syntax.

```java
OuterClassReference.new MemberInnerClassConstructor();  
```

# Java Anonymous inner class
Java anonymous inner class is an inner class without a name and for which only a single object is created. An anonymous inner class can be useful when making an instance of an object with certain "extras" such as overloading methods of a class or interface, without having to actually subclass a class.

In simple words, a class that has no name is known as an anonymous inner class in Java. It should be used if you have to override a method of class or interface. Java Anonymous inner class can be created in two ways:

### 1. Class (may be abstract or concrete).

```java
abstract class Person {  
    abstract void eat();  
}  

class TestAnonymousInner {  
    public static void main(String args[]) {  
       Person p = new Person() {  
           void eat() {
               System.out.println("nice fruits");
           }  
       };  
       p.eat();  
    }  
}  
```

### Internal working of given code
1. A class is created, but its name is decided by the compiler, which extends the Person class and provides the implementation of the eat() method.
2. An object of the Anonymous class is created that is referred to by 'p,' a reference variable of Person type.

### 2. Interface

```java
interface Eatable {  
    void eat();  
}  

class TestAnnonymousInner {  
    public static void main(String args[]) {  
       Eatable e = new Eatable() {  
           public void eat(){
               System.out.println("nice fruits");
           }  
       };  
       e.eat();  
    }  
}  
```

### Internal working of given code
1. A class is created, but its name is decided by the compiler, which implements the Eatable interface and provides the implementation of the eat() method.
2. An object of the Anonymous class is created that is referred to by 'p', a reference variable of the Eatable type.

# Java Local inner class
A class i.e., created inside a method, is called local inner class in java. Local Inner Classes are the inner classes that are defined inside a block. Generally, this block is a method body. Sometimes this block can be a for loop, or an if clause. Local Inner classes are not a member of any enclosing classes. They belong to the block they are defined within, due to which local inner classes cannot have any access modifiers associated with them. However, they can be marked as final or abstract. These classes have access to the fields of the class enclosing it.

```java
public class localInner {  
  private int data = 30; //instance variable  
 
  void display() {  
     class Local {  
        void msg() {
            System.out.println(data);
        }  
     }  
  
     Local l = new Local();  
     l.msg();  
  }  
 
  public static void main(String args[]) {  
     localInner obj = new localInner();  
     obj.display();   
  }  
}  
```

# Java static nested class
A static class is a class that is created inside a class, is called a static nested class in Java.

- It can access static data members of the outer class, including private.
- The static nested class cannot access non-static (instance) data members

```java
class TestOuter {  
    static int data = 30;  
    
    static class Inner {  
       void msg() {
          System.out.println("data is " + data);
       }  
    }  
  
    public static void main(String args[]){  
       TestOuter.Inner obj = new TestOuter.Inner();  
       obj.msg();  
    }  
} 
```

# Java Nested Interface
An interface, i.e., declared within another interface or class, is known as a nested interface. The nested interfaces are used to group related interfaces so that they can be easy to maintain. The nested interface must be referred to by the outer interface or class. It can't be accessed directly.

```java
interface Showable {  
   void show();  
   
   interface Message {  
     void msg();  
   }  
}  

class TestNestedInterface implements Showable.Message {  
  public void msg() {
     System.out.println("Hello nested interface");
  }  
  
  public static void main(String args[]) {  
    Showable.Message message = new TestNestedInterface(); //upcasting here  
    message.msg();  
  }  
} 
```
