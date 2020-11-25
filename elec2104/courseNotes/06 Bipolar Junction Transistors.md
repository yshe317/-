# 6.1 Biasing a Bipolar Junction

## 6.1.1 What happens in an NPN Junction?

This is a NPN junction which has two n-side on the two sides and one p section in the middle. We could apply a forward bias on the left side and reverse bias on the other side. This results in an interesting phenomenon: there is a current flowing from the left side to the right in spite of the reverse bias on the right hand side N section.

![[Pasted image 20200928135857.png]]

This is what happens: the forward biased junction could be considered as a diode that is on. Electrons move across the junction in the form of diffusion current, and in the middle P region, some electrons recombine with holes, and the rest may move out of the NPN junction or enter the depletion region. 

![[Pasted image 20200928140203.png]]

However, the right hand side diode is under reverse bias, which means it has a strengthened built-in potential. This means that the region prevents the flow of majority carriers across the junction. 

However, since we "injected" the electrons into the p-side of the depletion region, they just flow to the n side(as they are free carriers, instead of fixed carriers in the region).   

![[Pasted image 20200928140529.png]]

## 6.1.2 Modify the NPN junction
Our goal is to let electrons enter an N side, flow through the depletion region and be swept to another N side without recombining with holes in the middle P region. In order to minimise the probability of recombination, we could have the N region under forward biased be heavily doped, so that it is rich in electrons. Also, we could make the P region very narrow so electrons won't have the time to recombine before it is "swept" to another end of the junction. Another N side(right hand side) is slightly more doped, but not as heavily doped as the N side that is under forward bias. 

![[Pasted image 20200928140926.png]]

## 6.1.3 Bipolar Junction Transistor

A NPN junction with this set up is called a **Bipolar Junction Transistor**(BJT). There are three regions in a BJT: Emitter, Base, and Collector. As we could see in the below figure, a current from the base may be amplified and becomes much larger when it flows out of the emitter(as it combines with the curent flowing into the collector). 

Generally speaking, the base-emitter diode is forward biased and the base-collector diode is reverse biased. 

![[Pasted image 20200928141259.png]]


below is the comparison between a reverse biased PN junction and a reverse biased PN junction in a BJT configuration

![[Pasted image 20200928152213.png]]


## 6.1.4 PNP and NPN transistors
PNP transistors have the same functionality as the NPN transistors, they just have different majority carriers. In NPN transistors, the emitters are connected to a lower voltage than the collector. In PNP transistor, the emitter is also under forward biased. 

![[Pasted image 20200928152620.png]]

below is a diagram for an NPN transistor, note how it looks similar to the PNP transistor, but the base current direction is the opposite, as well as the emitter and collector current. 

![[Pasted image 20200928152730.png]]

Below are symbols for NPN and PNP transistors. Note that in this course, we will mainly focus on the NPN transistor.

![[Pasted image 20200928152851.png]]

---

# 6.2 NPN BJT currents
## 6.2.1 transport model
In NPN BJT, emitters inject electrons into base region, and almost all these electrons could travel across the narrow base and are collected by the collector. The base-emitter voltage $V_{BE}$ and the base collector voltage $V_{BC}$ determine currents in transistor. The voltage is positive when their corresponding diode is under forward bias. In NPN transistor, $V_{BE}$ is positive as the emitter should be under forward bias.  

we specify certain terminal currents: collector ($i_c$), base($i_B$) and emitter ($i_E$). Notice that the **forward active region** of a NPN BJT is when ==$V_{BE} > 0, V_{BC} < 0$.==This [[07. Different modes of operations and biasing BJT#7 2 Other regions of Operation|mode of operation]] is most frequently used for a BJT. 


The base-emitter voltage establishes the emitter current $i_E$
![[Pasted image 20200928152933.png]]

## 6.2.2 Forward active collector current
>** Forward active collector current** is the current flowing from the collector to base. This current has the **same** equation as the current in the base-emitter diode. 


The current $I_C$ could then be calculated using [[03.1 PN Junction#Diode I-V characteristics|diode i-v characteristics]], and the fact that the current is the same as in the base-emitter diode. (as shown in the diagram, it's the same current flowing across collector --> base --> emitter). 

> $$i_C = i_F = I_S[exp(\frac{V_{BE}}{V_T} - 1)]$$

and $I_S = \frac{AqD_nn_i^2}{N_AW_B}$
![[Pasted image 20201015152555.png]]

## 6.2.3 Base current
The base current is a small current proportional to the collector current. and its relationship with $i_C$ could be expressed with a gain $\beta$:

>$$\beta_F = \frac{i_C}{i_B}$$

Here, $\beta_F$ is the **forward** comman emitter current gain and has the range(depending on base width and emitter doping)

$$10 \leq \beta_F \leq 500$$


## 6.2.4 Forward Emitter Current
Since we've got base current and the collector current, with KCL, we could calculate the emitter current $i_E$

$i_E = i_C + i_B = I_S(1+\frac{1}{\beta_F})[exp\frac{V_{BE}}{V_T}-1] = \frac{I_S}{\alpha_F}[exp\frac{V_{BE}}{V_T}-1]$

Here $\alpha_F$ is the forward **common-base current gain**, which is 
>$$095 \leq \alpha_F = \frac{\beta_F}{\beta_F+1} \leq 1.0$$

> $$\beta_F = \frac{\alpha_F}{1-\alpha_F}$$

## 6.2.5 Summary of forward active current
BJT under forward active region could be considered as an "amplifier" as it could amplify the base currents and output a much larger current in the emitter terminal.

Injection of small base current could result in amplified changes in both the emitter current and collector current. This is because
$i_C = \beta_F \times i_B$ and $i_E = (\beta_F + 1)i_B$

Also, the collector and emitter currents are almost equal when the forward active base current gain($\alpha_F$) is approximately 1. This means that $i_C$ is almost the same as $i_E$


## 6.2.6 BJT Configurations
There are three ways to configure a BJT when operating as an amplifier: Common emitter, common base and common collector. The common emitter is the most frequently used configuration among the three.

![[Pasted image 20201015160159.png]]

As for the common emitter, we basically have the input and output terminals sharing the emitter terminal, and hence we are looking at the current flowing through the base and out of the collector. (as indicated by the red curve). This is why $\beta_F$ is called the common emitter current gain, and $\alpha_F$ is called the common-base current gain.  

# 6.3 PNP Forward Active Region
The forward active region of a BJT is when $V_{BE} < 0,V_{BC} > 0$.  

All the equations for NPN still hold for PNP BJT, except that all the voltages and currents are referenced oppositely.

![[Pasted image 20201015160918.png]]


# 6.4 Large Signal Model
The large signal model handles situations where the range of inputs is so huge that the device cannot be turned into a linear model[^1].  We could turn a BJT into the following model. This is done by modeling the behavior of a BJT.

Since $V_{BE}$ controls the state of a BJT, we could model it as a diode. If it has a positive voltage, then the BJT is forward biased and could allow base current to flow to the emitter. (which is also the case and the base-emitter junction is just a diode). We could also model the collector side as a voltage-controlled current source which changes with $V_{BE}$


![[Pasted image 20201015162041.png]]

Notice that since $i_B = \frac{I_S}{\beta_F}[exp(\frac{V_{BE}}{V_T}-1)]$,  in order to model the relationship between $i_B$ and $i_C$, however, the i-v characteristics of a diode does not have $\beta_F$ at the denominator, so we need to get rid of it by setting the cross-section area of the diode to $\frac{1}{\beta_F}$ as $I_S \propto A$
![[Pasted image 20201015162642.png]]

## 6.4.1 Chain of dependency
When determining values in a large singal model, there is a chain of dependency:

$$V_{BE} \rightarrow I_C \rightarrow I_B \rightarrow I_E$$


# 6.5 Small Signal Model
If we keep the change of input at a very small level, then we could compute a linear model for a BJT. The relationship between $V_{BE}$ and $I_C$ is almost linear when looking at the small signal model .

>$$I_C = KV_{BE}$$

Notice here **K** represents a relationship between the base emitter voltage and the collector current. Using this equation, we could measure the output voltage in small signal mode.
![[Pasted image 20201015164849.png]]

We could add a load resistor $R_L$ to the circuit, which is used to measure the output voltage. Since $-KV_{in}$ is the current flowing through $R_L$, using [[Ohm's law and Kirchoff's law#Ohm's law| Ohm's law]], we could compute the output voltage. 

we could also obtain the following equation
> $$\frac{V_{out}}{V_{in}} = -KR_L$$

If $KR_L > 1$, it means  the input voltage is amplified. 


[^1]: linear model: the circuit parameters are constant, and do not change with input voltage or current


## 6.5.1 Transconductance
> The **transconductance** of a diode measures how well it could convert voltage to current. It is denoted by $g_m$.

As for large signal analysis, $G = \frac{1}{R}$, however, for small signal analysis, $g_m$ is just the derivative of $I_C$ according to $V_{BE}$, which measures how changes in $V_{BE}$ affects $I_C$.
Hence $g_m = \frac{d}{dV_{BE}}(exp[\frac{V_{BE}}{V_T}-1]) = \frac{1}{V_T}(exp[\frac{V_{BE}}{V_T}-1]) =\frac{I_C}{V_T}$

>$$g_m = \frac{I_C}{V_T}$$
>$$\Delta I_C = g_m\Delta V_{BE}$$

![[Pasted image 20201015165547.png]]


## 6.5.2 Small signal model
To derive the small signal model from a large signal model, we could just change the DC input to a change in voltage($\Delta V_{BE}$). The "small" here refers to the small signal that is much smaller than the thermal voltage. 

This means that the magnitude of the AC signal provided must be small so that the BJT always operate in the linear region throughout the input cycle. 

![[Pasted image 20201015170351.png]]

## 6.5.3 Hybrid-Pi model

The change in collector current is $\Delta I_C = g_m\Delta V_{BE}$ and the change in base current $\Delta I_B = \frac{I_C}{\beta_F} = \frac{g_m\Delta V_{BE}}{\beta_F}$.

We could then derive:
>$$\frac{\Delta V_{BE}}{\Delta I_B} = \frac{\beta}{g_m} = r_{\pi}$$

where $r_\pi$ is the small signal resistance between base and emitter. This means we could further simplify the circuit to this:

![[Pasted image 20201015171014.png]]

In forward active model, a change in $\Delta V_{CE}$ does not influence the collector current or base current as it only depends on $V_{BE}$. 

$\Delta V_{CB}$ has no influence on the small signal model either. 


## 6.5.4 BJT circuit analysis using Small Signal Model
![[Pasted image 20201123160026.png]]

# 6.6 Early Effect
This is due to the non-idea characteristics of a BJT. In BJT, $V_{CE}$ does not influence the base emitter current $V_{BE}$, nor $I_C$. However, in reality, $V_{CE}$ does influence $I_C$ and the maximum current gain to some extent.

As $V_{CE}$ increases, the reverse bias increases, and the depletion region increases. The p section then decrease in width in the same amount, which is the effective base width. As the base decreases, the gain increases.(as current could more easily flow through the base, resulting in more current). Hence, increase in $V_{CE}$ could potentially increase the gain.

Also, since the effective width decreases, electrons could be more easily swept from the emitter side to the collector side(less change of recombination), also resulting in a greater current. 

This is known as the **Early Effect**.

As shown in the below diagrams, in reality, changes in the collector emitter voltage changes the collector current slightly. 
![[Pasted image 20201015220646.png]]

## 6.6.1 Early Voltage
After obtaining the characteristics plot under Early effect, if we trace the curves back which intersect at a common point where $I_C = 0$, where $V_{EC} = -V_A$. In order to take into account the early effect, we could time the current with a multiplicative factor. That is:

>$$I_C = I_S(exp\frac{V_{BE}}{V_T})(1+\frac{V_{CE}}{A})$$
>$$\beta_F = \beta_{F0}(1+\frac{V_{CE}}{A})$$
>$$I_B = \frac{I_S}{\beta_{F0}}(exp\frac{V_{BE}}{V_T})$$

$V_A$ could be assumed **infinite** if not specifically stated

## 6.6.2 Apply in Large signal model
We could account for the slope of the early effect by simply applying a correction factor to the collector current. 

Since $I_C = I_S(exp\frac{V_{BE}}{V_T})(1+\frac{V_{CE}}{A})$, and $V_{CE} \ll V_A$, we could safely neglect the $\frac{V_{CE}}{V_A}$ term and just substitude the $I_C$ expression for the derivative:
$$\frac{dI_C}{dV_{CE}} = I_S(exp\frac{V_{BE}}{V_T})(\frac{1}{V_A}) \approx \frac{I_C}{V_A}$$

$$\frac{dI_C}{dV_{BE}} = I_S(exp\frac{V_{BE}}{V_T})(1+\frac{V_{CE}}{V_A})\frac{1}{V_T} = \frac{I_C}{V_T}$$

The second expression is just $g_m$, and the early effect does not influence it. 


## 6.6.3 Apply in Small Signal Model
To account for the slope of the collector current, a resistor is addded.  
![[Pasted image 20201015223129.png]]

Since $r_\pi$ is determined by $i_b$, while $i_b$ is not influenced by the early effect, $r_\pi = \frac{\beta}{g_m}$ still holds true. $r_o$ is the output resistence and is connected between the emitter and collector terminals. Hence we could calculate $r_o$ 
$$r_o = \frac{\Delta V_{CE}}{\Delta I_C} = \frac{V_A}{I_S(exp\frac{V_{BE}}{V_T})} \approx \frac{V_A}{I_C}$$

Now both ==$R_L$ and $r_o$== could affect the maximum gain
