### Machine Learning vs Deep Learning
Machine Learning	                                 Deep Learning
Broad field of AI	                            Subset of ML
Uses various learning algorithms        	    Uses multilayer neural networks
Often requires manual feature engineering   	Learns representations automatically
Can work well with smaller datasets	            Often benefits from large datasets
Usually requires less computation	            Often requires more computation
Examples: Decision Trees, SVM, K-Means         	Examples: CNN, RNN, Transformers

### 1 Deep Learning
Definition: Deep Learning is a subset of Machine Learning that uses multi-layered Artificial Neural Networks (ANNs) to learn complex patterns from large amounts of data and make predictions or decisions.

In simple words, Deep Learning allows computers to learn increasingly complex features from examples using neural networks.

Example: Recognizing a cat
Suppose you give a computer thousands of cat and dog images.

In traditional machine learning, developers may manually design features such as edges, textures or shapes before training a classifier.

In Deep Learning, a neural network can learn useful features automatically from the image pixels

### 2. What is an Artificial Neural Network?
Definition: An Artificial Neural Network (ANN) is a computational model composed of interconnected processing units called artificial neurons, organized into layers, that learn relationships between inputs and outputs by adjusting parameters such as weights and biases.

A neural network is loosely inspired by biological nervous systems, but it does not function exactly like a human brain.

### Structure of a Neural Network
A basic neural network consists of three types of layers:

1. Input Layer- Receives input features from the dataset.
Example:Study hours, Attendance, Previous exam score.

2. Hidden Layers - Process the input data and learn useful patterns using weights, biases and activation functions.
A neural network can contain one or multiple hidden layers.

3. Output Layer - Produces the final prediction.
Examples: Pass or Fail, Cat or Dog, Predicted house price.


## What makes a neural network deep?
A network with multiple hidden layers is generally called a Deep Neural Network (DNN).
- One hidden layer: Shallow neural network.
- Multiple hidden layers: Deep neural network.

### 3. Artificial Neuron — Building Block of a Neural Network
Definition: An artificial neuron is a mathematical processing unit that receives inputs, multiplies them by weights, adds a bias, applies an activation function and produces an output.

Every neuron performs two major operations:
1. Calculate the weighted sum.
2. Apply an activation function.

Mathematical Formula
First, calculate the weighted sum: z= w1x1+w2x2+ ... + wnxn+b

Then apply an activation function: a=f(z)

Where:
Symbol	Meaning
xi	Input feature
wi	Weight
b	Bias
z  Weighted sum
f	Activation function
a	Neuron output

## Let's understand every component.
3.1 Inputs
Definition: Inputs are numerical values provided to a neuron for processing.

3.2 Weights
Definition: A weight is a learnable parameter that determines how strongly an input contributes to the neuron's calculation

Weights can be positive, negative or zero.

3.3 Bias
Definition: Bias is a learnable parameter added to the weighted sum to allow the neuron to adjust its output independently of the input values.

Bias provides additional flexibility to the neuron.

3.4 Weighted Sum - 
This value is passed to the activation function.

Remember: Inputs are provided, weights and biases are learned, and the weighted sum is calculated.


#### 4. Activation Functions
Definition: An activation function is a mathematical function applied to the weighted sum of a neuron to determine its output. Nonlinear activation functions allow neural networks to learn complex relationships.

## Why do we need activation functions?
Imagine a neural network containing 10 layers.
If all layers perform only linear or affine transformations, combining these layers still produces an affine transformation.

Therefore, the network cannot learn many complex nonlinear relationships.
Activation functions introduce nonlinearity, allowing the network to learn more complicated patterns.


## There are four important activation functions you should understand.

4.1 Sigmoid Activation Function
Definition: Sigmoid is an activation function that converts any real-valued input into a value between 0 and 1. 

4.2 ReLU (Rectified Linear Unit)
Definition: ReLU is an activation function that returns zero for negative inputs and returns the input itself for positive inputs.

4.3 Tanh (Hyperbolic Tangent)
Definition: Tanh is an activation function that maps real-valued inputs to values between -1 and 1.

4.4 Softmax Activation Function
Definition: Softmax converts a vector of numerical scores (logits) into a probability distribution where all outputs sum to 1.

### 5 Forward Propagation
Definition: Forward Propagation is the process of passing input data through a neural network, layer by layer, to calculate its final prediction.

In simple words, forward propagation means moving data from the input layer towards the output layer.

The network predicts approximately 76.85% probability for the positive class.
Important: The predicted probability is not necessarily correct. We must compare it with the actual answer using a loss function.

## 6. How Does a Neural Network Learn?

We have learned how a neural network makes predictions.

Now the important question is:

How does the neural network improve its predictions?

It learns through a repeated training process involving three major components:
1. Loss Function.
2. Backpropagation.
3. Optimizer.
The complete training cycle is:


* 6.1 Loss Function
Definition: A loss function is a mathematical function that measures the difference between a model's prediction and the actual target value.

In simple words, loss tells us how wrong the model's prediction is according to a chosen mathematical measure.

## Step 1: Calculate Loss
Suppose:
- Actual label = 1.
- Predicted probability = 0.7685.
Using binary cross-entropy for a positive example: L=-log(0.7685) = approx0.263

The loss measures how far the prediction is from the desired result under the chosen loss function


### Step 2: Backpropagation

Definition: Backpropagation is an algorithm that efficiently calculates the gradients of a neural network's loss with respect to its weights and biases by applying the chain rule of calculus backward through the network.
In simple words: Backpropagation tells the network how each parameter contributed to the prediction error.


What is the Chain Rule?
The chain rule is a calculus rule used to differentiate a function composed of other functions.

Why is this important?
A neural network consists of many connected mathematical operations.
Backpropagation uses the chain rule to calculate gradients through these operations efficiently.

Step 3: Update Weights
An optimizer uses gradients to update model parameters.


Where:
- w = Weight.
- alpha= Learning rate.
- L = Loss.
This process is repeated during training.


Steps of Backpropagation
1. Perform forward propagation.
2. Calculate the prediction.
3. Calculate the loss.
4. Calculate gradients using the chain rule.
5. Pass gradients backward through the network.
6. Provide gradients to the optimizer.


### Remember the difference:
- Forward propagation calculates predictions.
- Backpropagation calculates gradients.
- Optimizer updates weights and biases.

### 6.3 Optimizer
Definition: An optimizer is an algorithm that updates the weights and biases of a neural network using gradients to minimize the loss function.

One basic optimization method is Gradient Descent.
    Wnew = Wold - aplph(dL/dw)

    Wnew: Updated weight.
    Wold: Previous weight.
    alpha: learning rate
    dL/dw : Gradient of loss with respect to weight.

* What is Learning Rate?
Definition: Learning rate is a hyperparameter that controls the size of parameter updates during training.
For example:
- Very high learning rate: Training may become unstable or overshoot.
- Very low learning rate: Training may become unnecessarily slow.
- Suitable learning rate: Helps the model converge effectively.


### Optimizer Comparison
Optimizer	                   Main idea
SGD	                        Gradient-based updates
Momentum	                Uses previous gradient information
RMSprop	                    Adapts learning rates using squared gradients
Adam	                    Combines momentum and adaptive learning rates

Interview question: What is Adam optimizer?
Adam is an adaptive optimization algorithm that combines first-moment and second-moment estimates of gradients to adjust model parameters efficiently.


### 7. Epoch, Batch and Iteration
These terms describe how training data is processed.

7.1 Epoch
Definition: An epoch is one complete pass through the entire training dataset.

7.2 Batch
Definition: A batch is a subset of training examples processed together during a training step.

7.3 Batch Size
Definition: Batch size is the number of training examples processed in one batch.

7.4 Iteration
Definition: An iteration is one training step, typically involving processing one batch and performing one optimizer update.


Example:
- Training dataset = 1,000 examples.
- Batch size = 100.
- Epochs = 10.
Then:
Batches per epoch=1000/100=10

Assuming every batch causes one update: Total iterations =10*10=100

Term	         Meaning
Epoch	        Full dataset pass
Batch size	    Examples processed together
Iteration	    One optimization update
Learning rate	Parameter update step size


### 9. Common Problems During Neural Network Training
9.1 Overfitting
Definition: Overfitting occurs when a model learns the training data too closely, including noise and unnecessary details, and consequently performs poorly on unseen data.

Example: A student memorizes all practice questions but cannot solve new questions in the examination.

9.2 Underfitting
Definition: Underfitting occurs when a model is too simple, insufficiently trained or otherwise unable to capture important patterns in the training data.

Example:A student has not understood the basic concepts and cannot solve either practice questions or new examination questions.


### Overfitting vs Underfitting
Overfitting	                                     Underfitting
Learns training data too closely        	Fails to learn important patterns
Low training loss	                        High training loss
High validation loss                       	High validation loss
Poor generalization	                        Poor learning and generalization

9.3 Vanishing Gradient Problem
Definition: Vanishing gradients occur when gradients become extremely small while propagating backward through a neural network, making earlier layers difficult to train.

Why does it happen?
During backpropagation, gradients are multiplied through multiple layers. If these multiplications repeatedly involve small values, gradients can shrink towards zero.

9.4 Exploding Gradient Problem
Definition: Exploding gradients occur when gradients become excessively large during backpropagation, causing unstable and excessively large parameter updates.


### Final Revision
Deep Learning

Uses neural networks with multiple layers to learn complex patterns.

Artificial Neuron a=f(sum(wixi)+b)


Training Process

Input → Forward Propagation → Prediction → Loss → Backpropagation → Parameter Update.

Activation Functions
- ReLU: Common in hidden layers.
- Sigmoid: Binary classification output.
- Tanh: Outputs between -1 and 1.
- Softmax: Probability distribution over multiple classes.

Training Terminology
- Epoch: One complete pass through data.
- Batch: Group of training examples.
- Iteration: One optimization update.


### Concept	What you will learn
Regularization	        How to prevent overfitting
Dropout             	How randomly disabling neurons helps generalization
Batch Normalization 	How normalizing intermediate activations can stabilize training
Weight Initialization	How initial weights are selected
CNN	                    Neural networks for image and spatial data
RNN                 	Neural networks for sequential data
LSTM and GRU	        Handling longer-term dependencies in sequences
Attention Mechanism	    How models focus on relevant information
Transformers	        Architecture behind modern language models
Embeddings	            Representing information as numerical vectors



### Neural network Architecture
Our goal is to understand the complete journey:
AI → ML → Deep Learning → Neural Network Architectures → Generative AI → LLMs → RAG → Agentic AI.

## What are Deep Learning Architectures?
Definition: Deep Learning architectures are computational structures made up of interconnected artificial neurons and layers that learn patterns and relationships from data to perform tasks such as classification, prediction, recognition and content generation.

Different neural network architectures are designed to handle different types of data

Architecture	            Main purpose	            Example
ANN / MLP	                General numerical data	    House price prediction
CNN	                        Image processing	        Cat and dog recognition
RNN                     	Sequential data	            Text processing
LSTM	                    Long-term sequence learning 	Speech recognition
GRU	                        Efficient sequence learning	    Time-series prediction
Transformer                	Understanding relationships in sequences	ChatGPT


## 1. ANN / MLP (Artificial Neural Network)
An Artificial Neural Network (ANN) is a computational model inspired by the human brain, consisting of interconnected artificial neurons arranged in layers that learn patterns by adjusting weights and biases during training.

An MLP (Multilayer Perceptron) is a type of feedforward ANN containing one or more hidden layers, typically with fully connected neurons.

An ANN generally consists of three types of layers:
1. Input Layer: Receives input features from the dataset.
2. Hidden Layers: Process information and learn patterns.
3. Output Layer: Produces the final prediction.

## Important concepts
1. Neuron: A basic computational unit that receives inputs, applies weights and bias, and produces an output through an activation function.

2. Weight: A learnable numerical value that determines the influence of an input on a neuron.

3. Bias: A learnable numerical value added to the weighted sum to help the neuron adjust its output.

4. Activation Function: A mathematical function applied to a neuron's weighted input to introduce non-linearity into a neural network.

Important activation functions:
Function	Purpose
ReLU	Converts negative values to zero
Sigmoid	Maps values between 0 and 1
Tanh	Maps values between -1 and 1
Softmax	Converts output scores into probabilities

5. Forward Propagation: The process of passing input data through the network to calculate an output.

6. Backpropagation: The process of calculating gradients of the loss with respect to model parameters using the chain rule.

7. Loss Function: A mathematical function that measures the difference between predicted output and actual output.

8. Gradient Descent: An optimization algorithm that updates model parameters to reduce the loss.
Working of ANN
Input \rightarrow Hidden\ Layers \rightarrow Output


1. Input data enters the network.
2. Neurons calculate weighted sums.
3. Activation functions process the values.
4. The network produces predictions.
5. Loss function measures prediction error.
6. Backpropagation calculates gradients.
7. Optimizer updates weights and biases. 
ex - House price prediction, fraud detection

### 2 CNN (Convolutional Neural Network)
A Convolutional Neural Network (CNN) is a specialized Deep Learning architecture primarily designed to process grid-like data, especially images, by automatically extracting spatial features using convolution operations and learnable filters.

Why do we need CNN?
An image consists of pixels arranged in rows and columns.

CNN learns visual patterns in a hierarchical manner:
- Early layers: Edges and lines.
- Middle layers: Shapes and textures.
- Deeper layers: Complex objects and features.

1. Convolution: A mathematical operation in which a filter moves across an input to extract local features.

2. Filter / Kernel: A small learnable matrix of numerical values used to detect patterns such as edges, corners and textures.

Example of a 3 × 3 kernel:
\[
\begin{bmatrix}
1&0&-1\\
1&0&-1\\
1&0&-1
\end{bmatrix}
\]

3. Feature Map: The output produced when a filter is applied to an input through convolution.

4. Stride: The number of positions a filter moves at each step.
- Stride 1: Moves one position.
- Stride 2: Moves two positions.
5. Padding: Adding extra values, usually zeros, around the input boundary to control output dimensions and preserve edge information.

6. Pooling: A downsampling operation that reduces the spatial dimensions of feature maps.

Types:
- Max Pooling: Selects the maximum value.
- Average Pooling: Calculates the average value.
7. Receptive Field: The region of the original input that influences a particular neuron or output feature.

8. Flattening: Converts multidimensional feature maps into a one-dimensional vector for subsequent processing. Some modern CNNs instead use global pooling.
CNN architecture