# Java I/O Tutorial
Java I/O (Input and Output) is used to process the input and produce the output.

Java uses the concept of a stream to make I/O operation fast. The java.io package contains all the classes required for input and output operations.

We can perform file handling in Java by Java I/O API.

# Stream
A stream is a sequence of data. In Java, a stream is composed of bytes. It's called a stream because it is like a stream of water that continues to flow.

In Java, 3 streams are created for us automatically. All these streams are attached with the console.

1. System.out: standard output stream 
2. System.in: standard input stream
3. System.err: standard error stream

# OutputStream
Java application uses an output stream to write data to a destination; it may be a file, an array, peripheral device or socket.

## Useful methods of OutputStream
| Method |	Description |
| ------ | ------------ |
| public void write(int) throws IOException |	is used to write a byte to the current output stream. |
| public void write(byte[]) throws IOException |	is used to write an array of byte to the current output stream. |
| public void flush() throws IOException |	flushes the current output stream. |
| public void close() throws IOException |	is used to close the current output stream. |

![Output](/IO/image/2.png)


# InputStream
Java application uses an input stream to read data from a source; it may be a file, an array, peripheral device or socket.

## Useful methods of InputStream
| Method | Description |
| ------ | ------------ |
| public abstract int read() throws IOException |	reads the next byte of data from the input stream. It returns -1 at the end of the file. |
| public int available() throws IOException |	returns an estimate of the number of bytes that can be read from the current input stream. |
| public void close() throws IOException |	is used to close the current input stream. |

![Intput](/IO/image/1.png)
