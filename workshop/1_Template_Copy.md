# Pattern Name
Uncertainty



## Goal
*Describe the goal that you want to reach. The goal should be reachable by collecting information about the data, model or optimization process.*

Developing an AI-Powered Rider Compliance detector for e-scooters. 




## Problem
*Describe the specific obstacle that prevents you from reaching your goal.*

Too many approaches, hyperparameters and different architectures. And we wanted to determine the best of best.


## Context
*Describe the ML task, model type, data specifics (such as type and amount), pipeline stage, and any other contextual factors that help distinguish this pattern.*

Training a surface classification model using IMU signal data gathered from an e-scooter and labels gathered by expert riders.

## Forces
*Describe competing concerns, constraints, and influences that make this decision difficult.*

Scarcity of Annotated Data: Not enough labels. 

Failure: Model is overfitting, unable to generalize to real-world data.

Uncertainty: What is causing the overfitting? Is it the complexity of the architecture or is it the lack of data?


## Solution
*Describe what specific information you collect to achieve your goal and your method to aquired this information.*

Automated all the architectural decisions away: Determine the kernel sizes, number of filters etc. when sketching out an neural net architecture. Delegate searching for these parameters to raytune. 

## Rationale
*Explain why this specific information is the right choice to achieve your goal.*

This will assist us finding out if there is a simple yet powerful architecture that can generalize over unseen data.


## Resulting Context
*Describe the outcome. What are the advantages, disadvantages, or trade-offs?*

A fairly large model VGG-16 worked on test data, but also a LeNet variant, a much simpler model worked as good as it did. Neither of them performed good enough on real world data.




## Known Uses
*Where else might this pattern apply? Are there contexts where it would be unsuitable?*#




