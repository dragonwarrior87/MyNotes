### Enum class
```Java
public enum quarters 
{
    Q1,Q2,Q3,Q4
}
```

* Apex class to populate enum values based on the date field from custom object
```Java
public class displayQtr
{
    public void qtr(List<Vehicle__c> a)
    { 
        for (Vehicle__c ve: a)
        {
        if(ve.Service_Date__c.month()==1||ve.Service_Date__c.month()==2||ve.Service_Date__c.month()==3)
        ve.Vehicle_Model__c=quarters.Q1.name();
        
        if(ve.Service_Date__c.month()==4||ve.Service_Date__c.month()==5||ve.Service_Date__c.month()==6)
        ve.Vehicle_Model__c=quarters.Q2.name();

        if(ve.Service_Date__c.month()==7||ve.Service_Date__c.month()==8||ve.Service_Date__c.month()==9)
        ve.Vehicle_Model__c=quarters.Q3.name();

        if(ve.Service_Date__c.month()==10||ve.Service_Date__c.month()==11||ve.Service_Date__c.month()==12)
        ve.Vehicle_Model__c=quarters.Q4.name();
       }
   }
}
```

* Object trigger

```Java
trigger populatequarter on Vehicle__c(Before Insert)
{
    displayQtr q=new displayQtr();
    q.qtr(Trigger.New);
}
```

* End result will update the quarter name in the field "Vehicle_Model__c"
