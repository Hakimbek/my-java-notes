# Java List
List in Java provides the facility to maintain the ordered collection. It contains the index-based methods to insert, update, delete and search the elements. It can have the duplicate elements also. We can also store the null elements in the list.

The List interface is found in the java.util package and inherits the Collection interface. It is a factory of ListIterator interface. Through the ListIterator, we can iterate the list in forward and backward directions. The implementation classes of List interface are ArrayList, LinkedList, Stack and Vector. The ArrayList and LinkedList are widely used in Java programming. The Vector class is deprecated since Java 5.

# Java ArrayList
Java ArrayList class uses a dynamic array for storing the elements. It is like an array, but there is no size limit. We can add or remove elements anytime. So, it is much more flexible than the traditional array.

The important points about Java ArrayList class are:
- Java ArrayList class can contain duplicate elements.
- Java ArrayList class maintains insertion order.
- Java ArrayList class is non synchronized.
- Java ArrayList allows random access because array works at the index basis.
- In ArrayList, manipulation is little bit slower than the LinkedList in Java because a lot of shifting needs to occur if any element is removed from the array list.

## Constructors of ArrayList
| Constructor |	Description |
| ----------- | ----------- |
| ArrayList() |	It is used to build an empty array list. |
| ArrayList(Collection<? extends E> c) |	It is used to build an array list that is initialized with the elements of the collection c. |
| ArrayList(int capacity) |	It is used to build an array list that has the specified initial capacity. |

# Java Non-generic Vs. Generic Collection
Java collection framework was non-generic before JDK 1.5. Since 1.5, it is generic.

Java new generic collection allows you to have only one type of object in a collection. Now it is type safe so typecasting is not required at runtime.

# Java LinkedList class
Java LinkedList class uses a doubly linked list to store the elements. It provides a linked-list data structure. It inherits the AbstractList class and implements List and Deque interfaces.

The important points about Java LinkedList are:

- Java LinkedList class can contain duplicate elements.
- Java LinkedList class maintains insertion order.
- Java LinkedList class is non synchronized.
- In Java LinkedList class, manipulation is fast because no shifting needs to occur.
- Java LinkedList class can be used as a list, stack or queue.

## Doubly Linked List
In the case of a doubly linked list, we can add or remove elements from both sides.

## Constructors of Java LinkedList
| Constructor |	Description |
| ----------- | ----------- |
| LinkedList() |	It is used to construct an empty list. |
| LinkedList(Collection<? extends E> c) |	It is used to construct a list containing the elements of the specified collection, in the order, they are returned by the collection's iterator. |

# Difference between ArrayList and LinkedList

| ArrayList |	LinkedList |
| --------- | ---------- |
| ArrayList internally uses a dynamic array to store the elements. |	LinkedList internally uses a doubly linked list to store the elements. |
| Manipulation with ArrayList is slow because it internally uses an array. If any element is removed from the array, all the bits are shifted in memory. |	Manipulation with LinkedList is faster than ArrayList because it uses a doubly linked list, so no bit shifting is required in memory. |
| An ArrayList class can act as a list only because it implements List only. |	LinkedList class can act as a list and queue both because it implements List and Deque interfaces. |
| ArrayList is better for storing and accessing data. |	LinkedList is better for manipulating data. |
