# Abstraction



**What is Abstraction in Object Oriented programming?**

Abstraction is the process of hiding certain implementation details of an object and showing only essential features of the object to outside world.

It is different from Abstract class in Java.

Abstraction process identifies commonalities and hides the complexity of implementation. It helps us in focusing on the interface that we share with the outside world.



**How is Abstraction different from Encapsulation?**

Abstraction happens at class level design. It results in hiding the implementation details. Encapsulation is also known as “Information Hiding”. An example of encapsulation is marking the member variables private and providing getter and setter for these member variables.



**What is an abstract class in Java?**

An abstract class in Java has one or more abstract methods. An abstract method is just declared in the abstract class, but it is not implemented.

An abstract class has to be extended in Java and its abstract methods have to be implemented by a child class. Also, Java does not allow new instance of Abstract class.



**Is it allowed to mark a method abstract method without marking the class abstract?**

No. Java specification says that if there is at least one abstract method in a class, the class has to be marked abstract.



**Is it allowed to mark a method abstract as well as final?**

No. It will be contradictory statement to mark a method abstract as well as final.

An abstract method has to be overridden by a child class. And a final method cannot be overridden. Therefore, a method can be either abstract or final in Java.



**Can we instantiate an abstract class in Java?**

No. We cannot create an instance of an abstract class in Java.

**What is an interface in Java?**

An Interface in Java is an abstract type blueprint of a class. It contains the methods that a class must implement. It is like a protocol.

It has method signatures and constant declarations.



**Is it allowed to mark an interface method as static?**

Yes, from Java 8 onwards, we can define static and default methods in an interface. Prior to Java 8, it was not allowed.



**Why an Interface cannot be marked as final in Java?**

A final method cannot be overridden. But an interface method has to be implemented by another class. So, the interface method cannot be marked as final.



**What is a marker interface?**

There are interfaces that do not have any data member or methods. These interfaces are called Marker interface. E.g. Serializable, Cloneable, Remote etc.



**What can we use instead of Marker interface?**

We can use annotations instead of Marker interface.



**How Annotations are better than Marker Interfaces?**

Annotations serve the purpose of conveying metadata about the class to its consumers without creating a separate type for it. Annotations are more powerful than a Marker interface. They allow programmers to pass more sophisticated information to classes that "consume" it.

**What is the difference between abstract class and interface in Java?**

Differences between Abstract class and Interface are as follows:

- An abstract class can have implemented methods with body (non-abstract methods). Interface has only abstract methods. From Java 8 onwards, interface can have static/default methods in implemented form.
- An abstract class can have instance member variables. An interface cannot have instance variables. It can only have constants.
- An abstract class can have a constructor. Interface cannot have constructor. It has to be implemented by another class.
- A class can extend only one abstract class. A class can implement more than one interface.



**Does Java allow us to use private and protected modifiers for variables in interfaces?**

No. All the variables in an interface are implicitly public.

**How can we cast to an object reference to an interface reference?**

An Object that implements an Interface can be cast to the same Interface. Since an Object implementing an Interface already provides implementation for the methods of that Interface, it is allowed to do so as per the rules of Inheritance.


