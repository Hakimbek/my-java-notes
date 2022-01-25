# Static Binding and Dynamic Binding
Connecting a method call to the method body is known as binding.

There are two types of binding

## 1. Static Binding (also known as Early Binding).
When type of the object is determined at compiled time(by the compiler), it is known as static binding.

If there is any *private, final* or *static* method in a class, there is static binding.

```java
class Dog {  
    private void eat(){
        System.out.println("dog is eating...");
    }  
  
    public static void main(String args[]) {  
        Dog d = new Dog();  
        d.eat();  
    }  
}  
```

## 3. Dynamic Binding (also known as Late Binding).
When type of the object is determined at run-time, it is known as dynamic binding.

```java
class Animal {  
    void eat(){
        System.out.println("animal is eating...");
    }  
}  
  
class Dog extends Animal {  
    void eat(){
        System.out.println("dog is eating...");
    }  
  
    public static void main(String args[]) {  
        Animal a = new Dog();  
        a.eat();  
    }  
}  
```

### Output:
```
dog is eating...
```
