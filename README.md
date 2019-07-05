# Functional Safety

[//]: # (Image References)

[image1]: ./docs/ISO_26262.png "ISO"
[image2]: ./docs/V_Model.png "Software"
[image3]: ./docs/V_Model_2.png "Requirement"
[image4]: ./docs/software_V.png "VModel"
[image5]: ./docs/Programming.png "Language"
[image6]: ./docs/MISRA.png "Guidelines"

## Introduction
The term "functional" comes from a branch of systems engineering called requirements engineering. 

* Functional requirements* - what your system is supposed to do; in other words, the system's functions.

* Non-functional requirements* - how the system should behave: for example, how reliable is the system?

Functional safety looks at what happens when the system does something that it was not supposed to do, which is called a malfunction.

The most generic standard is IEC 61508, which originated from industrial markets.  It currently exists as a standard in the IEC/ISO basic safety publication, which covers "general functional safety," for a number of industries. ISO 26262 specifically applies to automotive passenger vehicle electrical and electronic systems. The ISO 26262 standard is an branch of the IEC 61508 standard.

## Project Reference
[Functional Safety](https://github.com/udacity/CarND-Functional-Safety-Project)

## Do and Don'ts
* Functional safety only looks at the electrical and electronic system malfunction.
* Functional safety does not test for nominal performance.
* If a potential electrical malfunction could cause the battery fire, that could be a part of a functional safety analysis. The car battery chemicals generally would be part of chemical system safety.
* Autonomous vehicle technology is so new that standards like ISO 26262 do not yet even consider certain issues related to self-driving cars such as machine learning algorithms.

## The Basics of Functional Safety: Review
* Identify Hazards
* Evaluate the risk
* Using System Engineering to Lower Risk

## ISO 26262

![alt text][image1]

## V Model 

![alt text][image2]

## Hardware and software
![alt text][image3]

## Software development
### The V Modle 
![alt text][image4]

### The programming language
![alt text][image5]

### MISRA
![alt text][image6]