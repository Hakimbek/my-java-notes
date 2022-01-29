# Java HttpURLConnection class
The Java HttpURLConnection class is http specific URLConnection. It works for HTTP protocol only. By the help of HttpURLConnection class, you can retrieve information of any HTTP URL such as header information, status code, response code etc.

### The java.net.HttpURLConnection is subclass of URLConnection class.

# HttpURLConnection Class Constructor

| Constructor |	Description |
| ----------- | ----------- |
| protected HttpURLConnection(URL u) |	It constructs the instance of HttpURLConnection class. |

# Java HttpURLConnection Methods

| Method |	Description |
| ------ | ----------- |
| void disconnect() |	It shows that other requests from the server are unlikely in the near future. |
| InputStream getErrorStream() |	It returns the error stream if the connection failed but the server sent useful data. |
| Static boolean getFollowRedirects() |	It returns a boolean value to check whether or not HTTP redirects should be automatically followed. |
| String getHeaderField(int n) |	It returns the value of nth header file. |
| long getHeaderFieldDate(String name, long Default) |	It returns the value of the named field parsed as a date. |
| String getHeaderFieldKey(int n) |	It returns the key for the nth header file. |
| boolean getInstanceFollowRedirects() |	It returns the value of HttpURLConnection's instance FollowRedirects field. |
| Permission getPermission() |	It returns the SocketPermission object representing the permission to connect to the destination host and port. |
| String getRequestMethod() |	It gets the request method. |
| int getResponseCode() |	It gets the response code from an HTTP response message. |
| String getResponseMessage() |	It gets the response message sent along with the response code from a server. |
| void setChunkedStreamingMode(int chunklen) |	The method is used to enable streaming of a HTTP request body without internal buffering, when the content length is not known in advance. |
| void setFixedLengthStreamingMode(int contentlength) |	The method is used to enable streaming of a HTTP request body without internal buffering, when the content length is known in advance. |
| void setFixedLengthStreamingMode(long contentlength) |	The method is used to enable streaming of a HTTP request body without internal buffering, when the content length is not known in advance. |
| static void setFollowRedirects(boolean set) |	It sets whether HTTP redirects (requests with response code) should be automatically followed by HttpURLConnection class. |
| void setInstanceFollowRedirects(boolean followRedirects) |	It sets whether HTTP redirects (requests with response code) should be automatically followed by instance of HttpURLConnection class. |
| void setRequestMethod(String method) |	Sets the method for the URL request, one of: GET POST HEAD OPTIONS PUT DELETE TRACE are legal, subject to protocol restrictions. |
| abstract boolean usingProxy() |	It shows if the connection is going through a proxy. |

```java
public class HttpURLConnectionDemo {    
  public static void main(String[] args) {    
    try {    
      URL url = new URL("http://www.javatpoint.com/java-tutorial");    
      HttpURLConnection huc = (HttpURLConnection) url.openConnection();  
      for(int i = 1; i <= 8; i++) {  
         System.out.println(huc.getHeaderFieldKey(i) + " = " + huc.getHeaderField(i));  
      }  
      huc.disconnect();   
    } catch(Exception e) { 
      System.out.println(e);
    }    
  }    
}    
```
