# Access Modifiers in Java
There are two types of modifiers in Java: access modifiers and non-access modifiers.

The access modifiers in Java specifies the accessibility or scope of a field, method, constructor, or class. We can change the access level of fields, constructors, methods, and class by applying the access modifier on it.

## There are four types of Java access modifiers:

## Private
The access level of a private modifier is only within the class. It cannot be accessed from outside the class.

### Role of Private Constructor
  - If you make any class constructor private, you cannot create the instance of that class from outside the class. 

### Note
  - A class cannot be private or protected except nested class.

## Default
The access level of a default modifier is only within the package. It cannot be accessed from outside the package. If you do not specify any access level, it will be the default.

It provides more accessibility than private. But, it is more restrictive than protected, and public.

## Protected
The protected access modifier is accessible within package and outside the package but through inheritance only.

The protected access modifier can be applied on the data member, method and constructor. It can't be applied on the class.

It provides more accessibility than the default modifer.

## Public
The public access modifier is accessible everywhere. It has the widest scope among all other modifiers.

## Understanding Java Access Modifiers

| Access Modifier |	Within class | Within package |	Outside package by subclass only | Outside package |
| --------------- | ------------ | -------------- | -------------------------------- | --------------- |
| Private |	Y	| N |	N |	N |
| Default |	Y |	Y |	N |	N |
| Protected |	Y |	Y |	Y |	N |
| Public | Y | Y | Y | Y |

## Java Access Modifiers with Method Overriding
If you are overriding any method, overridden method (i.e. declared in subclass) must not be more restrictive.

