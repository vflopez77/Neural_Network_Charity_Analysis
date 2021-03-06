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
- Here are the original model parameters:<br>
  - The activation for the inner layers is <b>RELU</b> and the activation for the output layer is <b>SIGMOID</b>.<br>
  - There were 80 nodes in the first hidden layer and 30 in the second hidden layer.<br>
  - There were 50 training epochs for all models as no improvement was ever observed after 50.<br>
<img src=Resources\Original_Model.png></img><br>
- The original model had an accuracy of <b>0.7242</b>.
<img src=Resources\Original_Performance.png></img><br>

- The first attempt at optimization had the following changes:
  - Dropped the possible noisy SPECIAL_CONSIDERATIONS field.
  - Added nodes to both hidden layers.
 - Here are the parameters for the first optimization attempt:<br>
    - The activation for the inner layers is <b>RELU</b> and the activation for the output layer is <b>SIGMOID</b>.<br>
    - There were 120 nodes in the first hidden layer and 60 in the second hidden layer.<br>
    - There were 50 training epochs.<br>
<img src=Resources\Optimization1_Model.png></img><br>
 - The first optimization attempt had an accuracy of <b>0.7248</b>, showing a very slight improvement.
  <img src=Resources\Optimization1_Performance.png></img><br>
  
- The second attempt at optimization had the following changes:
  - Dropped the possible noisy INCOME_AMT field.
  - Added a third hidden layer.
 - Here are the parameters for the second optimization attempt:<br>
    - The activation for the inner layers is <b>RELU</b> and the activation for the output layer is <b>SIGMOID</b>.<br>
    - There were 82 nodes in the first hidden layer, 41 in the second hidden layer, and 20 in the third hidden layer.<br>
    - There were 50 training epochs.<br>
<img src=Resources\Optimization2_Model.png></img><br>
 - The second optimization attempt had an accuracy of <b>0.7195</b>, showing worse performance.
  <img src=Resources\Optimization2_Performance.png></img><br>
    
- The third attempt at optimization had the following changes:
  - Restored SPECIAL_CONSIDERATIONS and INCOME_AMT fields.
  - Number of hidden layer nodes altered to match original model.
  - Activation function for hidden layers changed from RELU to the more modern Swish.
 - Here are the parameters for the first optimization attempt:<br>
    - The activation for the inner layers is <b>SWISH</b> and the activation for the output layer is <b>SIGMOID</b>.<br>
    - There were 80 nodes in the first hidden layer and 30 in the second hidden layer.<br>
    - There were 50 training epochs.<br>
<img src=Resources\Optimization3_Model.png></img><br>
 - The second optimization attempt had an accuracy of <b>0.7202</b>, slightly better than Attempt #2 but worse than Attempt #1 and the original model.
  <img src=Resources\Optimization3_Performance.png></img><br>

## Summary
- While this model shows some potential for automating the identification of worthwhile organizations for Alphabet Soup, it is not ideal and does not acheive the 75% accuracy goal.
- A simpler model such as Logistical Regression may prove to be more appropriate for this problem.
- A larger and more complete data set may be needed for a neural network model to work effectively.
