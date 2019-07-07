# Functional Safety
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

[//]: # (Image References)

[image1]: ./docs/ISO_26262.png "ISO"
[image2]: ./docs/V_Model.png "Software"
[image3]: ./docs/V_Model_2.png "Requirement"
[image4]: ./docs/software_V.png "VModel"
[image5]: ./docs/Programming.png "Language"
[image6]: ./docs/MISRA.png "Guidelines"
[image7]: ./docs/ASIL.png "ASIL"
[image8]: ./docs/Hazard.png "Hazard"
[image9]: ./docs/FlattenV.png "Linear"
[image10]: ./docs/Software_safety.png "Software Safety"
[image11]: ./docs/Robustness.png "Software Safety"
[image12]: ./docs/Interference.png "Freedom"
[image13]: ./docs/Temporal.png "Temporal"
[image14]: ./docs/Deadlocks.png "Deadlocks"
[image15]: ./docs/Livelocks.png "Livelocks"
[image16]: ./docs/Clock.png "Clock"

## Introduction
The term "functional" comes from a branch of systems engineering called requirements engineering. 

* Functional requirements* - what your system is supposed to do; in other words, the system's functions.

* Non-functional requirements* - how the system should behave: for example, how reliable is the system?

Functional safety looks at what happens when the system does something that it was not supposed to do, which is called a malfunction.

The most generic standard is **IEC 61508**, which originated from industrial markets.  It currently exists as a standard in the IEC/ISO basic safety publication, which covers "general functional safety," for a number of industries. *ISO 26262* specifically applies to automotive passenger vehicle electrical and electronic systems. The ISO 26262 standard is an branch of the IEC 61508 standard.

## Project Reference
[Functional Safety](https://github.com/udacity/CarND-Functional-Safety-Project)

## Do and Don'ts
* Functional safety only looks at the electrical and electronic system malfunction.
* Functional safety does not test for nominal performance.
* If a potential electrical malfunction could cause the battery fire, that could be a part of a functional safety analysis. The battery chemicals generally would be part of chemical system safety.
* Autonomous vehicle technology is so new that standards like ISO 26262 do not yet even consider certain issues related to self-driving cars such as machine learning algorithms.

## The Basics of Functional Safety
* Identify Hazards
* Evaluate the risk
* Using System Engineering to Lower Risk
---

## ISO 26262

![alt text][image1]

The ISO 26262 functional safety standard follows the V model.

* *Requirements engineering* Define what the system is going to do
* *Designing or modifying a system architecture* Design what the system will look like
* *Test the system* to make sure it behaves as expected
* *Integrate the system* into larger systems

## V Model 

![alt text][image2]

## Flattened V Model
Flatten out the V model to see it from a linear perspective.

![alt text][image9]

## Hazard Analysis and Risk Assessment

![alt text][image8]

## ASIL

![alt text][image7]

## Hardware and software
![alt text][image3]

## Software safety requirements
The software requirements are much more specific than technical requirements. Software requirements specify variable names, signal paths and software protocols and mechanisms. 

### Sources of Software Safety Requirements
![alt text][image10]

### Software Robustness and Quality
![alt text][image11]

### Freedom from Interference
![alt text][image12]

Types of interference
* Spatial interference
* Temporal interference
* Communication interference
---

## Software development
### The V Modle 
![alt text][image4]

### Mechanism for ensuring freedom from spatial interference
* Memory protection unit (MPU)
* Dual storage of relevant data
* Redundancy checks such as CRC to make sure data does not inadvertently change.
* Micro-controllers with memory error detection and correction capabilities
* Operating systems that allow software units to have their own virtual memory space

#### MPU
MPU is a prevention method because it stops elements from accessing memory to which they should not have access. An MPU can be programmed to set up the proper read, write and execute permissions between software elements.

#### Dual Storage
Dual storage of relevant data like with a 2's complement is a detection method.

### Mechanisms for Freedom from Temporal Interference

![alt text][image13]

#### Deadlocks Vs Livelocks

![alt text][image14]

Thread 1 needs Resource B and have Resource A. But Thread 2 keeps interrupting Thread 1 to grab Resource B. Same way Thread 2 needs Resource A and have Resource B is called deadlocks

![alt text][image15]

Both the threads have courtesy to go the other thread to go first.


#### Priority Ceiling
For addressing deadlocks, disabling OS interrupts that would stop process preemption, is inefficient and could compromise the overall response time and system latency. An alternative is a feature that is provided by a Real Time Operating System (RTOS) is a *priority ceiling*.

#### Synchronization

Clock synchronization between two Electronic Control Unit (ECU)

![alt text][image16]

#### Mechanism to prevent
* Cyclic execution scheduling
* Fixed priority based scheduling
* Time triggered scheduling
* Monitoring of processor execution time
* Program sequence monitoring
* Arrival rate monitoring.

#### 3 Safety Mechanism
* Alive supervision - Number of time the element got executed.
* Deadline monitoring - How long it takes to execute the software.
* Control flow monitoring - Software executed in the correct order.

### The programming language
![alt text][image5]

### MISRA
![alt text][image6]