## Medical Insurance Prediction Model

This program attempts to model one's medical insurance with a neural network.
The dataset used is from: https://github.com/stedy/Machine-Learning-with-R-datasets/blob/master/insurance.csv

The input parameters include:
* Age
* Sex
* BMI
* Number of children
* Smoking status
* Region of city.

While not excessive, these input parameters provide a decent dataset to train the model.

The output parameters is only the charges for the medical insurance, making this a regression problem.

Through tweaking the neural network's various characteristics, the optimal model was determined to have:
* 4 hidden layers 
  * 50 in the first hidden layer
  * 20 in the second hidden layer
  * 10 in the third hidden layer
  * 10 in the fourth hidden layer
* Huber loss computer
* Adamax optimizer
* Patience of 30
* 10000 epochs
* Batch size of 20

The model achieved an mean absolute error of $1226.97, and a mean absolute percentage error of 5.4062%. The mean absolute percentage error is not outstanding, but it is acceptable. However, the mean absolute error is a huge deviation from the actual value. Most people would not want their predicted insurance to be over $1000 in difference compared to their actual. Ideally, this number should be shrunk to < $100 for the model to be valid. After plotting both y_test and y_pred, an interesting phenomenon arises. Most of the predictions are extremely close to their actual value, however, there are select ones where the model's prediction are severely off. This could be due to the inconsistency of the model, the low row number of the dataset, or that parts of the input data have minimal correlation to medical insurance in the first place. This phenomenon means that the model can be used in practice to predict one's medical insurance given several parameters, working most of the time. However, the model will be very inconsistent due to the occasional huge deviation. Overall, the model's performance was mediocre, being able to predict decent results but is sometimes inconsistent and predicts highly deviated results.
