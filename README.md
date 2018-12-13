# Learning rate adaption during model training toward skin cancer classification
We will analyze the effect of learning rate adaption while training the models on the skin cancer dataset. Keras has a time-based learning rate schedule built in. The stochastic gradient descent optimization algorithm implementation in the SGD class has an argument called decay. This argument is used in the time-based learning rate decay schedule equation as follows:

LearningRate = LearningRate 1/1+(decayepoch)

When the decay argument is zero (the default), this has no effect on the learning rate (e.g.0.1).

LearningRate = 0.1 * 1/(1 + 0.0 * 1)

LearningRate = 0.1

When the decay argument is specied, it will decrease the learning rate from the previous epoch by the given fixed amount. You can create a nice default schedule by setting the decay value as follows:

Decay = LearningRate / Epochs 

Decay = 0.1 / 100 

Decay = 0.001

Lets see the time-based learning rate adaptation schedule in Keras. A small neural network model is constructed with a single hidden layer with 50 neurons and using the rectier activation function. The output layer has three neurons and uses the sigmoid activation function in order to output probability-like values. The learning rate for stochastic gradient descent has been set to a higher value of 0.1. The model is trained for 100 epochs and the decay argument has been set to 0.001, calculated as 0:1/100 . Additionally, it can be a good idea to use momentum when using an adaptive learning rate. In this case we use a momentum value of 0.9.

# Prerequisites:

Python 3.5

Keras 2.2.0

Tensorflow-GPU 1.9.0

Scikit-Learn

# Acknowledgment
Feel free to run the codes from the attached Jupyter Notebook. The codes can be used with your own custom datasets. All that you need is a CSV file containing the features and class labels. We believe the code would be of good value for the research community and request to kindly cite our study:
T. R. Thamizhvani, Suganthi Lakshmanan & R. Sivaramakrishnan (2018). Mobile application-based computer-aided diagnosis of skin tumours from dermal images, The Imaging Science Journal, 66:6, 382-391, DOI: 10.1080/13682199.2018.1492682
