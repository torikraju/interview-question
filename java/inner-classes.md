


# Inner Classes


**What is a Nested class?**

In Java, a Nested class is a class declared inside another class. We can have more than one class declared inside a file.



**How many types of Nested classes are in Java?**

Java provides four types of Nested classes:

- Member inner class
- Local inner class
- Anonymous inner class
- Static nested class

**Why do we use Nested Classes?**

There are following reasons for using nested classes:

- Logical Grouping: We can logically group classes in one place. If one class is useful to only one other class, then we put smaller class within the larger class and keep them in one file. This kind of nesting "helper classes" in a top-level class makes the package more streamlined.
- Encapsulation: Nested classes increase encapsulation. Let say there are two top-level classes, Foo and Bar. Bar needs access to private members of Foo. We can hide class Bar within class Foo. In this way, private members of Foo can be accessed by class Bar. So, class Foo remains encapsulated. Also, class Bar remains hidden from the outside world.
- Code Clarity: Nested classed make the code more readable and well organized. Only Top-level classes are exposed. The helper classes are kept hidden and closer the code where it is used by a Top-level class.



**What is the difference between a Nested class and an Inner class in Java?**

An Inner class in Java is non-static class. It is a type of Nested class that is defined in another class but not qualified with a Static modifier. A Nested class is also a class can be Static Nested class or a non-Static Inner class.

An Inner class has access to other members of the enclosing class, even if they are declared private. A Static Nested class cannot access the other members of the enclosing class.



**What is a Nested interface?**

A Nested interface is declared inside another interface or a top-level class. By default, it is static.

A Nested interface is also known as Static interface.

**How can we access the non-final local variable, inside a Local Inner class?**

Java allows a Local Inner class to access only Constant local members. So, we have to make the non-final local variable as final constant to access it inside a Local Inner class.



**Can an Interface be defined in a Class?**

Yes, we can define a Static Nested interface within a class. Only the enclosing class can access it.



**Do we have to explicitly mark a Nested Interface public static?**

A Nested Interface is implicitly public static. So, the modifiers public and static are redundant in declaration.



**Why do we use Static Nested interface in Java?**

Only the enclosing class can access a Static Nested interface. Consider following code in which interface Xyz is enclosed in class Abc.
```java
public class Abc {
	public interface Xyz {
		void callback();
	}
	public static void registerCallback(Xyz xyz) {...}
}
Client Code Abc.registerCallback(new Abc.Xyz() {
public void callback() {...} });
```


Any code that cannot access Abc can not access interface Xyz also.

So, the purpose of declaring an Inner interface is to restrict its access from outside world.
