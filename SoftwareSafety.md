# Functional Safety in Software development

[//]: # (Image References)
[image4]: ./docs/software_V.png "VModel"
[image5]: ./docs/Programming.png "Language"
[image6]: ./docs/MISRA.png "Guidelines"
[image13]: ./docs/Temporal.png "Temporal"
[image14]: ./docs/Deadlocks.png "Deadlocks"
[image15]: ./docs/Livelocks.png "Livelocks"
[image16]: ./docs/Clock.png "Clock"

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