# Neural Network Charity Analysis
## Overview
This Alphabet Soup foundation wants to be able to identify organizations that will provide good results when funded.
To that end, a file with data from 34,000 organizations, including whether they were successful or not, is being evaluated.
A neural network model will be built and trained to predict the success of these organizations.
A target of 75% or higher accuracy was desired.

## Results
### Data Preprocessing
The data for the neural network model is as follows:
- The target variable was IS_SUCCESSFUL - whether the money was used effectively.

- The features were:
  - APPLICATION_TYPE — Alphabet Soup application type
  - AFFILIATION — Affiliated sector of industry
  - CLASSIFICATION — Government organization classification
  - USE_CASE — Use case for funding
  - ORGANIZATION — Organization type
  - STATUS — Active status
  - INCOME_AMT — Income classification
  - SPECIAL_CONSIDERATIONS — Special consideration for application
  - ASK_AMT — Funding amount requested
  
- Identification columns that are not used:
  - EIN
  - NAME
### Compiling, Training and Evaluating the Model
The original model was only able to attain an accuracy of 0.7242
<img src=Resources\Original_Performance.png></img><br>
Here are the original model parameters.<br>
The activation for the inner layers is RELU and the activation for the output layer is SIGMOID.
<img src=Resources\Original_Model.png></img><br>
