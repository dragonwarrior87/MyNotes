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
#### Approval
 * Processing approval requests
 * Setting approval-process locks and unlocks on records using lock and unock methods and are treated as DML.
#### Blob
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
#### Continuation
To make callouts asynchronously to a SOAP or REST Web service.
If the continuationMethod property is not set for a Continuation, the same action method that made the asynchronous callout is called again when the callout response returns.
#### Cookie 
Lets you access cookies for your Force.com site using Apex.
Use the setCookies method of the PageReference Class to attach cookies to a page.
#### Crypto 
Provides methods for creating digests, message authentication codes, and signatures, as well as encrypting and decrypting information.
The methods in the Crypto class can be used for securing content in Force.com, or for integrating with external services such as Google or Amazon WebServices (AWS).
* Encrypt and Decrypt Exceptions *
The following exceptions can be thrown for these methods:
decrypt
encrypt
decryptWithManagedIV
encryptWithManagedIV
#### Custom Settings
Custom settings are similar to custom objects and enable application developers to create custom sets of data, as well as create and associate custom data for an organization, profile, or specific user. All custom settings data is exposed in the application cache, which enables efficient access without the cost of repeated queries to the database. This data can then be used by formula fields, validation rules, flows, Apex, and the SOAP API.
* Hierarchy
* List
#### Database 
Contains methods for creating and manipulating data.
Some Database methods also exist as DML statements.
#### Date 
Contains methods for the Date primitive data typ.
```java
date myDate = date.newInstance(1990, 11, 21);
date newDate = myDate.addMonths(3);
date expectedDate = date.newInstance(1991, 2, 21);
system.assertEquals(expectedDate, newDate);
```
