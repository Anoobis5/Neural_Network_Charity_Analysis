# Neural_Network_Charity_Analysis

## Project Over View

For this project, we were tasked with using a Deep-Learning Neural Network Model to analyze and classify the success of charitable donations. We used the data set of Charity Donations to create a binary classifier to predict if the applicants thatt will be funded by a charitable organization called Alphabet Soup will be successful. Our analysis consists of 3 main steps:

  * Processing the data for the neural-network
  * Compile, Train, and Evaluate the Model
  * Optimize the model for best accuracy



## Results

### Data Processing

When processing our data, we first removed the identification columns [EIN] and [NAME]:


![Drop_EIN_NAME](https://user-images.githubusercontent.com/84881187/137591437-a0644d10-1142-4e56-be63-74e0ea2af6b1.PNG)

Next, we targeted the column [IS_SUCCESSFUL], as this column contains binary data as to whether or not the charity donation was used effectively. For the features of our Neural-Network model, we used: [APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT]. We then endcoded the categorical variables using one-hot encoding, split into training and testing data sets, and standardized the values using the StandardScaler() module. 



### Compile, Train, and Evaluate the Model

The deep Neural-Network model we used primarily consists of two hidden layers with 80 neurons in the first layer, and 30 neurons in the second layer. Our input data has 25,724 samples, and 43 features. To expidite our training process, we used the activation function [relu] for our hidden layers; and since our output is a binary classification, we used the Sigmoid function in our output layer.

When we trained our model, we found an accuracy of 72.65. This is a sub-par performance in predicting the outcomes of charitable donations. Our next step is to try to optimize our model to reach optimal performance.

![Original_Model](https://user-images.githubusercontent.com/84881187/137592027-313d380f-a760-4a4e-8116-2e91102b35da.PNG)

![Original_Model_Accuracy](https://user-images.githubusercontent.com/84881187/137592030-84075875-56ce-4f11-b018-02e96012224b.PNG)



### Optimizing the model

Our first attempt at optimization was to add more hidden layers. We kept the 80 and 30 neuron layers and added 10, 50, and 70 neuron layers to our model. This results in 21,071 Traimable params, with an accuracy of 72.43.

![Attempt_1_Add_Layers](https://user-images.githubusercontent.com/84881187/137592613-dcc38f16-4126-4b18-a671-a35343085d7f.PNG)
![Attempt_1_Add_Layers_Accuracy](https://user-images.githubusercontent.com/84881187/137592617-39da724d-8d85-4cd3-ab4d-a5985add0d71.PNG)



In our Second Attempt at optimization, we used a different output function, namely [tanh]. This results in 5,981 Trainable params, with an accuracy score of 72.89.

![Attempt_2_Different_Output_Function](https://user-images.githubusercontent.com/84881187/137592725-3a6a6517-93c5-4c08-9dd0-e97d6ae2d623.PNG)
![Attempt_2_Different_Output_Function_Accuracy](https://user-images.githubusercontent.com/84881187/137592727-c7d653b4-3c25-4030-8619-bcc44883ef73.PNG)


For the Third Attempt, we used different functions for our layer actication. We changed our [relu] activation to [tanh] and kept the output activation at [sigmoid]. This resulted in 5,981 Traimable params once again, and an accuracy score of 72.06.

![Attempt_3_Different_Act![Attempt_3_Different_Activation_Accuracy](https://user-images.githubusercontent.com/84881187/137592787-b2d6db2c-7da5-4f14-ac00-ad9ef08330bd.PNG)
ivation](https://user-images.githubusercontent.com/84881187/137592784-27090825-c138-46c4-9e3e-a2ae44a1c823.PNG)


For our Fourth Attempt at optimization, we added more Neurons to a hidden layer, namely Layer1. We increased the neuron count from 80 to 100, and kept all other parameters the same. This resulted in 7,461 Trainable params with an accuracy score of 72.77.

![Attempt_4_More_Neurons_1](https://user-images.githubusercontent.com/84881187/137592832-ac04fee2-02b5-4fa0-88ee-482d4b67fd30.PNG)
![Attempt_4_More_Neurons_1_Accuracy](https://user-images.githubusercontent.com/84881187/137592851-ce656a34-d83a-4a09-8c40-4b2a14afe74e.PNG)


For the Fifth, and final attempt, we added more neurons to our second hidden layer, Layer2. We increased the neuron count from 30 to 50. This resulted in 7,621 Trainable params, with an accuracy score of 72.83.

![Attempt_5_More_Neurons_2](https://user-images.githubusercontent.com/84881187/137593031-5fbdab1e-baf4-4312-a3cf-3c4646ee0cfd.PNG)
![Attempt_5_More_Neurons_2_Accuracy](https://user-images.githubusercontent.com/84881187/137593034-7d4fdcf1-fc8e-42ec-ac52-c9084bd61a87.PNG)



## Project Summary

Unfortunately, our deep learning neural network model did not reach the target accuracy of 75%. Our average accuracy overall did not stray too far from our original model's accuracy of 72.65%, with all of our optimizations resulting in the 72% range themselves with slight decimal variance. 

Since we are using binary classification, it could be more beneficial to use a Supervised-Machine-Learning Model to analyze the data. Using a Random Forest Classifier, to combine a multitude of decision trees could help create a more accurate analysis with its number of estimators and depth with optimal speed that minimizes the data being overfitted. We could also drop more features to potentiall improve our optimization. Collecting more data in our dataset is always a great way to potentiall improve our analysis' accuracy. 
