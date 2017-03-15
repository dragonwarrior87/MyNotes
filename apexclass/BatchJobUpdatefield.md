## Simple Batch to update a field with some value.
```java
global class updateAccountFields implements DataBase.Batchable<sObject>{
     global final String query;
     global final String field;
     global final String value;
     global final String Entity;
     
     global updateAccountFields(String q,String e,String f,String v){
         query = q;
         field = f;
         value = v;
         entity = e;
     }
     global Database.QueryLocator start(Database.BatchableContext bc){
         return Database.getQueryLocator(query);
     }   
     global void execute(Database.BatchableContext bc,List<sObject> sObj){
         for(Sobject s : sObj){
             s.put(field,value);
         }
         update sObj;
     }
     global void finish(Database.BatchableContext bc){
     }
}```
