#### Address 
Can directly access the component fields of address compound fields.
Ex:
  ```java
  Address addr = myAccount.BillingAddress;
  String acctCity = addr.City;
  ```
 #### Answers 
 Answers is a feature of the Community application that enables users to ask questions and have community members post replies.
 Community members can then vote on the helpfulness of each reply, and the person who asked the question can mark one reply as 
 the best answer.
 #### ApexPages
 * Add and check for messages associated with the current page.
 * To reference the current page.
 ### Approval
 * Processing approval requests
 * Setting approval-process locks and unlocks on records using lock and unock methods and are treated as DML.
 ### Blob
 It is a primitive data type
* Pdf file can be created
* Can be converted to String
#### Boolean 
It is a primitive data type.
```java
valueOf(stringToBoolean)
//Converts the specified string to a Boolean value and returns true if the specified string value is true. Otherwise, returns false.
valueOf(fieldValue)
//Converts the specified object to a Boolean value. 
//Use this method to convert a history tracking field value or an object that represents a Boolean value.
```
#### BusinessHours 
To set the business hours at which your customer support team operates.
#### Cases
 To interact with case record.
#### Comparable Interface
Adds sorting support for Lists that contain non-primitive types, that is, Lists of user-defined types.
* Implement Comparable interface
* Define compareTo(Object compareTo) method

