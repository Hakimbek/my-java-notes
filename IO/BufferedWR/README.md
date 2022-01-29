# Java BufferedWriter Class
Java BufferedWriter class is used to provide buffering for Writer instances. It makes the performance fast. It inherits Writer
class. The buffering characters are used for providing the efficient writing of single arrays, characters, and strings.

## Class constructors
| Constructor |	Description |
| ----------- | ----------- |
| BufferedWriter(Writer wrt) |	It is used to create a buffered character output stream that uses the default size for an output buffer. |
| BufferedWriter(Writer wrt, int size) |	It is used to create a buffered character output stream that uses the specified size for an output buffer. |

## Class methods
| Method |	Description |
| void newLine() |	It is used to add a new line by writing a line separator. |
| void write(int c) |	It is used to write a single character. |
| void write(char[] cbuf, int off, int len) |	It is used to write a portion of an array of characters. |
| void write(String s, int off, int len) |	It is used to write a portion of a string. |
| void flush() |	It is used to flushes the input stream. |
| void close() |	It is used to closes the input stream |

```java
public class BufferedWriterExample {  
    public static void main(String[] args) throws Exception {     
      FileWriter writer = new FileWriter("D:\\testout.txt");  
      BufferedWriter buffer = new BufferedWriter(writer);  
      buffer.write("Welcome to javaTpoint.");  
      buffer.close();  
      System.out.println("Success");  
    }  
}  
```

# Java BufferedReader Class
Java BufferedReader class is used to read the text from a character-based input stream. It can be used to read data line by line by readLine() method. It makes the performance fast. It inherits Reader class.

## Java BufferedReader class constructors
| Constructor |	Description |
| ----------- | ----------- |
| BufferedReader(Reader rd) |	It is used to create a buffered character input stream that uses the default size for an input buffer. |
| BufferedReader(Reader rd, int size) |	It is used to create a buffered character input stream that uses the specified size for an input buffer. |

## Java BufferedReader class methods
| Method |	Description |
| ------ | ----------- |
| int read() |	It is used for reading a single character. |
| int read(char[] cbuf, int off, int len) |	It is used for reading characters into a portion of an array. |
| boolean markSupported() |	It is used to test the input stream support for the mark and reset method. |
| String readLine() |	It is used for reading a line of text. |
| boolean ready() |	It is used to test whether the input stream is ready to be read. |
| long skip(long n) |	It is used for skipping the characters. |
| void reset() |	It repositions the stream at a position the mark method was last called on this input stream. |
| void mark(int readAheadLimit) |	It is used for marking the present position in a stream. |
| void close() |	It closes the input stream and releases any of the system resources associated with the stream. |

```java
public class BufferedReaderExample {    
   public static void main(String args[]) throws Exception {             
      InputStreamReader r = new InputStreamReader(System.in);    
      BufferedReader br = new BufferedReader(r);           
      String name= "";    
      while(!name.equals("stop")){    
         System.out.println("Enter data: ");    
         name = br.readLine();    
         System.out.println("data is: " + name);    
      }              
      br.close();    
      r.close();    
   }    
}  
```
