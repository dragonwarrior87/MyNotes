# Globle Class for using Static Variables and Methods

``` java
public class globle_cls { 
    
    public globle_cls(){
            inst_cnt=0;
        }
     //    public static list<string> event = new list<string>();
    public static string[] event = new string[]{};
    public static integer count=0;
    public integer inst_cnt;
 
    public static void limt_methd(){
    
       system.debug('No Of DML Statements: '+Limits.getDMLStatements());
       system.debug('No Of Query Rows: '+Limits.getQueryRows());
       system.debug('No Of DML Rows: '+Limits.getDMLRows());
       system.debug('No Of SOQL Statements: '+Limits.getQueries());
        
    }
     
  }
   
   ```
   
   # Basic Trigger Code
   
   ``` java
   trigger T_basic_prc on Account(before insert,after insert,before update,after update,before delete,after delete,after undelete) {

system.debug('Trigger started');
    
        if(trigger.isbefore){
        system.debug('ISBEFORE trigger testing');
         if(trigger.isinsert){
        system.debug('ISINSERT trigger testing');
         globle_cls.limt_methd();
}
         if(trigger.isupdate){
        system.debug('ISUPDATE trigger testing');
        globle_cls.limt_methd();
         }
         if(trigger.isdelete){
        system.debug('ISDELETE trigger testing');
        globle_cls.limt_methd();
        }

 }
    
    if(trigger.isafter){
        system.debug('ISAFTER trigger testing');
        if(trigger.isinsert){
        globle_cls.limt_methd();
        }
        if(trigger.isupdate){
        system.debug('ISUPDATE trigger testing');
       globle_cls.limt_methd();
        }
        if(trigger.isdelete){
        system.debug('ISDELETE trigger testing');
       globle_cls.limt_methd();
        }
        if(trigger.isUNdelete){
        system.debug('AFTER UNISDELETE trigger testing');
       globle_cls.limt_methd();
    }
  }  
    
}

```
# Execution of Trigger code
``` java
account[] al= new account[]{};
for(integer i=0; i < 100;i++){
    
    account a = new account(name='acct_tgr'+i, site='Trg_site');
    
    al.add(a);
}

insert al;

```


