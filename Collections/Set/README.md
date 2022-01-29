# Java HashSet
Java HashSet class is used to create a collection that uses a hash table for storage. It inherits the AbstractSet class and implements Set interface.

The important points about Java HashSet class are:

- HashSet stores the elements by using a mechanism called hashing.
- HashSet contains unique elements only.
- HashSet allows null value.
- HashSet class is non synchronized.
- HashSet doesn't maintain the insertion order. Here, elements are inserted on the basis of their hashcode.
- HashSet is the best approach for search operations.
- The initial default capacity of HashSet is 16, and the load factor is 0.75.

## Difference between List and Set
A list can contain duplicate elements whereas Set contains unique elements only.

## Constructors of Java HashSet class

| Constructor |	Description |
| ----------- | ----------- |
|	HashSet() |	It is used to construct a default HashSet. |
|	HashSet(int capacity) |	It is used to initialize the capacity of the hash set to the given integer value capacity. The capacity grows automatically as elements are added to the HashSet. |
|	HashSet(int capacity, float loadFactor) |	It is used to initialize the capacity of the hash set to the given integer value capacity and the specified load factor. |
|	HashSet(Collection<? extends E> c) |	It is used to initialize the hash set by using the elements of the collection c. |

# Java LinkedHashSet class
ava LinkedHashSet class is a Hashtable and Linked list implementation of the set interface. It inherits HashSet class and implements Set interface.

The important points about Java LinkedHashSet class are:

- Java LinkedHashSet class contains unique elements only like HashSet.
- Java LinkedHashSet class provides all optional set operation and permits null elements.
- Java LinkedHashSet class is non synchronized.
- Java LinkedHashSet class maintains insertion order.

## Constructors of Java LinkedHashSet class

| Constructor |	Description |
| ----------- | ----------- |
| HashSet() |	It is used to construct a default HashSet. |
| HashSet(Collection c) |	It is used to initialize the hash set by using the elements of the collection c. |
| LinkedHashSet(int capacity) |	It is used initialize the capacity of the linked hash set to the given integer value capacity. |
| LinkedHashSet(int capacity, float fillRatio) |	It is used to initialize both the capacity and the fill ratio (also called load capacity) of the hash set from its argument. |

# Java TreeSet class
Java TreeSet class implements the Set interface that uses a tree for storage. It inherits AbstractSet class and implements the NavigableSet interface. The objects of the TreeSet class are stored in ascending order.

The important points about Java TreeSet class are:

- Java TreeSet class contains unique elements only like HashSet.
- Java TreeSet class access and retrieval times are quiet fast.
- Java TreeSet class doesn't allow null element.
- Java TreeSet class is non synchronized.
- Java TreeSet class maintains ascending order.

## Constructors of Java TreeSet class

| Constructor |	Description |
| ----------- | ----------- |
| TreeSet() |	It is used to construct an empty tree set that will be sorted in ascending order according to the natural order of the tree set. |
| TreeSet(Collection<? extends E> c) |	It is used to build a new tree set that contains the elements of the collection c. |
| TreeSet(Comparator<? super E> comparator) |	It is used to construct an empty tree set that will be sorted according to given comparator. |
| TreeSet(SortedSet<E> s) |	It is used to build a TreeSet that contains the elements of the given SortedSet. |
