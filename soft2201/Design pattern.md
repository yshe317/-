
A pattern is a description of a problem and its solution
# 1. Behavioural Design Pattern

## Strategy Pattern
- Define a family of algorithms, encapsulate each one, and make them interchangeable
- Let the algorithm vary independently from clients that use it 
#### Applicability
- Many related classes differ only in their behavior 
- You  need  di fferent  vari ant  of   an  al gori thm 
- An algorithm uses data that should be hidden from its clients 
- A class defines many behaviors that appear as multiple statements in its operations 
#### Structure
![[Pasted image 20201128180230.png]]
#### Participants
![[Pasted image 20201128180300.png]]
#### Advantage
- Family of related algorithms (behaviors) for context to reuse 
- Alternative to sub-classing 
- Strategies eliminate conditional statements
- Provide choice of different implementation of the same behavior  

#### Disadvantage
- Clients must be aware of different strategies  
- Communicate overhead between Strategy and Context 
- Increased number of objects in an application 


## State
- Allow an object to change its behaviour when its internal state changes
- The object will appear to change its class when the state changes
#### Application
- Any time you need to change behaviours dynamically, i.e., the state of an object drives its behavior and change its behavior dynamically at run-time
- There are multi-part checks of an object’s state to determine its behaviour, i.e., operations have large, multipart conditional statements that depend on the object’s state

#### Structure
![[Pasted image 20201128182122.png]]
#### Participant
![[Pasted image 20201128182142.png]]
#### Advantage
- Removes case or if/else statements depending on state, and replaces them with function calls; makes the state transitions explicit; permits states to be shared
- Localizes state-specific behaviour for different states
- It makes state transition explicit
- State objects can be shared
#### Disadvantage
- Does require that all the states have to have their own objects


## Observer
week9
Define a one-to-many dependency between objects so that when one object changes state, all its dependentsare notified and updated automatically
#### Applicability
- An abstraction has two aspects, one dependent on the other
- A change to one object requires changing others, and it’s not clear how many objects need to be changed 
- An object should be able to notify other objects without making assumptions about who these objects are
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
- Abstract the instantiation process
- Make a system independent of how its objects are created, composed and represented
- Provides flexibility in what gets created, who creates it, how it gets created and when
## Factory Method 
#### Applicability
- a class cannnot anticipate the class objects it must create
- A class wants its subclass to specify the objects it creates.
- Classes responsibility to one of several helper subclasses, and you want to localize the knowledge of which helper subclass is the delegate 
#### Structure
![[Pasted image 20201128174305.png]]
#### Participants
![[Pasted image 20201128174323.png]]

#### Advantage
Flexibility: subclasses get a hook*for providing an extension to an object; connects parallel class hierarchies 
#### Disadvantage
Can require subclassing just to get an implementation 



## Builder
Separate the construction of a complex object from its representation so that the same construction process can create different representations
#### Applicability
- The algorithm for creating a complex object should be independent of the parts that make up the object and how they're assembled
- The construction process must allow different representations for the object that's constructed
#### Structure
![[Pasted image 20201128175016.png]]

#### Participants
![[Pasted image 20201128175025.png]]

#### advantage
- Gives flexibility that can be extended by implementing new subclasses of the Builder, and isolates code of construction from implementation
- Varying product's inter nal representation 
	- do to change the product's internal representation is define a new kind of builder
- Isolation of code construction and representation 
	- Each ConcreteBuilder contains all the code to create and assemble a particular kind of product. 
	- Different Directors can reuse it to build Product variants from the same set of parts
- Finer control over the construction process 
#### disadvantage
Not completely generic, less useful in situations where variety of implementations is not high 



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
#### Applicability 
- To use an existing class with an interface does not match the one you need
- You want to create a reusabe class that cooperates with unrelated  or unforeseen classes, i.e., classes that don't necessarily have compatible interfaces
- (Object adapter only)Adapt an existing interface, which has several existing implementations.
#### structure
![[Pasted image 20201126114235.png]]
#### participants
![[Pasted image 20201126114258.png]]
#### Advantage
![[Pasted image 20201126125432.png]]
#### Disadvantage
![[Pasted image 20201126125438.png]]

#### Class Adapter
Relies on class inheritance to achieve adapter
![[Pasted image 20201126130314.png]]

#### Object Adapter
Relies on object composition to achieve adapter
![[Pasted image 20201126130340.png]]