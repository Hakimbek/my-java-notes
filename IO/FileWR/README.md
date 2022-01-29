# Java FileWriter Class
Java FileWriter class is used to write character-oriented data to a file. It is character-oriented class which is used for file handling in java.

Unlike FileOutputStream class, you don't need to convert string into byte array because it provides method to write string directly.

## Constructors of FileWriter class
| Constructor |	Description |
| ----------- | ----------- |
| FileWriter(String file) |	Creates a new file. It gets file name in string. |
| FileWriter(File file) |	Creates a new file. It gets file name in File object. |

## Methods of FileWriter class
| Method |	Description |
| ------ | ----------- |
| void write(String text) |	It is used to write the string into FileWriter. |
| void write(char c) |	It is used to write the char into FileWriter. |
| void write(char[] c) |	It is used to write char array into FileWriter. |
| void flush() |	It is used to flushes the data of FileWriter. |
| void close() |	It is used to close the FileWriter. |

```java
public class FileWriterExample {  
    public static void main(String args[]) {    
         try {    
           FileWriter fw = new FileWriter("D:\\testout.txt");    
           fw.write("Welcome to javaTpoint.");    
           fw.close();    
         } catch(Exception e) {
           System.out.println(e);
         }    
          System.out.println("Success...");    
     }    
}  
```

# Java FileReader Class
Java FileReader class is used to read data from the file. It returns data in byte format like FileInputStream class.

It is character-oriented class which is used for file handling in java.

## Constructors of FileReader class
| Constructor |	Description |
| ----------- | ----------- |
| FileReader(String file) | It gets filename in string. It opens the given file in read mode. If file doesn't exist, it throws FileNotFoundException. |
| FileReader(File file) |	It gets filename in file instance. It opens the given file in read mode. If file doesn't exist, it throws FileNotFoundException. |

## Methods of FileReader class
| Method |	Description |
| ------ | ----------- |
| int read() |	It is used to return a character in ASCII form. It returns -1 at the end of file. |
| void close() |	It is used to close the FileReader class. |

```java
public class FileReaderExample {  
    public static void main(String args[]) throws Exception {    
          FileReader fr = new FileReader("D:\\testout.txt");    
          int i;    
          while((i = fr.read()) != -1)    
            System.out.print((char)i);    
          fr.close();    
    }    
}    
```
