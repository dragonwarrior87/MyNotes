#Enum
  >Enum is a special class that define set of Constants.
  >Enum constants are implicitly public, Static and Final.
```java
public enum Season {WINTER, SPRING, SUMMER, FALL}
//Enum constants are implicilty Final and Static
Season e = Season.WINTER;
//disply the output of e as WINTER
    system.debug(e);
//Values() -- It Rerutns an array Containing all of the values of enum type in the order they are declared.
	for(season ss:season.values()){
//system.debug('Enum values are :'+ss);
    system.debug('The Name of the Enum Item is :'+ss.name());
    system.debug('The Position of the Enum Item is :'+ss.ordinal());
}

```
#Values() --This method returns the values of the Enum as a list of the same Enum type.
	Each Enum value has the following methods that take no arguments.

	Name() -- Returns the name of the Enum item as a String.
	Ordinal() -- Returns the position of the item, as an Integer, in the list of Enum values starting with zero.

#Example:
```java
	system.debug('The name of the Enum item is'+Season.WINTER.name());
	system.debug('The value of the Enum item is'+Season.WINTER.ordinal());
```
	
