# Inheritance

**What is the purpose of ‘this’ keyword in java?**

In Java, ‘this’ keyword refers to current instance of the object. It is useful for differentiating between instance variables and local variables. It can be used to call constructors. Or it can be used to refer to the instance. In case of method overriding, this is used for falling the method of current class.

**Explain the concept of Inheritance?**

Inheritance is an important concept in Object Oriented Programming. Some objects share certain characteristics and behavior. By using Inheritance, we can put the common behavior and characteristics in a base class which also known as super class. And then all the objects with common behavior inherit from this base class.

It is also represented by IS-A relationship.

Inheritance promotes, code reuse, method overriding and poly-morphism.


**Which class in Java is superclass of every other class?**

Java is an object-oriented programming language. In Java, Object class is the superclass of every other class.


**Why Java does not support multiple inheritance?**

Multiple Inheritance means that a class can inherit behavior from two or more parent classes.

The issue with Multiple Inheritance is that both the parent classes may have different implementation for the same method. So, they have different ways of doing the same thing. Now which implementation should the child class choose?

This leads to ambiguity in Multiple Inheritance. This is the main reason for Java not supporting Multiple Inheritance in implementation.

Let’s say you have a class TV and another class AtomBomb. Both have method switchOn() but only TV has switchOff() method. If your class inherits from both these classes then you have an issue that you can switchOn() both parents, but switchOff will only switchOff() TV.

But you can implement multiple interfaces in Java.

**In OOPS, what is meant by composition?**

Composition is also known as “has-a” relationship. In composition, “has-a” relation relates two classes. E.g. Class Car has a steering wheel.

If a class holds the instance of another class, then it is called composition.

**How aggregation and composition are different concepts?**

In OOPS, Aggregation and Composition are the types of association relations. A composition is a strong relationship. If the composite object is destroyed, then all its parts are destroyed. E.g. A Car has a Steering Wheel. If Car object is destroyed, then there is no meaning of Steering Wheel.

In Aggregation, the relationship is weaker than Composition.

E.g. A Library has students. If a Library is destroyed, Students still exist. So, Library and Student are related by Aggregation. A Library has Books. If Library is destroyed, the Books are also destroyed. Books of a Library cannot exist without the Library. So, Book and Library are related by Composition.


**Why there are no pointers in Java?**

In Java there are references instead of pointers. These references point to objects in memory. But there is no direct access to these memory locations. JVM is free to move the objects within VM memory.

The absence of pointers helps Java in managing memory and garbage collection effectively. Also, it provides developers with convenience of not getting worried about memory allocation and de-allocation.


**If there are no pointers in Java, then why do we get NullPointerException?**

In Java, the pointer equivalent is Object reference. When we use a it points to object reference. So JVM uses pointers but programmers only see object references.

In case an object reference points to null object, and we try to access a method or member variable on it, then we get NullPointerException.


**What is the purpose of ‘super’ keyword in java?**
super keyword is used in the methods or constructor of a child class. It refers to immediate parent class of an object.

By using super we can call a method of parent class from the method of a child class.

We can also call the constructor of a parent class from the constructor of a child class by using super keyword.


**Is it possible to use this () and super () both in same constructor?**

No, Java does not allow using both super () and this () in same constructor. As per Java specification, super () or this () must be the first statement in a constructor.

**What is the meaning of object cloning in Java?**

Object.clone() method is used for creating an exact copy of the object in Java. It acts like a copy constructor. It creates and returns a copy of the object, with the same class and with all the fields having same values as of the original object.

One disadvantage of cloning is that the return type is an Object. It has to be explicitly cast to actual type.
















