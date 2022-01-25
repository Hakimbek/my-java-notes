# Super Keyword in Java
The super keyword in Java is a reference variable which is used to refer immediate parent class object.

Whenever you create the instance of subclass, an instance of parent class is created implicitly which is referred by super reference variable.

# Usage of Java super Keyword

## 1. super can be used to refer immediate parent class instance variable.

```java
class Animal {  
    String color = "white";  
}

class Dog extends Animal {  
    String color = "black";  

    void printColor() {  
        System.out.println(color);  //prints color of Dog class  
        System.out.println(super.color);  //prints color of Animal class  
    }  
}  

class TestSuper {  
    public static void main(String args[]) {  
        Dog d = new Dog();  
        d.printColor();  
    }
}  
```

### Output:
```
black
white
```


## 2. super can be used to invoke immediate parent class method.

```java
class Animal {  
    void eat() {
        System.out.println("eating...");
    }  
}  

class Dog extends Animal {  
    void eat() {
        System.out.println("eating bread...");
    }
    
    void bark() {
        System.out.println("barking...");
    }
    
    void work(){  
        super.eat();  
        bark();  
    }  
}  

class TestSuper {  
    public static void main(String args[]) {  
        Dog d = new Dog();  
        d.work();  
    }
}  
```

### Output:
```
eating...
barking...
```

## 3. super() can be used to invoke immediate parent class constructor.

```java
class Animal {  
    Animal(){
        System.out.println("animal is created");
    }  
}  

class Dog extends Animal {  
    Dog() {  
        super();  
        System.out.println("dog is created");  
    }  
}  

class TestSuper {  
    public static void main(String args[]) {  
        Dog d = new Dog();  
    }
}  
```

### Output:
```
animal is created
dog is created
```

## Note
As we know well that default constructor is provided by compiler automatically if there is no constructor. But, it also adds *super()* as the first statement.

```java
class Animal {  
    Animal(){
        System.out.println("animal is created");
    }  
}  

class Dog extends Animal {  
    Dog() {  
        System.out.println("dog is created");  
    }  
}  

class TestSuper {  
    public static void main(String args[]) {  
        Dog d = new Dog();  
    }
}  
```

### Output:
```
animal is created
dog is created
```
