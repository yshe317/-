# 5.Half-wave Rectifier

a basic rectifier converts an ac voltage to a pulsating（有节奏舒张) dc voltage.

A common application of diodes is half-wave rectification. The half-wave rectifier could block either positive or negative half of the input wave. 

![[Pasted image 372.png]]


As for the constant voltage model, 
$$out = V_in - V_on = (V_psin(wt) - V_on)$$


![[Pasted image 373.png]]

Note that the output voltage is still zero when the diode is off, and the step-down transformer is just a device that could convert a higher voltage to a lower one. As shown in the picture, 240-V voltage is converted to only around 10V. 


## 5.1.0 Set up Rectifier

### 5.1.1 A Dangerous Approach
Now we need to consider how to ensure the output voltage is constant from a rectifier. The first thought is: simply replace the resistor with a capacitor, as shown in the below diagram:

  ![[Pasted image 374.png]]
  
  As the diode is turned on, voltage gradually accumulates in the capcitor, and at the peak of the input voltage, the diode current tries to reverse, shutting down the diode. However, since the capacitor has nowhere to discharge, the voltage level remains. This could be a potentially dangerous circuit as the capcitor may retain a lethal voltage after the power is switched off. 
  
  As shown in the figure, the voltage level in the capacitor goes to the peak and stays there.
  ![[Pasted image 375.png]]
  
  ### 5.1.2 Set Up A Rectifier

Due to the problem discussed above, we need to ensure that the capcitor always has somewhere to discharge. We could connect an output impedance or load resistor[^1] to discharge capacitor safely. The resistor should consume a current large enough to discharge the capacitor in a reasonable time, but small enough to minimise power waste. 

![[Pasted image 376.png]]

This rectifier ensures that the capcitor could discharge and resolves the problems metions in the previous section. We then could analyze the voltage change as the capcitor charges and discharges. 

First, the voltage level shall increase until a peak point, then the diode is off as capacitor retains higher voltage level than the input(as input voltage decreases after the peak, following a sin curve), forcing a reverse current. After diode is off, the capacitor then discharges by applying voltage to the resistor. We could then expect the voltage level to decrease, until the input voltage becomes positive again and is higher than the voltage retained by the capacitor. The input then charges the capactor again. This process repeats for each period of the sin curve.  

![[Pasted image 377.png]]

### 5.1.3 Application - DC charger

An important application of diode is DC charger.   
  
  [^1]: An electrical load is an electrical component or portion of a circuit that consumes (active) electric power. 
  
  
  
  