## Simple example to understand Access modifiers through functions

#### Class 1: Base class has protected method
```Java
public abstract class AbstractBaseClass 
{
     public void publicMethod() 
     {
        System.debug('Public method, calling protected method');
        protectedMethod();
        System.debug('Protected method call worked');
     }
    protected virtual void protectedMethod() 
    {
        System.debug('In base class protected method');
    }
}
```
#### Class 2: Derived class overriding the protected method
```java
public class Subclass extends AbstractBaseClass 
{
     protected override void protectedMethod() 
     {
        System.debug('In subclass protected method');
     }
}
```
#### Class 3: Another class for calling the above
```java
public class CallingClass 
{
     private Subclass instance = new Subclass();
     public CallingClass() 
     {
         instance.publicMethod();
     }
}
```
*Try this example to understand access modifiers*

#### Output:
* Public method, calling protected method
* In subclass protected method
* Protected method call worked

*When you disable the overriding you will get the below output*

* Public method, calling protected method
* In base class protected method
* Protected method call worked

