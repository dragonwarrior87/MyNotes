#Enum
  >Enum is a special class that define set of Constans.
  >Enum constans are implicitly public, Static and Final.
```java
public enum Season {WINTER, SPRING, SUMMER, FALL}
//Enum constants are implicilty Final and Static
Season e = Season.WINTER;
//disply the output of e as WINTER
    system.debug(e);
	system.debug('The name of the Enum item is'+Season.WINTER.name());
	system.debug('The value of the Enum item is'+Season.WINTER.ordinal());
//Values() -- It Rerutns an array Containing all of the values of enum type in the order they are declared.
	for(season ss:season.values()){
//system.debug('Enum values are :'+ss);
    system.debug('The Name of the Enum Item is :'+ss.name());
    system.debug('The Position of the Enum Item is :'+ss.ordinal());
}

```
