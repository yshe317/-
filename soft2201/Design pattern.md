# Strategy


# Singleton
Ensure a class only has one instance,and provide global point of access to it.

##### Applicability
There must be only one exactly instance of a class, client can access it from an access point.  For example, the whole system with using database.
The sole instance should be extensible by subclassing, and clients should be able to use an extended instance without modifying their code.  	

##### Advantage
![[Pasted image 20201125142454.png]]
1. There must be only one exactly instance of a class
2. You gain a global access point to that instance.
3. The singleton object is initialized only when it’s requested for the first time.
![[Pasted image 20201125142209.png]]
##### Disadvanture
![[Pasted image 20201125142624.png]]
##### Code
![[Pasted image 20201125143523.png]]
![[Pasted image 20201125143555.png]]
##### Link
https://www.cnblogs.com/damsoft/p/6105122.html



# Decorator
Attach additional responsibilities to an object dynamically(flexible alternative to subclassing for extending functionality) 


