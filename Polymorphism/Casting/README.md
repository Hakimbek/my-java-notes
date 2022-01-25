# Upcasting
If the reference variable of Parent class refers to the object of Child class, it is known as upcasting.

```java
class A {

}  

class B extends A {

}  

A a = new B();  //upcasting  
```

# Downcasting 
When Subclass type refers to the object of Parent class, it is known as downcasting. If we perform it directly, compiler gives Compilation error. If you perform it by typecasting, ClassCastException is thrown at runtime. But if we use instanceof operator, downcasting is possible.

```java
B b = new A(); //Compilation error  

B b = (B) new A(); 
//Compiles successfully but ClassCastException is thrown at runtime    
```

# Java *instanceof*
The java instanceof operator is used to test whether the object is an instance of the specified type (class or subclass or interface).

The instanceof in java is also known as type comparison operator because it compares the instance with type. It returns either true or false. If we apply the instanceof operator with any variable that has null value, it returns false.

```java
class Simple {  
  public static void main(String args[]) {  
    Simple s=new Simple();  
    System.out.println(s instanceof Simple); //true  
  }  
} 
```

### Output:
```
true
```

## Downcasting with java instanceof operator

```java
class Animal { 

}  
  
class Dog extends Animal {  
  static void method(Animal a) {  
      if(a instanceof Dog) {  
         Dog d = (Dog) a; //downcasting  
         System.out.println("ok downcasting performed");  
      }  
  }  
   
  public static void main (String [] args) {  
      Animal a = new Dog();  
      Dog.method(a);  
  }  
    
}  
```

### Output:
```
ok downcasting performed
```

## Downcasting without the use of java instanceof

```java
class Animal { 

}  

class Dog extends Animal {  
    static void method(Animal a) {  
       Dog d = (Dog)a; //downcasting  
       System.out.println("ok downcasting performed");  
    }  
    
   public static void main (String [] args) {  
      Animal a = new Dog();  
      Dog.method(a);  
    }  
}  
```

### Output:
```
ok downcasting performed
```

Let's take closer look at this, actual object that is referred by a, is an object of Dog class. So if we downcast it, it is fine. But what will happen if we write:

```java
Animal a = new Animal();  
Dog.method(a);  
//Now ClassCastException throws  
```
