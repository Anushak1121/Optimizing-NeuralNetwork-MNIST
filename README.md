The MNIST (Modified National Institute of Standards and Technology) dataset is one of the most popular datasets used in machine learning and deep learning
It contains 70,000 handwritten images of the digits from 0 to 9
Each image is of 28x28 dimension and is represented using pixels values between 0 and 255, where
0 stands for black
255 stands for white

We used following approach to check model performance in each case.

Baseline Model Performance:
A baseline model with two hidden layers having ReLU and tanh activations, using stochastic gradient descent with a batch size of 32, and run for 50 epochs, yielded good overall results (99.7% train accuracy and 97.6% validation accuracy).
We observed initial rapid improvement in loss and accuracy, followed by divergence between the training and validation sets after the initial few epochs.

Effect of Momentum:
Introduction of momentum leads to a quicker decrease in loss.
However, higher values of momentum may result in the model oscillating around the minimum.

Effect of Learning Rate:
A lower learning rate (1e-4) reduces the oscillations in loss and yields a more generalized performance.
However, using even lower learning rates (like 1e-5) would require more epochs for the model to yield desirable results.

Adam vs SGD with Momentum:
The use of Adam helps in tackling the problems listed above, and with the right learning rate, Adam shows improved convergence.
Further reduction of the learning rate for Adam (1e-5) leads to smoother convergence but slower model training.

Effect of Regularization:
Dropout with lower ratios (20%) shows no major improvement, but increasing the dropout rate (30%, 50%) reduces overfitting.
The use of batch normalization yields slightly lower performance than dropout.
The combination of dropout and batch normalization shows no major improvement compared to dropout with a moderate ratio (30%).

Effect of Weight Initialization:
Using weight initialization techniques that are preferable for certain activation functions (like ReLU) does not yield any major performance gain.
