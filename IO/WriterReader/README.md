# Java Writer
It is an abstract class for writing to character streams. The methods that a subclass must implement are write(char[], int, int), flush(), and close(). Most subclasses will override some of the methods defined here to provide higher efficiency, functionality or both.

## Constructor
| Constructor |	Description |
| ----------- | ----------- |
| protected	Writer() |	It creates a new character-stream writer whose critical sections will synchronize on the writer itself. |
| protected	Writer(Object lock) |	It creates a new character-stream writer whose critical sections will synchronize on the given object |

## Methods
| Method |	Description |
| ------ | ----------- |
| Writer	append(char c) |	It appends the specified character to this writer. |
| Writer	append(CharSequence csq) |	It appends the specified character sequence to this writer |
| Writer	append(CharSequence csq, int start, int end) |	It appends a subsequence of the specified character sequence to this writer. |
| abstract void	close() |	It closes the stream, flushing it first. |
| abstract void	flush() |	It flushes the stream. |
| void	write(char[] cbuf) |	It writes an array of characters. |
| abstract void	write(char[] cbuf, int off, int len) |	It writes a portion of an array of characters. |
| void	write(int c) |	It writes a single character. |
| void	write(String str) |	It writes a string. |
| void	write(String str, int off, int len) |	It writes a portion of a string. |

```java
public class WriterExample {  
    public static void main(String[] args) {  
        try {  
            Writer w = new FileWriter("output.txt");  
            String content = "I love my country";  
            w.write(content);  
            w.close();  
            System.out.println("Done");  
        } catch (IOException e) {  
            e.printStackTrace();  
        }  
    }  
}  
```

# Java Reader
Java Reader is an abstract class for reading character streams. The only methods that a subclass must implement are read(char[], int, int) and close(). Most subclasses, however, will override some of the methods to provide higher efficiency, additional functionality, or both.

## Constructor
|	Constructor |	Description |
| ----------- | ----------- |
| protected	Reader() |	It creates a new character-stream reader whose critical sections will synchronize on the reader itself. |
| protected	Reader(Object lock) |	It creates a new character-stream reader whose critical sections will synchronize on the given object. |

## Methods
| Method |	Description |
| ------ | ----------- |
| abstract void	close() |	It closes the stream and releases any system resources associated with it. |
| void	mark(int readAheadLimit) |	It marks the present position in the stream. |
| boolean	markSupported() |	It tells whether this stream supports the mark() operation. |
| int	read() |	It reads a single character. |
| int	read(char[] cbuf) |	It reads characters into an array. |
| abstract int	read(char[] cbuf, int off, int len) |	It reads characters into a portion of an array. |
| int	read(CharBuffer target) |	It attempts to read characters into the specified character buffer. |
| boolean	ready() |	It tells whether this stream is ready to be read. |
| void	reset() |	It resets the stream. |
| long	skip(long n) |	It skips characters. |

```java
public class ReaderExample {  
    public static void main(String[] args) {  
        try {  
            Reader reader = new FileReader("file.txt");  
            int data = reader.read();  
            while (data != -1) {  
                System.out.print((char) data);  
                data = reader.read();  
            }  
            reader.close();  
        } catch (Exception ex) {  
            System.out.println(ex.getMessage());  
        }  
    }  
}  
```
