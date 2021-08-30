# Neural_Network_Charity_Analysis

## Overview
The purpose of this analysis is to use neural networks to help better predict whether recipients of charity funds will have successful campaigns. The neural network will rely on data from over 34,000 organizations that have received funding from the company over the prior years.

## Results
* Target Variables: IS_SUCCESSFUL
* Feature Variables: ASKAMOUNT, STATUS, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, SPECIAL_CONSIDERATIONS
* Other Variables: SPECIAL_CONSIDERATIONS was considered a noisy variable and removed during optimization
* Model Configuration:
    * Number of Neurons: Hidden Layer 1 had 24 neurons and Hidden Layer 2 had 12 neurons
    * Number of Layers: Two hidden layers
    * Activation Functions: Relu for the hidden layers and sigmoid for the output layer
    * Honestly I have no real idea why these were chosen beyond being instructed that these parameters should be used as the base case. Additional information on this included in the summary section. 


![image](https://user-images.githubusercontent.com/82549092/131277396-3c1f0aed-4b5b-45fb-9981-36ee4f189a6b.png)


* Model Performance: The model achieved an approximate accuracy of 73% and a loss of 55%.
* Steps to Increase Model Performance:
    *  Removed variables not related to the target
    *  Increased the number of layers
    *  Increased the number of neurons
    *  Changed the activation function of the hidden layers from "relu" to "softmax".

## Summary
Based on the deployed neural network model, there is an approximately 75% chance of predicting if a project will be successful, but unfortunately this comes at a large loss of 55%. Making changes the number of neurons, layers, and activation functions did not significantly change these results.

I would recommend using a different model for this scenario. This scenario is extremely similar to the credit risk problem a few weeks back, where a categorical yes or no is not the best solution. It would be better to estimate the chances of success for each project based on the input variables. The covariance between these different projects could then be studied to determine if the company has a strong concentration of risk in a specific industry, as it is reasonable to assume that macroeconomic factors within and industry during a specific time also has a large impact on if a project is successful.

The two main issues with using the neural network models are:
* Confirmation bias - this exercise seemed to push the idea that if you continue to change variables and functions, you will eventually get the desired results. By removing too many "noisy" variables to get the desired outcome, it appears you could be simply ignoring variables that make it so that you _cannot_ accurately predict success. 
* Model understanding - most of this lesson, as well as what I have read online seem to just be documentation on how to choose inputs so that you get your desired results, but not on how the model works. Without having a clear understanding of how the model works, it is extremely easy to make a critical error without realizing it. Without understanding the model, you have no standing when questioned as to why you didn't predict a project failing.



