# Usage of Java this keyword
There can be a lot of usage of Java this keyword. In Java, this is a reference variable that refers to the current object.

## 1. this can be used to refer current class instance variable.

```java
class Student {  
  int id;  
  String name;  
  float fee;  

  Student(int id, String name, float fee) {  
    this.id = id;  
    this.name = name;  
    this.fee = fee;  
  }
  
  void display() {
    System.out.println(id + " " + name + " " + fee);
  }  
}

class TestThis {  
  public static void main(String args[]){  
    Student s1 = new Student(111,"hakim",5000f);  
    Student s2 = new Student(112,"arif",6000f);  
    s1.display();  
    s2.display();  
  }
}  
```

### Output:
```
111 hakim 5000.0
112 arif 6000.0
```

## 2. this can be used to invoke current class method (implicitly)

```java
class A {  
  void m(){
    System.out.println("hello m");
  }
  
  void n(){  
    System.out.println("hello n");  
    this.m();  
  }  
}  

class TestThis {  
  public static void main(String args[]) {  
    A a = new A();  
    a.n();  
  }
}  
```

### Output:
```
hello n
hello m
```

## 3. this() can be used to invoke current class constructor.

```java
class A {  
  A() {
    System.out.println("hello a");
  }  
  
  A(int x) {  
    this();  
    System.out.println(x);  
  }  
}

class TestThis {  
  public static void main(String args[]) {  
    A a = new A(10);  
  }
}  
```

### Output:
```
hello a
10
```
## Rule
  - Call to this() must be the first statement in constructor.

## 4. this can be passed as an argument in the method call.

```java
class S {  
  void m(S obj) {  
    System.out.println("method is invoked");  
  } 
  
  void p() {  
    m(this);  
  } 
  
  public static void main(String args[]) {  
    S s1 = new S();  
    s1.p();  
  }  
}  
```

### Output:
```
method is invoked
```

## 5. this can be passed as argument in the constructor call.

```java
class B {  
  A obj;  
  
  B(A obj) {  
    this.obj = obj;  
  }  
  
  void display() {  
    System.out.println(obj.data); //using data member of A class  
  }  
}  
  
class A {  
  int data = 10;  
  
  A() {  
    B b = new B(this);  
    b.display();  
  } 
  
  public static void main(String args[]) {  
    A a = new A();  
  }  
}  
```

### Output:
```
10
```

## 6. this can be used to return the current class instance from the method.

```java
class A {  
  A getA() {  
    return this;  
  }
  
  void msg(){
    System.out.println("Hello java");
  }  
} 

class Test {  
  public static void main(String args[]) {  
    new A().getA().msg();  
  }  
}  
```

### Output:
```
Hello java
```
