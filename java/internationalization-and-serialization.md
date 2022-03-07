
# Internationalization



**What is Locale in Java?**

A Locale object represents a specific geographical, political, or cultural region. It is used to locale-sensitive operations in Java. It helps is following the local conventions of a country, native or region. These conventions can be for formatting the dates, money, numbers etc.



**How will you use a specific Locale in Java?**

To use a specific Locale, we need to load that Locale. We can use ResourceBundle.getBundle("Locale.UK") method to load a Locale.



# Serialization



**What is the serialization?**

Serialization is a process converting an object into a byte array. This byte array represents the class, version and internal state of the object. JVM can use this byte array to transmit/read the object over a network.

**What is the purpose of serialization?**

Some of the uses of serialization are:

- Communication: It is used for transmitting an object over network between two machines.
- Persistence: We can store the object’s state in a database and retrieve it from database later on.
- Caching: Serialization can be used for caching to improve performance. We may need 10 minutes to build an object, but it may take just 10 seconds to de-serialize the object.
- Cross JVM Synchronization: It can be used in same way across multiple JVM that follow different architecture.



**What is Deserialization?**

Deserialization is the process of reconstructing the object from the serialized state. It is the reverse process of serialization.



**What is Serialization and Deserialization conceptually?**

Serialization is to convert Object data into a stream of bytes

Deserialization is to convert a stream of bytes back into a copy of the original object.

**Why do we mark a data member transient?**

Member variables of an object are marked transient to indicate that they should not be serialized.

During serialization process the transient variables are not considered part of the persistent state of an object.



**Is it allowed to mark a method as transient?**

No, Java does not allow marking a method as transient. The transient keyword is valid only for member variables.



**How does marking a field as transient makes it possible to serialize an object?**

Let say we have a class ABC that implements Serializable interface, but it contains a member variable object of class XYZ that does not implement Serializable interface. Due to this it is not possible to Serialize the class ABC.

To solve this issue, we can mark the member variable XYZ as Transient in class ABC. This will allow us to serialize the class ABC.



**What is Externalizable interface in Java?**

Externalizable interface extends Serializable interface in Java. It is used for giving the Class control over saving and restoring the contents of its instances.

A class implements methods writeExternal() and readExternal() to store and restore the object.



**What is the difference between Serializable and Externalizable interface?**

Serializable is a marker interface but Externalizable is not a marker interface.

When we implement Serializable interface, the class is serialized automatically by default. We can override writeObject() and readObject()methods to control more complex object Serialization process.

In case of Externalizable, we use readExternal() and writeExternal() methods to give control to class for class's serialization process.

Serializable interface is based on recursive algorithm.

Serializable gives you two options. One option is to provide custom way of serialization, the other default way. In Externalizable, you have to always implement readExternal() and writeExternal() methods.

A public no-arg constructor is needed while using Externalizable interface.

In Serialization, we need to define serialVersionUID. If it is not explicitly defined it will be generated automatically based on all the fields, methods of the class.