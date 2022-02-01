# Data Types in Java

Data types specify the different sizes and values that can be stored in the variable. There are two types of data types in Java:

# Primitive data types
 The primitive data types include **boolean, char, byte, short, int, long, float** and **double**.

| Data Type |	Default Value |	Default size | Range(inclusive) | 
| --------- | ------------- | ------------ | ----- |
| boolean |	false |	1 bit |  |
| char |	'\u0000' |	2 byte | '\u0000' (or 0) to '\uffff' (or 65,535) |
| byte |	0 |	1 byte | -128 to 127 |
| short |	0 |	2 byte | -32,768 to 32,767 |
| int |	0 |	4 byte | 2,147,483,648 (-2^31) to 2,147,483,647 (2^31 - 1) |
| long |	0L |	8 byte | -9,223,372,036,854,775,808 (-2^63) to 9,223,372,036,854,775,807 (2^63 - 1) |
| float |	0.0f |	4 byte |
| double |	0.0d |	8 byte |

## Unicode System
Unicode is a universal international standard character encoding that is capable of representing most of the world's written languages.

## Why java uses Unicode System?
Before Unicode, there were many language standards:
- ASCII (American Standard Code for Information Interchange) for the United States.
- ISO 8859-1 for Western European Language.
- KOI-8 for Russian.
- GB18030 and BIG-5 for chinese, and so on.

### Problem
This caused two problems:
1. A particular code value corresponds to different letters in the various language standards.
2. The encodings for languages with large character sets have variable length.Some common characters are encoded as single bytes, other require two or more byte.

### Solution
To solve these problems, a new language standard was developed i.e. Unicode System. In unicode, character holds 2 byte, so java also uses 2 byte for characters.

The Boolean data type specifies one bit of information, but its "size" can't be defined precisely.

## 2. Non-primitive data types
The non-primitive data types include **Classes, Interfaces**, and **Arrays**.
