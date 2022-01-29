# Java BufferedOutputStream Class
Java BufferedOutputStream class
is used for buffering an output stream. It internally uses buffer to store data. It adds more efficiency than to write data directly into a stream. So, it makes the performance fast.

## Java BufferedOutputStream class constructors
| Constructor |	Description |
| ----------- | ----------- |
| BufferedOutputStream(OutputStream os) |	It creates the new buffered output stream which is used for writing the data to the specified output stream. |
| BufferedOutputStream(OutputStream os, int size) |	It creates the new buffered output stream which is used for writing the data to the specified output stream with a specified buffer size. |

## Java BufferedOutputStream class methods
| Method |	Description |
| ------ | ----------- |
| void write(int b) |	It writes the specified byte to the buffered output stream. |
| void write(byte[] b, int off, int len) |	It write the bytes from the specified byte-input stream into a specified byte array, starting with the given offset |
| void flush() |	It flushes the buffered output stream. |

```java
public class BufferedOutputStreamExample {    
   public static void main(String args[])throws Exception {    
       FileOutputStream fout = new FileOutputStream("D:\\testout.txt");    
       BufferedOutputStream bout = new BufferedOutputStream(fout);    
       String s = "Welcome to javaTpoint.";    
       byte b[] = s.getBytes();    
       bout.write(b);    
       bout.flush();    
       bout.close();    
       fout.close();    
       System.out.println("success");    
   }    
}  
```

# Java BufferedInputStream Class
Java BufferedInputStream class is used to read information from stream. It internally uses buffer mechanism to make the performance fast.

The important points about BufferedInputStream are:
- When the bytes from the stream are skipped or read, the internal buffer automatically refilled from the contained input stream, many bytes at a time.
- When a BufferedInputStream is created, an internal buffer array is created.

## Java BufferedInputStream class constructors
| Constructor |	Description |
| ----------- | ----------- |
| BufferedInputStream(InputStream IS) |	It creates the BufferedInputStream and saves it argument, the input stream IS, for later use. |
| BufferedInputStream(InputStream IS, int size) |	It creates the BufferedInputStream with a specified buffer size and saves it argument, the input stream IS, for later use. |

## Java BufferedInputStream class methods
| Method |	Description |
| ------ | ----------- |
| int available() |	It returns an estimate number of bytes that can be read from the input stream without blocking by the next invocation method for the input stream. |
| int read() |	It read the next byte of data from the input stream. |
| int read(byte[] b, int off, int ln) |	It read the bytes from the specified byte-input stream into a specified byte array, starting with the given offset. |
| void close() |	It closes the input stream and releases any of the system resources associated with the stream. |
| void reset() |	It repositions the stream at a position the mark method was last called on this input stream. |
| void mark(int readlimit) |	It sees the general contract of the mark method for the input stream. |
| long skip(long x) |	It skips over and discards x bytes of data from the input stream. |
| boolean markSupported() |	It tests for the input stream to support the mark and reset methods. |

```java
public class BufferedInputStreamExample {    
   public static void main(String args[]) {    
     try {    
       FileInputStream fin = new FileInputStream("D:\\testout.txt");    
       BufferedInputStream bin = new BufferedInputStream(fin);    
       int i;    
       while((i = bin.read()) != -1) {    
          System.out.print((char) i);    
       }    
       bin.close();    
       fin.close();    
     } catch(Exception e) 
         System.out.println(e);
     }    
   }    
}  
```
