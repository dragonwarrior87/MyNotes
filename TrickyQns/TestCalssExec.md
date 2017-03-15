## Find the debugs that will be getting after running below testclass
### Trigger:
```jave
trigger TestClassExecution on Patient__c (after insert,after update,after delete,after undelete) {
    System.debug('####after insert,after update,after delete,after undelete'+'trigger.old'+trigger.old == null);
    System.debug('####after insert,after update,after delete,after undelete'+'trigger.oldMAp'+trigger.old == null);
 }
}
```
### Test Class
```Java
@isTest public Class TestExecuteTests {
    static TestMethod void TestAllEvents(){
        Test.startTest();
        List<NameOfNameSpace__Patient__c> pList = new List<NameOfNameSpace__Patient__c>();
        pList.add(new NameOfNameSpace__Patient__c(Name = 'TestPatient',NameOfNameSpace__RelatedField__c = 'a0A2800000N5zwt'));
        insert pList;
        update pList;
        delete pList;
        unDelete pList;
        Test.stopTest();

    }
}
```
