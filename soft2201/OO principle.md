# General Responsibility Assignment Software Pattern(GRASP)
### High cohesion
Where responsibility of the element share common characteristics (properties,methods, associations,
### Low Coupling
How an object type is connected to another type.  Consider the assignment ofresponsibilities and any unnecessary binding to other types.
### Controller
can represent two components of a system. 
1. Represents the overall system, a rootobject which represents a major subsystem. 
2. Represents a use case scenario within which thesystem operation occurs (a use-case or session controller).
### Information Expert Principle
Assign a responsibility to the information expert - the class that has theinformation necessary to fulfill the responsibility.

### Creator
 Responsibility of object creation.

### Polymorphism
When related alternatives or behaviour vary by type, assign responsibility forthe behaviour using polymorphic operations to the type for which the behaviour varies.

### Pure Fabrication
Assign a highly cohesive set of responsibilities to an artificial or conveniencebehaviour class (or type) that does not represent a problem concept-something made up,  inorder to support high cohesion, low coupling, and reuse.

### Indirection
Assign the responsibility to an intermediate object to mediate between other com-ponents or services, so that they are not directly coupled

### Protected Variation
 Identify points of predicted variation or instability; assign responsibilitiesto create a stable interface around them.

# SOLID
## Single Responsibility Principle(SRP)
Every class should have a single responsibility andthat responsibility should be entirely met by that class
## Open Close Principle(OCP)
Open for extension but closed for modification; inheritanceis used for this, e.g. through the use ofinherited abstract base classes;
## Liskov Substitution Principle(LSP)
If S<:T (“S is a subtype of T”) then a T objectcan be replaced with an S object and no harm done;
## Interface Segregation Principle(ISP)
Client code should not have to implement interfaces it doesn’t need;
## Dependency Inversion Principle(DIP)
High level, complex modules should not depend onlow-level, simple models —use abstraction, and implementation details should depend on abstractions, not the other way around.
