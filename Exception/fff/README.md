# Difference between final, finally and finalize

| # |	Key |	final |	finally |	finalize |
| - | --- | ----- | ------- | -------- |
| 1 |	Definition	| final is the keyword and access modifier which is used to apply restrictions on a class, method or variable. |	finally is the block in Java Exception Handling to execute the important code whether the exception occurs or not. |	finalize is the method in Java which is used to perform clean up processing just before object is garbage collected. |
| 2 |	Applicable to |	Final keyword is used with the classes, methods and variables. |	Finally block is always related to the try and catch block in exception handling. | finalize() method is used with the objects. |
| 3 |	Functionality |	Once declared, final variable becomes constant and cannot be modified. Final method cannot be overridden by sub class. Final class cannot be inherited. | finally block runs the important code even if exception occurs or not. Finally block cleans up all the resources used in try block |	finalize method performs the cleaning activities with respect to the object before its destruction. |
| 4 |	Execution |	Final method is executed only when we call it. |	Finally block is executed as soon as the try-catch block is executed. It's execution is not dependant on the exception. | finalize method is executed just before the object is destroyed. |
