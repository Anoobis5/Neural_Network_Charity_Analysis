# Neural_Network_Charity_Analysis

## Project Over View

For this project, we were tasked with using a Deep-Learning Neural Network Model to analyze and classify the success of charitable donations. We used the data set of Charity Donations to create a binary classifier to predict if the applicants thatt will be funded by a charitable organization called Alphabet Soup will be successful. Our analysis consists of 3 main steps:

  * Processing the data for the neural-network
  * Compile, Train, and Evaluate the Model
  * Optimize the model for best accuracy



## Results

#### Data Processing

When processing our data, we first removed the identification columns [EIN] and [NAME]:


![Drop_EIN_NAME](https://user-images.githubusercontent.com/84881187/137591437-a0644d10-1142-4e56-be63-74e0ea2af6b1.PNG)

Next, we targeted the column [IS_SUCCESSFUL], as this column contains binary data as to whether or not the charity donation was used effectively. For the features of our Neural-Network model, we used: [APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT]. We then endcoded the categorical variables using one-hot encoding, split into training and testing data sets, and standardized the values using the StandardScaler() module. 



#### Compile, Train, and Evaluate the Model

The deep Neural-Network model we used primarily consists of two hidden layers with 80 neurons in the first layer, and 30 neurons in the second layer. Our input data has 25,724 samples, and 43 features. To expidite our training process, we used the activation function [relu] for our hidden layers; and since our output is a binary classification, we used the Sigmoid function in our output layer.

When we trained our model, we found an accuracy of 72.7. This is a sub-par performance in predicting the outcomes of charitable donations. 

![Original_Model](https://user-images.githubusercontent.com/84881187/137592027-313d380f-a760-4a4e-8116-2e91102b35da.PNG)

![Original_Model_Accuracy](https://user-images.githubusercontent.com/84881187/137592030-84075875-56ce-4f11-b018-02e96012224b.PNG)



## Project Summary
