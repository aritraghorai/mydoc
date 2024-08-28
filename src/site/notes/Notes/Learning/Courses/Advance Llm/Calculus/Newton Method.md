---
{"dg-publish":true,"permalink":"/notes/learning/courses/advance-llm/calculus/newton-method/","title":"Newton Method"}
---

## Gradient Descent 
Gradient Descent is an optimization algorithm used to minimize the loss function in machine learning and statistical models. It helps find the optimal parameters (weights) for a model by iteratively adjusting them to reduce the error between predicted and actual values.

### How Gradient Descent Works:

1. **Initialization**: Start with initial random values for the model parameters (weights). 

2. **Calculate the Loss**: Compute the loss (or cost) function, which measures how well the model with current parameters fits the data. Common loss functions include Mean Squared Error (MSE) for regression and Cross-Entropy Loss for classification.

3. **Compute the Gradient**: Calculate the gradient of the loss function with respect to each parameter. The gradient is a vector of partial derivatives, indicating the direction and rate of the steepest increase in loss.

4. **Update Parameters**: Adjust the parameters in the opposite direction of the gradient to reduce the loss. This is done using the update rule:
$$
   \theta := \theta - \alpha \cdot \nabla J(\theta)
   
$$
   where:
   -  \( \theta \) represents the model parameters.
   - \( \alpha \) is the learning rate, a small positive number that controls the step size.
   - \( \nabla J(\theta) \) is the gradient of the loss function with respect to the parameters.

5. **Repeat**: Repeat the steps of calculating the loss, computing the gradient, and updating the parameters until convergence, i.e., when the changes in the loss function or parameters become negligibly small or after a predetermined number of iterations.

### Types of Gradient Descent:

1. **Batch Gradient Descent**: Uses the entire training dataset to compute the gradient. This provides a stable convergence path but can be computationally expensive, especially for large datasets.

2. **Stochastic Gradient Descent (SGD)**: Uses a single randomly selected training example to compute the gradient and update the parameters. This makes the updates more frequent and introduces noise, which can help escape local minima but may lead to less stable convergence.

3. **Mini-Batch Gradient Descent**: A compromise between batch and stochastic gradient descent. It uses a small subset (mini-batch) of the training dataset to compute the gradient and update the parameters. This balances the efficiency and convergence stability of batch and stochastic methods.

### Key Concepts:

- **Learning Rate (\( \alpha \))**: A critical hyperparameter that determines the size of the steps taken towards the minimum. A too-large learning rate can cause the algorithm to overshoot the minimum, while a too-small learning rate can lead to slow convergence.

- **Convergence**: The point at which further updates do not significantly change the parameters, indicating that the minimum of the loss function has been reached.

- **Local vs. Global Minimum**: For non-convex functions, gradient descent may converge to a local minimum, which may not be the global minimum. Various strategies, such as using different starting points or SGD, can help in finding a better minimum.

### Applications:

Gradient Descent is widely used in training various machine learning models, including linear regression, logistic regression, neural networks, and deep learning models. Its efficiency and simplicity make it a fundamental technique for optimization in machine learning.

## Neural Network Basics
### Basic Neural Network
```
The image illustrates a **single-layer neural network model** known as a **perceptron**. It shows two inputs, ( x_1 ) and ( x_2 ), each multiplied by corresponding weights, ( w_1 ) and ( w_2 ), and summed with a bias term ( b ) to produce an output ( \hat{y} ). The equation representing this process is ( \hat{y} = w_1 \cdot x_1 + w_2 \cdot x_2 + b ).

The text on the right side of the image states “Regression With a Perceptron,” indicating the perceptron is used for regression tasks. The objective is to find weights and bias that optimize predictions, aiming to reduce prediction errors.

This visual representation helps in understanding the basic functioning of a neural network in predictive modelling tasks.
```
![Newton Method.png](/img/user/assets/Newton%20Method.png)

### Loss Function
![Newton Method Loss function.png](/img/user/assets/Newton%20Method%20Loss%20function.png)

### With Activation Function
![Newton Method Activation Funtion.png](/img/user/assets/Newton%20Method%20Activation%20Funtion.png)

![Newton Method-1.png](/img/user/assets/Newton%20Method-1.png)

