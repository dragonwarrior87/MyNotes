
- [OOPS concepts](#OOPsConcept)
- [Constructors](#Consturctors)
- [Types of Classes](#ClassTypes)
- [Access Modifiers](#Access Modifiers)

### Consturctors
	The special method which instantiates the class.

* No return type associated with this
* Shares same name as class
* Constructor can be parameterised or blank
	+ The constructor can be overloded based on the parameter type
		```java
		public constructor(integer a) {}

		public constructor(string b) {}
		```
	+ The constructor can be overloaded based on the Number of parameters
		```java
		public constructor(integer a, string b){}
		
		public constructor(integer a){}
		```
### ClassTypes
	* VIRTUAL
	* ABSTRACT

### Access Modifiers
	* private
		+ default Access  modifier
		+ can only be used within the inner class
	* protected 
		+ variables/methods marked as protected can be shared among class via inheritence
	* public
		+ These variables and methods will be available within namespace
	* global
		+ These are available for the external application (which are driven by SOAP/REST api)
