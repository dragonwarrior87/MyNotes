# Delete Records from Recycle Bin using below Code
  > Run the below code in Execute Anonymus Block

```java
list<account> al=[select id from account where isDeleted =true limit 100 all Rows];
list<id> adl= new list<id>();
for(account a: al){
    adl.add(a.id);
}
system.debug(adl.size());
database.emptyRecycleBin(adl);
```
