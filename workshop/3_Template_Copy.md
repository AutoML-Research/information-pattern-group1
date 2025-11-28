# Pattern Name
*Give the pattern a short and descriptive name.*

High noise in target in a small dataset.

## Goal
*Describe the goal that you want to reach. The goal should be reachable by collecting information about the data, model or optimization process.*

Stock returns forecasting and risk modeling.


## Problem
*Describe the specific obstacle that prevents you from reaching your goal.*

Stock returns are unpredictable. We need a competitive model that performs on par with the state of the art.


## Context
*Describe the ML task, model type, data specifics (such as type and amount), pipeline stage, and any other contextual factors that help distinguish this pattern.*

Training a time-series forecasting model for tabular, numerical data. Features to be used was fixed: Fundamental analysis, low-frequency price data etc.


## Forces
*Describe competing concerns, constraints, and influences that make this decision difficult.*

Need for accuracy: Stock return forecasting is hard but the system should be at least as good as the competitor.

Robustness to noise in face of biased data:

Explainability: Why does the model make the decisions it makes is important for client. They would like to understand the contribution of each feature that led to a certain decision of the model.


## Solution
*Describe what specific information you collect to achieve your goal and your method to aquired this information.*

Optuna and Tpot enabled us tuning our hyperparameters and making model selection decisions. 
 

## Rationale
*Explain why this specific information is the right choice to achieve your goal.*

The goal was to understand the effect of the noise: The tool would enable us to see if we bias we face is stemming from the data or the architecture.  


## Resulting Context
*Describe the outcome. What are the advantages, disadvantages, or trade-offs?*

Our suspicions about the data bias was verified: Architectural decision that we have made prior using automl-like tools were not the source of the problems.

Using the automl-like tools increased the amount of work unnecessarily, return on investment was underwhelming.

## Known Uses
*Where else might this pattern apply? Are there contexts where it would be unsuitable?*

Benefits of automl-like tools would be limited where experts opinions about where the bias stemming from are clear and accurate. In a scenario where data is extremely noisly, the GIGO principal holds.
