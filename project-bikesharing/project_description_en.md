# Bike Sharing Prediction Project Analysis

## Project Overview

This project aims to build a neural network to predict future bike rental numbers using bike sharing data. The implemented neural network is a basic feedforward network consisting of an input layer, hidden layer, and output layer.

## Neural Network Fundamentals

### Neural Network Structure
Neural networks are computational models inspired by the biological neurons in the human brain. A basic neural network consists of the following elements:

1. **Neurons (Nodes)**: Basic computational units that receive inputs, process them, and generate outputs through activation functions.
2. **Layers**:
   - **Input Layer**: Where the data is initially fed into the network
   - **Hidden Layer(s)**: Located between input and output layers, responsible for learning complex patterns
   - **Output Layer**: Produces the final prediction values
3. **Weights**: Parameters that represent the strength of connections between neurons
4. **Biases**: Parameters that adjust the activation threshold of each neuron
5. **Activation Functions**: Non-linear functions (sigmoid, ReLU, tanh, etc.) that transform inputs to outputs

### Forward Propagation
Forward propagation is the process by which input data passes through the network to generate outputs:

1. **Mathematical Representation**:
   - Hidden layer input: $z^{[1]} = W^{[1]} \cdot X + b^{[1]}$
   - Hidden layer activation: $a^{[1]} = \sigma(z^{[1]})$
   - Output layer input: $z^{[2]} = W^{[2]} \cdot a^{[1]} + b^{[2]}$
   - Output layer activation: $a^{[2]} = f(z^{[2]})$

   Where $W$ represents weight matrices, $b$ represents bias vectors, $\sigma$ is the activation function (sigmoid function in this project), and $f$ is the output layer activation function (linear function in this project).

2. **Computational Steps**:
   - For each layer, compute the matrix product of the previous layer's output and current layer's weights
   - Add the bias
   - Apply the activation function to generate the output
   - Repeat until the final layer

### Backpropagation
Backpropagation is the process used to update weights to minimize prediction errors:

1. **Computational Flow**:
   - Calculate output error: $L = \frac{1}{2}(y - \hat{y})^2$ (for squared error)
   - Output layer error: $\delta^{[2]} = -(y - \hat{y}) \cdot f'(z^{[2]})$
   - Backpropagate error to hidden layer: $\delta^{[1]} = (W^{[2]})^T \cdot \delta^{[2]} \cdot \sigma'(z^{[1]})$
   - Gradients with respect to weights: $\nabla_{W^{[1]}} L = \delta^{[1]} \cdot X^T$, $\nabla_{W^{[2]}} L = \delta^{[2]} \cdot (a^{[1]})^T$
   - Gradients with respect to biases: $\nabla_{b^{[1]}} L = \delta^{[1]}$, $\nabla_{b^{[2]}} L = \delta^{[2]}$

2. **Chain Rule**:
   Backpropagation is based on the chain rule of calculus. The gradient of the error with respect to parameters (weights and biases) at each layer is calculated using the errors from subsequent layers.

### Weight Update
Gradient descent is used to update weights and biases based on the calculated gradients:

1. **Gradient Descent**:
   - Weight update: $W^{[l]} = W^{[l]} - \alpha \cdot \nabla_{W^{[l]}} L$
   - Bias update: $b^{[l]} = b^{[l]} - \alpha \cdot \nabla_{b^{[l]}} L$

   Where $\alpha$ is the learning rate that controls the magnitude of updates.

2. **Stochastic Gradient Descent (SGD)**:
   In this project, gradients are computed and weights are updated using small batches (128 samples) instead of the entire dataset. This improves computational efficiency and potentially helps avoid local optima.

3. **Role of Learning Rate**:
   - Too large learning rate: May cause unstable convergence or divergence
   - Too small learning rate: May lead to very slow convergence
   - Choosing an appropriate learning rate (0.5 in this project) is crucial

## Dataset

The dataset used in this project contains hourly bike rental data with the following features:

- Time-related information such as hour of day, day of week, month, and season
- Environmental information such as weather conditions, temperature, humidity, and wind speed
- Number of casual users, registered users, and total users

The data is normalized, and categorical variables are converted to dummy variables. The dataset is split into training, validation, and test sets.

## Neural Network Implementation

The neural network has the following characteristics:

- **Input Layer**: Number of nodes corresponding to the number of features
- **Hidden Layer**: 10 nodes (set as a hyperparameter)
- **Output Layer**: 1 node (predicted bike rental count)
- **Activation Functions**: Sigmoid function for the hidden layer, linear function (f(x)=x) for the output layer
- **Learning Rate**: 0.5 (set as a hyperparameter)
- **Number of Iterations**: 4000 (set as a hyperparameter)

## Implementation Details

The main implementation of the neural network is included in the `my_answers.py` file, which contains the following key methods:

1. **forward_pass_train**: Implements forward propagation during training
2. **backpropagation**: Implements error backpropagation and calculates delta weights
3. **update_weights**: Implements weight updates using gradient descent
4. **run**: Implements forward propagation (prediction) during testing

## Training Process

The network is trained using Stochastic Gradient Descent (SGD). In each iteration, 128 samples are randomly selected from the training data, and these are used to update the weights. During training, both training loss and validation loss are tracked to monitor overfitting.

## Evaluation Method

The model is evaluated using the test dataset. Predicted values are compared with actual values, and the model's performance is visualized. Mean Squared Error (MSE) is used as the evaluation metric.

## Important Notes

When running the code, attention must be paid to the version of Pandas being used. The current code uses the `.ix` method, which has been deprecated in newer versions of Pandas. Instead, `.loc` or `.iloc` should be used.

## Summary

This project serves as a good exercise for understanding and implementing basic concepts of deep learning. It allows learning the fundamentals of deep learning, such as the basic structure of neural networks, forward propagation and error backpropagation algorithms, and weight update methods. By using real data, it also deepens understanding of data preprocessing and evaluation methods.
