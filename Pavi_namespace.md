# Pattern class
* Used to represent the compiled representation of regular expression.
	
	* Example methods
	* Compile(RegExp), Matcher(RegExp),Matches(RegExp,I/P String) etc.,
	
	* Note that the following code example:
	  1. Pattern.matches(regExp, input);	
  * produces the same result as this code example:
	  1. Pattern.compile(regex);	
    2. Matcher(input).matches();	
  
# Queueable class
* Used to enable the aysnchronous execution of apex jobs that can be monitored.
	
* Lets see how this can be used
```Java
	Public class Myqueueclass implements Queueable
	{
		public void execute(QueueableContext context)
		{
		//Code
		}
	}
	
* To make the job to add in queue i.e to submit for asynchronous execution
	
	ID jobid=system.enqueueJob(new Myqueueclass());
	
* To query information about your submitted job, perform a SOQL query on AsyncApexJob by filtering on the job ID that the System.enqueueJob method returns. This example uses the jobID variable that was obtained in the previous example.

	AsyncApexJob jobInfo = [SELECT Status,NumberOfErrors FROM AsyncApexJob WHERE Id=:jobID];
```
