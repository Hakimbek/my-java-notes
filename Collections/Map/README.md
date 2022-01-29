# Java Map Interface
A map contains values on the basis of key, i.e. key and value pair. Each key and value pair is known as an entry. A Map contains unique keys.

A Map doesn't allow duplicate keys, but you can have duplicate values. HashMap and LinkedHashMap allow null keys and values, but TreeMap doesn't allow any null key or value.
A Map can't be traversed, so you need to convert it into Set using keySet() or entrySet() method.

# Map.Entry Interface
Entry is the subinterface of Map. So we will be accessed it by Map.Entry name. It returns a collection-view of the map, whose elements are of this class. It provides methods to get key and value.

# Java HashMap
Java HashMap class implements the Map interface which allows us to store key and value pair, where keys should be unique. If you try to insert the duplicate key, it will replace the element of the corresponding key. It is easy to perform operations using the key index like updation, deletion, etc. HashMap class is found in the java.util package.

## Points to remember
- Java HashMap contains values based on the key.
- Java HashMap contains only unique keys.
- Java HashMap may have one null key and multiple null values.
- Java HashMap is non synchronized.
- Java HashMap maintains no order.
- The initial default capacity of Java HashMap class is 16 with a load factor of 0.75.

# Java LinkedHashMap class
Java LinkedHashMap class is Hashtable and Linked list implementation of the Map interface, with predictable iteration order. It inherits HashMap class and implements the Map interface.

## Points to remember
- Java LinkedHashMap contains values based on the key.
- Java LinkedHashMap contains unique elements.
- Java LinkedHashMap may have one null key and multiple null values.
- Java LinkedHashMap is non synchronized.
- Java LinkedHashMap maintains insertion order.
- The initial default capacity of Java HashMap class is 16 with a load factor of 0.75.

# Java TreeMap class
Java TreeMap class is a red-black tree based implementation. It provides an efficient means of storing key-value pairs in sorted order.

The important points about Java TreeMap class are:

- Java TreeMap contains values based on the key. It implements the NavigableMap interface and extends AbstractMap class.
- Java TreeMap contains only unique elements.
- Java TreeMap cannot have a null key but can have multiple null values.
- Java TreeMap is non synchronized.
- Java TreeMap maintains ascending order.

# What is difference between HashMap and TreeMap?
| HashMap |	TreeMap |
| ------- | ------- |
| HashMap can contain one null key. |	TreeMap cannot contain any null key. |
| HashMap maintains no order. |	TreeMap maintains ascending order. |

# Java Hashtable class
Java Hashtable class implements a hashtable, which maps keys to values. It inherits Dictionary class and implements the Map interface.

## Points to remember
- A Hashtable is an array of a list. Each list is known as a bucket. The position of the bucket is identified by calling the hashcode() method. A Hashtable contains values based on the key.
- Java Hashtable class contains unique elements.
- Java Hashtable class doesn't allow null key or value.
- Java Hashtable class is synchronized.
- The initial default capacity of Hashtable class is 11 whereas loadFactor is 0.75.

# Difference between HashMap and Hashtable

| HashMap |	Hashtable |
| ------- | --------- |
| HashMap is non synchronized. It is not-thread safe and can't be shared between many threads without proper synchronization code. |	Hashtable is synchronized. It is thread-safe and can be shared with many threads. |
| HashMap allows one null key and multiple null values. |	Hashtable doesn't allow any null key or value. |
| HashMap is a new class introduced in JDK 1.2. |	Hashtable is a legacy class. |
| HashMap is fast. |	Hashtable is slow. |
| We can make the HashMap as synchronized by calling this code Map m = Collections.synchronizedMap(hashMap); |	Hashtable is internally synchronized and can't be unsynchronized. |
| HashMap is traversed by Iterator. |	Hashtable is traversed by Enumerator and Iterator. |
| Iterator in HashMap is fail-fast. |	Enumerator in Hashtable is not fail-fast. |
8) HashMap inherits AbstractMap class.	Hashtable inherits Dictionary class.
