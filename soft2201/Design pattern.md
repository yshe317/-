
# 1. Behavioural Design Pattern
## Strategy Pattern

## State

## Observer
week9
Define a one-to-many dependency between objects so that when one object changes state, all its dependentsare notified and updated automatically
#### structure
![[Pasted image 20201126132720.png]]

#### participants
![[Pasted image 20201126132756.png]]

#### Advantage
![[Pasted image 20201126133457.png]]

#### disadvantage
![[Pasted image 20201126133756.png]]

## Memento Design Pattern
week10
Without violating encapsulation, capture and externalise an object's internal state so that the state can later be restored to this state
#### Structure
![[Pasted image 20201126104034.png]]
#### Participants
![[Pasted image 20201126104121.png]]
![[Pasted image 20201126104129.png]]
#### Advantage
![[Pasted image 20201126104411.png]]
#### Disadvantage
Might be expensive 
![[Pasted image 20201126104351.png]]
#### Usage
save and load

# 2. Creational Design Pattern

## Prototype
WEEK 10
Specify the kindsof objects to create using a prototype instance, and create new objects by copying this prototype 
#### participants
![[Pasted image 20201126105831.png]]
#### advantage
![[Pasted image 20201126110355.png]]
![[Pasted image 20201126110741.png]]
![[Pasted image 20201126111711.png]]
![[Pasted image 20201126111726.png]]
![[Pasted image 20201126111834.png]]
#### disadvantage
![[Pasted image 20201126110406.png]]

	


## Singleton
week11
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

- How classes and objects are composed to form larger structures
- Structural class patterns use inheritance to compose interfaces or implementations 
- Structural object patterns describe ways to compose objects to realise new functionality
## Façade Pattern
week11
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
week11
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


## Adapter
week9
Allow classes of incompatible interfaces to work together. Convert the interface of a class into another interface that clients expect.
#### structure
![[Pasted image 20201126114235.png]]
#### participants
![[Pasted image 20201126114258.png]]
#### Advantage
![[Pasted image 20201126125432.png]]
#### Disadvantage
![[Pasted image 20201126125438.png]]

####Class Adapter
Relies on class inheritance to achieve adapter
![[Pasted image 20201126130314.png]]

#### Object Adapter
Relies on object composition to achieve adapter
![[Pasted image 20201126130340.png]]