# Neural_Network_Charity_Analysis

## Overview

The Objective of this analysis is to determine if organizations that were funded by the company Alphabet Soup, used their money effectively. There were more than 34,000 organizations that had received funding from Alphabet soup. Data is give in csv file, contains following columns like application type, industry sector, government classification, use case for funding, organization type etc. I created neural network models using Scikit-Learn, Tensorflow and Keras to complete this analysis.

## Result

* The columns "EIN" & "NAME" were dropped becuase were not infludencing the outcome
* The column "Is Successful" had a value of 1 if the funding was used effectively and a value of 0 if it wasn't. I used this as my target variables.
* Used "Affiliation", Classification", "Organization", "Income Amount" "Special Considerations" and "Ask Amount" as feature variables.

![datafreme_df](https://user-images.githubusercontent.com/91766890/155928957-1e430ff5-4449-4fca-bd35-9102b59649ba.png)

## Compiling, Training and Evaluating the Model
* I used 3 layers (excluding the output layer) with 10 neurons each. I increased the number of neurons and hidden layers from my initial attempts since it gave better results. I used a combination of tanh and relu activation functions as it gave slightly better results than using a relu activation function alone.
* The highest model performance I could achieve was ~73%. I could not achieve the target model performance.
* To tune the model, I first used kerastuner to search for the best hyperparameters to train the model. I achieved an accuracy of ~72%
* Next I manually tuned the data by
    Dropping more redundant columns like "EIN","NAME", "STATUS", "SPECIAL_CONSIDERATIONS" as it was not influencing outcome.
    Changing binning cutoffs
    Adding more hidden layers and neurons
    Changing the activation functions The accuracy I achieved was comparable to the accuracy from searching for the best hyperparameters.

## Summary
