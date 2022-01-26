# Java Arrays
Java array is an object which contains elements of a similar data type. Additionally, The elements of an array are stored in a contiguous memory location. It is a data structure where we store similar elements. We can store only a fixed set of elements in a Java array.

Array in Java is index-based, the first element of the array is stored at the 0th index, 2nd element is stored on 1st index and so on.

Unlike C/C++, we can get the length of the array using the length member. In C/C++, we need to use the sizeof operator.

In Java, array is an object of a dynamically generated class. Java array inherits the Object class, and implements the Serializable as well as Cloneable interfaces. We can store primitive values or objects in an array in Java. Like C/C++, we can also create single dimentional or multidimentional arrays in Java.

## Advantages
### Code Optimization
  - It makes the code optimized, we can retrieve or sort the data efficiently.
### Random access
  - We can get any data located at an index position.

## Disadvantages
### Size Limit
  - We can store only the fixed size of elements in the array. It doesn't grow its size at runtime. To solve this problem, collection framework is used in Java which grows automatically.

# Types of Array in java

## Single Dimensional Array

### Syntax to Declare an Array in Java

```java
dataType[] arr; (or)  
dataType []arr; (or)  
dataType arr[];  
```

### Instantiation of an Array in Java

```java
arrayRefVar = new datatype[size];  
```

### Passing Array to a Method in Java
  - We can pass the java array to method so that we can reuse the same logic on any array.

### Anonymous Array in Java
  - Java supports the feature of an anonymous array, so you don't need to declare the array while passing an array to the method.

### Returning Array from the Method
  - We can also return an array from the method in Java.

### ArrayIndexOutOfBoundsException
  - The Java Virtual Machine (JVM) throws an ArrayIndexOutOfBoundsException if length of the array in negative, equal to the array size or greater than the array size while traversing the array.

# Multidimensional Array
In such case, data is stored in row and column based index (also known as matrix form).

### Syntax to Declare Multidimensional Array in Java

```java
dataType[][] arrayRefVar; (or)  
dataType [][]arrayRefVar; (or)  
dataType arrayRefVar[][]; (or)  
dataType []arrayRefVar[];   
```

### Example to instantiate Multidimensional Array in Java

```java
int[][] arr = new int[3][3]; //3 row and 3 column  
```

## Jagged Array in Java
If we are creating odd number of columns in a 2D array, it is known as a jagged array. In other words, it is an array of arrays with different number of columns.
