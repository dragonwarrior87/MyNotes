## Simple example to understand Access modifiers through functions
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
public class Subclass extends AbstractBaseClass 
{
     protected override void protectedMethod() 
     {
        System.debug('In subclass protected method');
     }
}
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
