# Polymorphism

**What is Runtime Polymorphism?**

Runtime Polymorphism or Dynamic Polymorphism is the polymorphism that exists at runtime. In case of method overriding it is not known which method will be called at runtime. Based on the type of object, JVM decides the exact method that should be called.

So, at compile time it is not known which method will be called at run time.



**Is it possible to achieve Runtime Polymorphism by data members in Java?**

No. We need to create Runtime Polymorphism by implementing methods at two levels of inheritance in Java.



**Explain the difference between static and dynamic binding?**

In Static binding references are resolved at compile time. In Dynamic binding references are resolved at Run time.

E.g.



```java 
Person p = **new** Person();
p.walk(); // Java compiler resolves this binding at compile time.
public void walkObject o){
	((Person) o).walk(); // this is dynamic binding.
}
```