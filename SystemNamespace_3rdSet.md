#### JSON Class

Contains methods for serializing Apex objects into JSON format and deserializing JSON content that was serialized using the serialize method in this class.
Namespace:System

Usage:
Use the methods in the System.JSON class to perform round-trip JSON serialization and deserialization of Apex objects.

#### JSONGenerator Class

methods used to serialize objects into JSON content using the standard JSON encoding.
Namespace:System

Usage:
The System.JSONGenerator class is provided to enable the generation of standard JSON-encoded content and gives you more control on the structure of the JSON output.

#### JSONParser Class
Represents a parser for JSON-encoded content.
Namespace:System

Usage:
Use the System.JSONParser methods to parse a response that's returned from a call to an external service that is in JSON format, such as a JSON-encoded response of a Web service callout.

#### JSONToken Enum
Contains all token values used for parsing JSON content.
Namespace
System

Enum Value	Description
END_ARRAY --> The ending of an array value. This token is returned when ']' is encountered.
END_OBJECT	--> The ending of an object value. This token is returned when '}' is encountered.
FIELD_NAME	--> A string token that is a field name.
NOT_AVAILABLE	--> The requested token isn't available.
START_ARRAY	--> The start of an array value. This token is returned when '[' is encountered.
START_OBJECT	--> The start of an object value. This token is returned when '{' is encountered.
VALUE_EMBEDDED_OBJECT	--> An embedded object that isn't accessible as a typical object structure that includes the start and end object tokens START_OBJECT and END_OBJECT but is represented as a raw object.
VALUE_FALSE	--> The literal “false” value.
VALUE_NULL	--> The literal “null” value.
VALUE_NUMBER_FLOAT	--> A float value.
VALUE_NUMBER_INT	--> An integer value.
VALUE_STRING	--> A string value.
VALUE_TRUE	--> A value that corresponds to the “true” string literal.
