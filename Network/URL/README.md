# Java URL
The Java URL class represents an URL. URL is an acronym for Uniform Resource Locator. It points to a resource on the World Wide Web. For example:

```
https://www.javatpoint.com/java-tutorial  
```

A URL contains many information:

## Protocol
In this case, http is the protocol.

## Server name or IP Address
In this case, www.javatpoint.com is the server name.

## Port Number
It is an optional attribute. If we write http//ww.javatpoint.com:80/sonoojaiswal/ , 80 is the port number. If port number is not mentioned in the URL, it returns -1.

## File Name or directory name
In this case, index.jsp is the file name.

# Constructors of Java URL class

## URL(String spec)
Creates an instance of a URL from the String representation.

## URL(String protocol, String host, int port, String file)
Creates an instance of a URL from the given protocol, host, port number, and file.

## URL(String protocol, String host, int port, String file, URLStreamHandler handler)
Creates an instance of a URL from the given protocol, host, port number, file, and handler.

## URL(String protocol, String host, String file)
Creates an instance of a URL from the given protocol name, host name, and file name.

## URL(URL context, String spec)
Creates an instance of a URL by parsing the given spec within a specified context.

## URL(URL context, String spec, URLStreamHandler handler)
Creates an instance of a URL by parsing the given spec with the specified handler within a given context.

# Commonly used methods of Java URL class
