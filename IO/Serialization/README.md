# Serialization and Deserialization in Java
Serialization in Java is a mechanism of writing the state of an object into a byte-stream. It is mainly used in Hibernate, RMI, JPA, EJB and JMS technologies.

The reverse operation of serialization is called deserialization where byte-stream is converted into an object. The serialization and deserialization process is platform-independent, it means you can serialize an object on one platform and deserialize it on a different platform.

For serializing the object, we call the writeObject() method of ObjectOutputStream class, and for deserialization we call the readObject() method of ObjectInputStream class.

## java.io.Serializable interface
Serializable is a marker interface (has no data member and method). It is used to "mark" Java classes so that the objects of these classes may get a certain capability. The Cloneable and Remote are also marker interfaces.

The Serializable interface must be implemented by the class whose object needs to be persisted.

The String class and all the wrapper classes implement the java.io.Serializable interface by default.

# ObjectOutputStream class
The ObjectOutputStream class is used to write primitive data types, and Java objects to an OutputStream. Only objects that support the java.io.Serializable interface can be written to streams.

## Constructor

| Constructor | Description |
| ----------- | ----------- |
| public ObjectOutputStream(OutputStream out) throws IOException {} |	It creates an ObjectOutputStream that writes to the specified OutputStream. |

## Important Methods

| Method |	Description |
| ------ | ----------- |
| public final void writeObject(Object obj) throws IOException {} |	It writes the specified object to the ObjectOutputStream. |
| public void flush() throws IOException {} |	It flushes the current output stream. |
| public void close() throws IOException {} |	It closes the current output stream. |

# ObjectInputStream class
An ObjectInputStream deserializes objects and primitive data written using an ObjectOutputStream.

## Constructor

| Constructor | Description |
| ----------- | ----------- |
| public ObjectInputStream(InputStream in) throws IOException {} |	It creates an ObjectInputStream that reads from the specified InputStream. |

## Important Methods

| Method |	Description |
| ------ | ----------- |
| public final Object readObject() throws IOException, ClassNotFoundException{} |	It reads an object from the input stream. |
| public void close() | throws IOException {}	It closes ObjectInputStream. |

## Note
All the objects within an object must be Serializable.

# Java transient Keyword
During the serialization, when we do not want an object to be serialized we can use a transient keyword.
