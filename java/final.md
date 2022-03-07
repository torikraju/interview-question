#Final

` `**How can you change the value of a final variable in Java?**

Java does not allow changing the value of a final variable. Once the value is set, it cannot be changed.



**Can a class be marked final in Java?**

Yes, a class can be marked final in Java. Once a class is marked final, it cannot be extended.



**How can we create a final method in Java?**

To mark a method, add modifier final to that method. A final method cannot be overridden by a child class.



**How can we prohibit inheritance in Java?**

If you mark a class final, it cannot be extended. This will prohibit the inheritance of that class in Java.

**Why Integer class in final in Java?**

Integer class is a wrapper for int. If it is not marked final, then any other class can extend it and modify the behavior of Integer operations. To avoid this Integer wrapper class is marked as final.



**What is a blank final variable in Java?**

When we declare a final variable without giving any initial value, then it is called blank final variable.



**How can we initialize a blank final variable?**

A blank final instance variable can be initialized in a constructor. A blank final static variable can be initialized in the static block of class.



**Is it allowed to declare main method as final?**

Yes, we can mark the main method as final.
