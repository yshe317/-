# About network analysis
there are two meaningful means of network analysis: nodal analysis and mesh analysis.

nodal analysis is using KCl while mesh analysis uses KVL

# Nodal Analysis
## with current sources
There are 3 steps in the nodal analysis

1. select a node as a reference node, this node is assumed to have 0 potential
2. apply KCL so to each of the n-1 nonreference nodes, and use Ohm's law to express the branch currents in terms of node voltages
3. Solve the resulting simultaneous equations to obtain the unkown node voltages

* note that current always flow from higher potential to lower potentials*

## with voltage sources
there are 2 possibilities
1. voltage source is connected between reference node and nonreference node, we could set the voltage at the nonreference node equal to the voltage of the voltage source
2. if two nonreference nodes form a generalized node or supernode, we apply both KCL and KVL to determine the node voltages

supernode: formed by enclosing a voltage source connected between two nonreference node and any elements connected in parallel with it 

![[Pasted image 5.png]]

node 2, node 3 and the voltage source could be considered as a huge node, and as an entity.

## an example 
![[Pasted image 4.png]]

in the above example, we set i1, i2 and i3 as currents flowing through resistence R1, R2, and R3. in terms of node 1, I1 flows into it, while i2, i1 and I2 flows out of it. so we could obtain an equation
`I1 = I2 + i1 + i2`
and at node 2, it is I2 + i2 = i3;
we could now express

# Mesh Analysis
a mesh is a loop that does not contain any other loop within it. The Mesh Analysis applies KVL to find unkown currents, and a current through a mesh is also known as a mesh current. 

## steps to determine mesh currents
1. assign mesh currents i1, i2, .... in to the n meshes
2. apply kvl to each of the n meshes, use ohm's law to express the voltages in terms of the mesh currents
3. solve the resulting n simulaneous equations to get the mesh currents.

![[Pasted image 6.png]]

## mesh analysis with current sources
mesh example 1
![[Pasted image 20201004184455.png]]

there are two possible conditions for a mesh analysis with current sources
1. if a current source exists only in 1 mesh, then we could conduct mesh analysis in usual ways, 
2. If a current exists in both meshes, then we could create a supermesh by ignoring the current source and any elements connected in series with it.

![[Pasted image 7.png]]

Note that even though we create a supermesh, when conducting calculations, we still need to treat the mesh separately, that is, use i1 for elements in mesh 1, and i2 for elements in mesh 2. 

# Superposition
if there are more than 2 independent sources in a circuit, then we could use mesh or nodal analysis to calculate the value of a specific variable. Another approach is to determine the contribution of each variable and then add them up, this approach is known as *superposition*

## Steps to apply superposition
1. turn off all independent sources except one source. Find the output due to that active source(make one source active at a time)
2. repeat step 1 for each of the independent sources
3. find the total contribution by adding algebraically all the contributions due to independent sources.

## example
![[Pasted image 8.png]]
![[Pasted image 9.png]]











