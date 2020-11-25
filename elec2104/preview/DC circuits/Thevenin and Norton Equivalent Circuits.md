# Source Transformation(p135)
A source transformation is the process of replacing a voltage source Vs in series with a resistor R by a current source is in parallel with a resistor R or vice versa.

The two circuits below are equivalent if they have the same voltage-current characteristics ==at terminal ab==

![[Pasted image 35.png]]

Indeed, we could easily show that the two circuits are equivalent. If we turn off all the sources, then the input resistence at terminal a-b is equal to R, and if we short circuit the terminal a-b, then the current flowing through a-b is V/R. Hence, the two circuits are equivalent. 

# Thevenin's Theorem(p139)

## the Thevenin's theorem
There are cases where a particular element in a circuit is variable, while other elements are fixed.  If this variable component of the circuit is a linear two-terminal circuit(has two nodes that connect with the circuit externally), then it could be replaced by an equivalent circuit with a voltage source Vth in series with a resistor Rth.

## How to use Thevenin's theorem
since thevenin's theorem could replace a rather complicated circuit component into an equivalent circuit with a voltage source Vth and a resistor Rth, then the main objective is to find Vth and Rth. 

Analysis of thevenin Voltage and Resistence depends on if there are dependent sources in the circuit. 

### Case 1: no dependent sources
If there are no dependent sources, we turn off all the independent sources, and then Rth is the input resistence at a-b, and the value of Rth could be calculated using Ohm's law

![[Pasted image 33.png]]

### Case2: dependent sources
if there are dependent sources, then according to the superposition theorem, we could only turn off all the independent sources, as dependent sources are determined by certain circuit elements. 

We could choose to either apply a voltage or current source(could specify any value to them, or even an unspecified variable) and then determine the current or voltage respectively. After that, we could calculate Rth with Ohm's law. 

![[Pasted image 34.png]]

# Norton's Theorem(p145)

 Norton’s theorem states that a linear two-terminal circuit can be replaced by an equivalent circuit consisting of a current source IN in parallel with a resistor RN, where IN is the short-circuit current through the terminals and RN is the input or equivalent resistance at the termi- nals when the independent sources are turned off.
 
 ==main difference from Thevenin's theorem is that Norton's theorem is a current source in parallel with a resistor==
 
 
 ## Close relationship with Thevenin's theorem

 Since Rn is determined the same way as Rth, according to source transformation(p135), we could say Rn = Rth, and In = Isc, therefore, we could say that 
 
 ![[Pasted image 36.png]]
 
 This is essentially what source transformation is, and therefore, source transformation is also called the thevenin-Norton transformation.
 
 ## Conditions for equivalent circuits
 To determine the Norton or Thevenin's equivlaent circuits, we need the following information(any two is enough, and the remaining one could be calculated using Ohm's law):
 1. the open-circuit voltage at a-b Voc
 2. the short circuit current at a-b Isc
 3. the input resistence at a-b when all the independent sources are turned off.
 
 
