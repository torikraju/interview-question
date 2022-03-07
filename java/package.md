# Package

**What is the purpose of package in Java?**

A package is used to encapsulate a group of classes, interfaces and sub-packages. Often, it is a hierarchical structure of storing information. It is easier to organize the related classes and sub-packages in this manner. A Package also provides access protection for classes and interfaces. A package also helps in removing naming collision.



**What is java.lang package?**

In Java, java.lang package contains the classes that are fundamental to the design of Java programming language. The most important class in this package is Object class.

It also contains wrapper classes like- Integer, Boolean, Character etc. It provides Math class for mathematical operations.



**Which is the most important class in Java?**

It is an open-ended question with many answers. In my view, Object class is the most important class of Java programming language. It is the root of all the classes in Java. It provides some very important and fundamental methods.



**Is it mandatory to import java.lang package every time?**

No. By default, JVM loads it internally.



**Can you import same package or class twice in your class?**

If we import same package multiple times in a class, compiler includes it only once. So, neither JVM nor Compiler gives any error/warning on including a package multiple time. 

If you have two classes with same name, then you may get name collision on importing the class erroneously. JVM internally loads the class only one time.

**What is a static import in Java?**

Static import is similar to normal import declaration. Normal import allows us to import classes from packages without using package qualifier. Static import allows us to import static members from a class without using class qualifier.



**What is the difference between import static com.test.Fooclass and import com.test.Fooclass?**

First import is a static import and the second import is normal import of a class. First import allows us to import static members of class.