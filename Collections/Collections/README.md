# Java Collections class
Java collection class is used exclusively with static methods that operate on or return collections. It inherits Object class.

```java
public class CollectionsExample {  
    public static void main(String a[]) {      
        List<String> list = new ArrayList<String>();  
        list.add("C");  
        list.add("Core Java");  
        list.add("Advance Java");  
        
        System.out.println("Initial collection value:" + list);  
        Collections.addAll(list, "Servlet", "JSP");  
        System.out.println("After adding elements collection value:" + list);  
        String[] strArr = {"C#", ".Net"};  
        Collections.addAll(list, strArr);  
        System.out.println("After adding array collection value:" + list);  
    }  
}  
```
### Output:
```
Initial collection value:[C, Core Java, Advance Java]
After adding elements collection value:[C, Core Java, Advance Java, Servlet, JSP]
After adding array collection value:[C, Core Java, Advance Java, Servlet, JSP, C#, .Net]
```

# Sorting in Collection
We can sort the elements of:

- String objects
- Wrapper class objects
- User-defined class objects

Collections class provides static methods for sorting the elements of a collection. If collection elements are of a Set type, we can use TreeSet. However, we cannot sort the elements of List. Collections class provides methods for sorting the elements of List type elements.

## Method of Collections class for sorting List elements
 - public void sort(List list): is used to sort the elements of List. List elements must be of the Comparable type.

## Note
String class and Wrapper classes implement the Comparable interface. So if you store the objects of string or wrapper classes, it will be Comparable.

### Example to sort string objects
```java
class TestSort {  
  public static void main(String args[]) {  
  
     ArrayList<String> al = new ArrayList<String>();  
     al.add("Viru");  
     al.add("Saurav");  
     al.add("Mukesh");  
     al.add("Tahir");  
  
     Collections.sort(al);  
     Iterator itr = al.iterator();  
     while(itr.hasNext()) {  
       System.out.println(itr.next());  
     }  
  } 
}  
```

### Example to sort string objects in reverse order
```java
Collections.sort(al,Collections.reverseOrder());  
```

## Example to sort user-defined class objects

```java
class Student implements Comparable<Student> {  
    public String name;  
  
    public Student(String name) {  
      this.name = name;  
    } 
    
    public int compareTo(Student person) {  
      return name.compareTo(person.name);  
    }   
}  

public class TestSort {  
  public static void main(String[] args) {  
      ArrayList<Student> al = new ArrayList<Student>();  
      al.add(new Student("Viru"));  
      al.add(new Student("Saurav"));  
      al.add(new Student("Mukesh"));  
      al.add(new Student("Tahir"));  
      
      Collections.sort(al);  
      for (Student s : al) {  
         System.out.println(s.name);  
      }  
  }  
}  
```

### Output:
```
Mukesh
Saurav
Tahir
Viru
```

# Java Comparable interface
Java Comparable interface is used to order the objects of the user-defined class. This interface is found in java.lang package and contains only one method named compareTo(Object). It provides a single sorting sequence only, i.e., you can sort the elements on the basis of single data member only. For example, it may be rollno, name, age or anything else.

## compareTo(Object obj) method
### public int compareTo(Object obj)
  - It is used to compare the current object with the specified object. It returns

- positive integer, if the current object is greater than the specified object.
- negative integer, if the current object is less than the specified object.
- zero, if the current object is equal to the specified object.

## Java Comparable Example
```java
class Student implements Comparable<Student> {  
  int rollno;  
  String name;  
  int age;  
  
  Student(int rollno,String name,int age) {  
    this.rollno=rollno;  
    this.name=name;  
    this.age=age;  
  }  
  
  public int compareTo(Student st) {  
  if(age == st.age)  
     return 0;  
  else if(age > st.age)  
     return 1;  
  else {  
     return -1;  
  }  
}  
```

## Java Comparable Example: reverse order
```java
public int compareTo(Student st) {    
   if(age == st.age)    
      return 0;    
   else if(age < st.age)    
      return 1;    
   else {    
      return -1;    
   }    
}    
```

# Java Comparator interface
Java Comparator interface is used to order the objects of a user-defined class.

This interface is found in java.util package and contains 2 methods compare(Object obj1,Object obj2) and equals(Object element).

It provides multiple sorting sequences, i.e., you can sort the elements on the basis of any data member, for example, rollno, name, age or anything else.

## Java Comparator Example (Generic)

### Student.java
```java
class Student {  
  int rollno;  
  String name;  
  int age;  
  
  Student(int rollno, String name, int age) {  
    this.rollno=rollno;  
    this.name=name;  
    this.age=age;  
  }  
}  
```

### AgeComparator.java
```java
class AgeComparator implements Comparator<Student> {  
   public int compare(Student s1, Student s2) {  
   if(s1.age == s2.age)  
      return 0;  
   else if(s1.age > s2.age)  
      return 1;  
   else {  
      return -1;  
   }  
}  
```

```java
class Simple{  
  public static void main(String args[]) {  
    ArrayList<Student> al = new ArrayList<Student>();  
    al.add(new Student(101, "Vijay", 23));  
    al.add(new Student(106, "Ajay", 27));  
    al.add(new Student(105, "Jai", 21));  

     System.out.println("Sorting by age");  
  
     Collections.sort(al, new AgeComparator());  
     for(Student st: al) {  
        System.out.println(st.rollno + " " + st.name + " " + st.age);  
     }  
   }  
}  
```

# Another example
```java
public class Main {
    public static void main(String[] args) {
        ArrayList<Student> students = new ArrayList<>(Arrays.asList(
                new Student("Hakim", 22, 5),
                new Student("Ali", 10, 5),
                new Student("Orif", 50, 4),
                new Student("Kamol", 1, 7),
                new Student("Karim", 5, 1),
                new Student("Bilol", 15, 6),
                new Student("Ibrohim", 3, 5),
                new Student("Mariam", 22, 2),
                new Student("Bekzod", 13, 1)
        ));

        Collections.sort(students, new NameComparator().thenComparing(new AgeComparator()));

        students.forEach(System.out::println);
    }
}
```
