# Java StringBuffer Class
Java StringBuffer class is used to create mutable (modifiable) String objects. The StringBuffer class in Java is the same as String class except it is mutable i.e. it can be changed.

## Note
Java StringBuffer class is thread-safe i.e. multiple threads cannot access it simultaneously. So it is safe and will result in an order.

## Important Constructors of StringBuffer Class

| Constructor |	Description |
| ----------- | ----------- |
| StringBuffer() |	It creates an empty String buffer with the initial capacity of 16. |
| StringBuffer(String str) |	It creates a String buffer with the specified string.. |
| StringBuffer(int capacity) |	It creates an empty String buffer with the specified capacity as length. |

## Important methods of StringBuffer class

| Modifier and Type |	Method	Description |
| ----------------- | ------------------ |
| public synchronized StringBuffer	append(String s) |	It is used to append the specified string with this string. The append() method is overloaded like append(char), append(boolean), append(int), append(float), append(double) etc. |
| public synchronized StringBuffer	insert(int offset, String s) |	It is used to insert the specified string with this string at the specified position. The insert() method is overloaded like insert(int, char), insert(int, boolean), insert(int, int), insert(int, float), insert(int, double) etc. |
| public synchronized StringBuffer	replace(int startIndex, int endIndex, String str) |	It is used to replace the string from specified startIndex and endIndex. |
| public synchronized StringBuffer	delete(int startIndex, int endIndex) |	It is used to delete the string from specified startIndex and endIndex. |
| public synchronized StringBuffer	reverse() |	is used to reverse the string. |
| public int	capacity() |	It is used to return the current capacity. |
| public void	ensureCapacity(int minimumCapacity) |	It is used to ensure the capacity at least equal to the given minimum. |
| public char	charAt(int index) |	It is used to return the character at the specified position. |
| public int	length() |	It is used to return the length of the string i.e. total number of characters. |
| public String	substring(int beginIndex) |	It is used to return the substring from the specified beginIndex. |
| public String	substring(int beginIndex, int endIndex) |	It is used to return the substring from the specified beginIndex and endIndex. |

## What is a mutable String?
A String that can be modified or changed is known as mutable String. StringBuffer and StringBuilder classes are used for creating mutable strings.

# Java StringBuilder Class
Java StringBuilder class is used to create mutable (modifiable) String. The Java StringBuilder class is same as StringBuffer class except that it is non-synchronized. It is available since JDK 1.5.

## Important Constructors of StringBuilder class

| Constructor |	Description |
| ----------- | ----------- |
| StringBuilder() |	It creates an empty String Builder with the initial capacity of 16. |
| StringBuilder(String str) |	It creates a String Builder with the specified string. |
| StringBuilder(int length) |	It creates an empty String Builder with the specified capacity as length. |

## Important methods of StringBuilder class

| Method |	Description |
| ------ | ----------- |
| public StringBuilder append(String s) |	It is used to append the specified string with this string. The append() method is overloaded like append(char), append(boolean), append(int), append(float), append(double) etc. |
| public StringBuilder insert(int offset, String s) |	It is used to insert the specified string with this string at the specified position. The insert() method is overloaded like insert(int, char), insert(int, boolean), insert(int, int), insert(int, float), insert(int, double) etc. |
| public StringBuilder replace(int startIndex, int endIndex, String str) |	It is used to replace the string from specified startIndex and endIndex. |
| public StringBuilder delete(int startIndex, int endIndex) |	It is used to delete the string from specified startIndex and endIndex. |
| public StringBuilder reverse() |	It is used to reverse the string. |
| public int capacity() |	It is used to return the current capacity. |
| public void ensureCapacity(int minimumCapacity) |	It is used to ensure the capacity at least equal to the given minimum. |
| public char charAt(int index) |	It is used to return the character at the specified position. |
| public int length() |	It is used to return the length of the string i.e. total number of characters. |
| public String substring(int beginIndex) |	It is used to return the substring from the specified beginIndex. |
| public String substring(int beginIndex, int endIndex) |	It is used to return the substring from the specified beginIndex and endIndex. |

# Difference between String and StringBuffer

| No. |	String | StringBuffer |
| --- | ------ | ------------ |
| 1 |	The String class is immutable. | The StringBuffer class is mutable. |
| 2 |	String is slow and consumes more memory when we concatenate too many strings because every time it creates new instance. | StringBuffer is fast and consumes less memory when we concatenate strings. |
| 3 |	String class overrides the equals() method of Object class. So you can compare the contents of two strings by equals() method. | StringBuffer class doesn't override the equals() method of Object class. |
| 4 |	String class is slower while performing concatenation operation. | StringBuffer class is faster while performing concatenation operation. |
| 5 |	String class uses String constant pool. |	StringBuffer uses Heap memory |

# Difference between StringBuffer and StringBuilder

| No. |	StringBuffer | StringBuilder |
| --- | ------------ | ------------- |
| 1 |	StringBuffer is synchronized i.e. thread safe. It means two threads can't call the methods of StringBuffer simultaneously. | StringBuilder is non-synchronized i.e. not thread safe. It means two threads can call the methods of StringBuilder simultaneously. |
| 2 |	StringBuffer is less efficient than StringBuilder. | StringBuilder is more efficient than StringBuffer. |
| 3 |	StringBuffer was introduced in Java 1.0 |	StringBuilder was introduced in Java 1.5 |
