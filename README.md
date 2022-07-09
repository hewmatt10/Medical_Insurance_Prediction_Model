## Medical Insurance Prediction Model

This program attempts to model one's medical insurance with a neural network.

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
