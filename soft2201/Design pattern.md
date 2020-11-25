
# 1. Behavioural Design Pattern
## Strategy Pattern


## Memento Design Pattern


# 2. Creational Design Pattern
## Prototype




## Singleton
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





# Structural Design Patterns
## Façade Pattern
Provides a unified interface to a set of interfaces in a subsystem.Defines ahigher-level interface that simplifies subsystem use.

### Participants
![[Pasted image 20201125231240.png]]

##### Advantage
- Simplify the usage of an existing subsystem by defining your own interface
- Shields clients from subsystem components, reduce the number of objects that clients deal with and make the subsystem easier to use.
- Promote weak coupling between the subsystem and the clients

##### Disadvantage
- Does not prevent applications from using subsystem classes if they need to. Choice between ease of use and flexibility.


## Decorator
Attach additional responsibilities to an object dynamically(flexible alternative to subclassing for extending functionality) 
### Participants
![[Pasted image 20201125230101.png]]

##### Advantage
- More flexibility and less complexity than static inheritance 
- Avoids feature-laden (heavily loaded) classes high up in the hierarchy 

##### Disadvantage
- Decorator and its component are not identical 
- Many little objects 
![[Pasted image 20201125230807.png]]
