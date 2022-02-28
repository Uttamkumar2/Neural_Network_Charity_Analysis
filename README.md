# Neural Network Charity Analysis

## Overview

The Objective of this analysis is to determine if organizations that were funded by the company Alphabet Soup, used their money effectively. There were more than 34,000 organizations that had received funding from Alphabet soup. Data is give in csv file, contains following columns like application type, industry sector, government classification, use case for funding, organization type etc. I created neural network models using Scikit-Learn, Tensorflow and Keras to complete this analysis.

## Result

* The columns "EIN" & "NAME" were dropped becuase were not infludencing the outcome
* The column "Is Successful" had a value of 1 if the funding was used effectively and a value of 0 if it wasn't. I used this as my target variables.
* Used "Affiliation", Classification", "Organization", "Income Amount" "Special Considerations" and "Ask Amount" as feature variables.

![datafreme_df](https://user-images.githubusercontent.com/91766890/155928957-1e430ff5-4449-4fca-bd35-9102b59649ba.png)

* Accuracy Attempt 1 : Droping more redundent columns,  changing binning cutoffs and more hidden layers.
  ![accuracy_attempt1](https://user-images.githubusercontent.com/91766890/155931189-4671581e-a6e6-487d-99d2-1726da0f4af4.png)

* Accuracy Attempt 2 : Changing activation functions
  ![accuracy_attempt2](https://user-images.githubusercontent.com/91766890/155931203-64a9cfe4-46e6-48f3-917b-813d20012839.png)

* Accuracy Attempt 3 : kerastuner Search 
  ![accuracy_attempt3](https://user-images.githubusercontent.com/91766890/155931214-a9421307-59e8-4f38-b8ad-ff1def7355f7.png)


## Compiling, Training and Evaluating the Model
* I used 3 layers (excluding the output layer) with 10 neurons each. I increased the number of neurons and hidden layers from my initial attempts since it gave better results. I used a combination of tanh and relu activation functions as it gave slightly better results than using a relu activation function alone.
* The highest model performance I could achieve was ~73%. I could not achieve the target model performance.
* To tune the model, I first tried dropping more redunt colunes like "EIN","NAME", "STATUS", "SPECIAL_CONSIDERATIONS" as it was not influencing outcome. and change banning cutoffs, add more hidden layers, I achieved acuracy 72%
* Then I tried by chaning activation function
* in #3rd attempt I used kerastuner to search for the best hyperparameters to train the model. The acuracy I achieve was comprable to by using activation fuction.

## Summary

Overall, the model, even with the optimization attempts, could not yield the 75% accuracy target, falling short at 73%. As there are quite a few negative values in the scaled dataset, We can give more attempt using SVM to solve this problem, SVM have an advantage over neural networks for binary classification problem.

