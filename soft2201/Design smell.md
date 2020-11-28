## common design smells
### Missing abstraction
bunches of data or encoded strings are used instead of creating an abstraction
### Multifaceted abstraction
an abstraction has multiple responsibilities assigned to it
### Insufficient modularization
an abstraction has not been completely decomposed, and a further decomposition could reduce its size, implementation complexity, or both
### Cyclically-dependent modularization
two or more abstractions depend on each other directly or indirectly (creating tightly-coupling abstractions)
### Cyclic hierarchy
a super-type in a hierarchy depends on any of its subtypes

## Summary of Common Symptoms Design Smells

#### Rigidity(difficult to change)
the system is hard to change because every change forces many other changes to other parts of the system
#### Fragility(easy to break)
Changes cause the system to break in places that have no conceptual relationship to the part that was changed 
#### Immobility(difficult to reuse)
很难将系统分解为可在其他系统中重用的组件
It is hard to detangle the system into components that can be reused in other systems   
#### Viscosity(difficult to do the right thing)
![[Pasted image 20201128161834.png]]
#### Needless complexity(overdesign)
when design contains elements that are not useful. 
#### Needless Repetition(mouse abuse)
- Developers tend to find what they think relevant code, copy and paste and change it in their module
- Code appears over and over againin slightly different forms, developers are missing an abstraction 
- Bugs found in repeating modules have tobe fixed in every repetition 
#### Opacity(disorganized expression)
tendency of a module to be difficult to understand
- Code written in unclear and non-expressive way
- Code that evolves over time tends to become more and more opaque with age
- Developers need to put themselves in the reader’s shoes and make appropriate effort to refactor their code so that their readers can understand it 

follow the Design principle[[OO principle]]