# Java File Class
The File class is an abstract representation of file and directory pathname. A pathname can be either absolute or relative.

## Constructors
| Constructor |	Description |
| ----------- | ----------- |
| File(File parent, String child) |	It creates a new File instance from a parent abstract pathname and a child pathname string. |
| File(String pathname) |	It creates a new File instance by converting the given pathname string into an abstract pathname. |
| File(String parent, String child) |	It creates a new File instance from a parent pathname string and a child pathname string. |
| File(URI uri) |	It creates a new File instance by converting the given file: URI into an abstract pathname. |

## Useful Methods
| Method |	Description |
| ------ | ----------- |
| static File	createTempFile(String prefix, String suffix) |	It creates an empty file in the default temporary-file directory, using the given prefix and suffix to generate its name. |
| boolean	createNewFile() |	It atomically creates a new, empty file named by this abstract pathname if and only if a file with this name does not yet exist. |
| boolean	canWrite() |	It tests whether the application can modify the file denoted by this abstract pathname.String[] |
| boolean	canExecute() |	It tests whether the application can execute the file denoted by this abstract pathname. |
| boolean	canRead() |	It tests whether the application can read the file denoted by this abstract pathname. |
| boolean	isAbsolute() |	It tests whether this abstract pathname is absolute. |
| boolean	isDirectory() |	It tests whether the file denoted by this abstract pathname is a directory. |
| boolean	isFile() |	It tests whether the file denoted by this abstract pathname is a normal file. |
| String	getName() |	It returns the name of the file or directory denoted by this abstract pathname. |
| String	getParent() |	It returns the pathname string of this abstract pathname's parent, or null if this pathname does not name a parent directory. |
| Path	toPath() |	It returns a java.nio.file.Path object constructed from the this abstract path. |
| URI	toURI() |	It constructs a file: URI that represents this abstract pathname. |
| File[]	listFiles() |	It returns an array of abstract pathnames denoting the files in the directory denoted by this abstract pathname |
| long	getFreeSpace() |	It returns the number of unallocated bytes in the partition named by this abstract path name. |
| String[]	list(FilenameFilter filter) |	It returns an array of strings naming the files and directories in the directory denoted by this abstract pathname that satisfy the specified filter. |
| boolean	mkdir() |	It creates the directory named by this abstract pathname. |

```java
public class FileDemo {  
    public static void main(String[] args) {  
  
        try {  
            File file = new File("javaFile123.txt");  
            if (file.createNewFile()) {  
                System.out.println("New File is created!");  
            } else {  
                System.out.println("File already exists.");  
            }  
        } catch (IOException e) {  
            e.printStackTrace();  
        }  
  
    }  
}  
```
