# Code Review


## Fagan inspection
formal review
- An early effort to formalise the process of reviews
- The basis, or at least similar, to subsequent formal approaches
- Describe program development process in terms of operations
- Define ‘entry’ and ‘exit’ criteria for all operation
- Specify objectives for the inspection process to keep the team focused on one objective at a time
### 计划(Planning)
- Preparation of materials
- Arranging of participants
- Arranging of meeting place

### 概述(Overview)
- Group education of participants on review materials
- Assignment of roles
### 准备(Preparation)
- Participants review item to be inspected and supporting material to prepare for the meeting, noting any questions or possible defects
- Participants prepare their roles
### 召开检查会议(Inspection Meeting)
- Actual finding of defect
### 重做(Rework)
- Rework is the step insoftware inspection in which the defects found during the inspection meeting are resolved by the author, designer or programmer. On the basis ofthe list of defects the low-level document is corrected until the requirements in the high-level document are met.

### 追查(Follow-up)
- In the follow-up phase of software inspections all defects found in the inspection meeting should be corrected. The moderator is responsible for verifying that this is indeed the case. They should verify that all defects are fixedand no new defects are inserted while trying to fix the initial defects.

## Formal inspection
- Management review
	- Monitor progress
	- Determine status of plans
	- Evaluate management effectiveness
	- Supports decisions about changes in direction, resource allocation, and scope
	- Maintenance plans
	- Disaster recovery
	- Migration strategies
	- Customer complaints
	- Risk management plans
- Management review roles
	- Decision maker
	- Review leader
	- Recorder
	- Management staff
	- Technical staff
- Management review processes
	-  Preparation
	-  Plan time and resources
	-  Provide funding
	-  Provide trainning 
	-  Ensure reviews are conducted
	-  Act on reviews
- Technical review
	- Software requirements
	- Software desgin
	- Software test documentation
	- Specifications
	- ... procedures
- Technical review roles
	- Decision maker
	- Review leader
	- Recorder
	- Technical reviewer

![[Pasted image 20201128204148.png]]


### Change List/Pull Request reviews
- A complete, ‘working’ project exists
- A set of changes are to be applied
- The changes must be reviewed before they are accepted
- Owner
	- Is this change wanted?
- Technical Reviwer 
	- Does this change work?
- Technical Reviwer
	- Is this change maintainable?•(Can I understand it?)


## Design by Contract (DbC)




## review challenges
- Size
	- make many small changes will be more managable than a big change.