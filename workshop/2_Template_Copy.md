# Pattern Name
*Give the pattern a short and descriptive name.*

Anomaly detection

## Goal
*Describe the goal that you want to reach. The goal should be reachable by collecting information about the data, model or optimization process.*

Whenever there is an anomaly during the execution of grinding tools from Bosch, they need to be detected. The data is gathered from the sensor signals of grinding tools. 


## Problem
*Describe the specific obstacle that prevents you from reaching your goal.*

Lack of labeled data -> Unsupervised learning was the only option. Gathering labels was very costly in terms of resources like time and money and human.

Manually determining and evaluating the model architecture using different hyperparameters was costly and error-prone.


## Context
*Describe the ML task, model type, data specifics (such as type and amount), pipeline stage, and any other contextual factors that help distinguish this pattern.*

Training a pattern recognition algorithm that generates clusters that can reveal right thresholds to detect anomalous samples. 

## Forces
*Describe competing concerns, constraints, and influences that make this decision difficult.*

Model size:

Time: 

Computational resources:

Labels:

## Solution
*Describe what specific information you collect to achieve your goal and your method to aquired this information.*

Using MLFlow from Tensorflow to generated results from different variations of the system defined with various hyperparameter (filter sizes for layers, loss types, etc.) sets. 

## Rationale
*Explain why this specific information is the right choice to achieve your goal.*

Using MLFlow enabled a consolidated and automated way to compare the performance of the system with different hyperparameter settings.


## Resulting Context
*Describe the outcome. What are the advantages, disadvantages, or trade-offs?*

Project finished on time, errors were manageable, results were clear and explainable to make other engineers come up with their informed decisions was possible.

## Known Uses
*Where else might this pattern apply? Are there contexts where it would be unsuitable?*

In settings which tabular data is used and where the time constraint is the core concern, using MLflow and Optuna for making HPO decisions is preferable. 
