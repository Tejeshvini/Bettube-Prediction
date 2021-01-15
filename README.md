# Bettube-Prediction
Coding Task for recruitment

Since the objective of this assessment is prediction, I've used the ML model that's relatively better at it - Neural Networks.

Few key things to note

* I have used one hot encoding for categorical variables like Home Team, Away Team etc and Label encoding would an an order to it.Therefore, introducing bias.
* I've used one hot encoding for the response variable - Brownlow votes, and used a softmax function with 4 neurons in the output layer. Hence, the output from the neural network is an array of probabilities of the observation belonging to each class - 0,1,2,3.
* I had initially tried building a Logistic Regression model with l2 penalty (lasso regularozation) to reduce the number of parameters which had increased due to one hot encoding. However, I did not proceed with it as neural network seemed to work better.

## Results

* I've used 2013-2016 for training and validation of the model. 85% of this set was used for training and 15% for validation. 93% validation accuracy was acheived with 20 epochs.
* The performance of the model on the test set (2016-2019) was 94% accurate.
* As seen in the confusion matrix, the model predicts no oberservations in 1 or 2 class labels (This could be because most of the observations are in class 0) 