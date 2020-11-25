# Operational Amplifiers

## Basics
an operational amplifier is a circuit element designed to perform mathmatical operations of addition, subtraction, multiplication, division, division and integration.

![[Pasted image 59.png]]


# Ideal Op Amp
an op amp is ideal if it has infinite open-loop gain, infinite input resistence and zero output resistence.

## characteristics of ideal op Amps
![[Pasted image 60.png]]
1. The currents into both input terminals are zero
this is because of the infinite input resistance, An infinite resistance means there is an open circuit and therefore current cannot enter the op amp.
2. The voltage across the input terminals is equal to zero 
which implies that v1 = v2, vd = v2-v1 = 0. An ideal op amp has zero current into its two input terminals, and hence the voltage between the two terminals is equal to zero.

# Inverting Amplifier
an inverting amplifier reverses the polarity of the input signal while amplifying it.
![[Pasted image 62.png]]

## calculate gains
![[Pasted image 61.png]]

# Non-inverting Amplifier
a non-inverting amplifier has the input voltage applied at the non-inverting terminal, and a resisteor R1 is connected between the inverting terminal and the ground. 
![[Pasted image 63.png]]

## calculate voltage gain
By applying KCL to the above circuit, we could calculate the voltage gain which is 1 + Rf/R1
![[Pasted image 64.png]]

### voltage follower
Notice that if Rf = 0 or R1 = inf, then the gain becomes 1, which becomes the circuit below, this is called a *voltage follower*

For a voltage follower, v0 = vi , as the voltage is amplified by 1, which means it remains the same.

![[Pasted image 65.png]]

voltage follower could be useful as an intermediate-stage of buffer amplifier that is used to isolate one circuit from another. 


# Summing Amplifier
![[Pasted image 67.png]]

above is a summing amplifier that could take several input signals and output a weighted sum of these inputs.

## calculate the output

![[Pasted image 68.png]]



# Difference Amplifier
Difference amplifier is a device that amplifies the difference between two inputs but rejects any signals common to the two inputs.

Below is an example of a difference amplifier

![[Pasted image 69.png]]

By applying KVL to both node a and b, we could obtain the following equation
![[Pasted image 70.png]]

and since a difference amplifier rejects any signals in common, the amplifier must have the property that vo = 0 if v1 = v2,and this property exists when
R1/R2 = R3/R4, which could simply the above euqation and make it 

![[Pasted image 71.png]]

Note that if R2 = r1 and r3 = r4, we could obtain a subtractor. 




