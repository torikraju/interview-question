# Reflection

**What is Reflection in Java?**

Reflection is Java language's ability to inspect and dynamically call classes, methods, attributes etc. at Runtime. It helps in examining or modifying the Runtime behavior of a class at Runtime.



**What are the uses of Reflection in Java?**

Reflection is often used in Testing, Debugging and in Integrated Development Environment (IDE).

Reflection allows you to write programs that do not have to "know" everything at compile time. It makes programs more dynamic, since they can be tied together at runtime.

Many modern frameworks like Spring etc. use Reflection. Some modern languages like Python etc. also use Reflection.

JAVA API for XML Parsing (JAXP) also uses Reflection.



**How can we access private method of a class from outside the class?**

We can use Reflection to access private method of a class from outside the class. IN Java, we use getDeclaredMethod() to get instance of a private method. Then we mark this method accessible and finally invoke it.

In following sample code, we are accessing private method message() of class Foo by Reflection.

FileName: Foo.java


```java
public class Foo* {
	private void message () {
    	System.out.println("hello java");
	}
}
```

FileName: FooMethodCall.java
```java
import java.lang.reflect.Method
public class FooMethodCall{
	public static void main(String[] args)throws Exception {
		Class c = Class.forName("Foo");
		Object o= c.newInstance();
		Method m =c.getDeclaredMethod("message", null);
		m.setAccessible(true);
		m.invoke(o, null);
	}
}
```


**How can we create an Object dynamically at Runtime in Java?**

We can use Reflection to create an Object dynamically at Runtime in Java. We can use Class.newInstance() or Constructor.newInstance() methods for creating such Objects.