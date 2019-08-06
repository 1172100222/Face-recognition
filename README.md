# Face-recognition
Y.T Tao and B.H Chen's learning project of face recognition.

## Preparation
A **label** is the thing we're predicting (y). A **feature** is an input variable (x). An example is a particular instance of data, **x**. There are two kinds of examples: 
- labeled examples: A labeled example includes both feature(s) and the label.
- unlabeled examples: An unlabeled example contains features but not the label.
We use labeled examples to train the model and use use that model to predict the label on unlabeled examples.

A **model** defines the relationship between features and label. 

**Training** means creating or learning the model. Training a model simply means learning (determining) good values for all the weights and the bias from labeled examples.

**Inference** means applying the trained model to unlabeled examples.

A **regression** model predicts continuous values while a **classification** model predicts discrete values.

**Loss** is a number indicating how bad the model's prediction was on a single example.

### Gradient Descent
First pick starting values for the weights, then calculates the gradient of the loss curve at the starting point. The gradient descent algorithm takes a step in the direction of the negative gradient in order to reduce loss as quickly as possible. Then add some fraction of the gradient's magnitude to the starting point to determine the next point along the loss function curve. The gradient descent then repeats this process until overall loss stops changing or at least changes extremely slowly.  When that happens, we say that the model has **converged**.

Note that gradient descent algorithms multiply the gradient by a scalar known as the learning rate (also sometimes called step size) to determine the next point. The ideal learning rate in one-dimension is the inverse of the second derivative of f(x) at x; the ideal learning rate for 2 or more dimensions is the inverse of the Hessian. (**Here we assume the resulting plot of loss is convex.**)

In gradient descent, a **batch** is the total number of examples we use to calculate the gradient in a single iteration. When working at very large scale data sets, a very large batch may cause even a single iteration to take a very long time to compute. So we often choose **Stochastic Gradient Descent** (SGD, it uses only a single example (a batch size of 1) per iteration) or **Mini-batch Stochastic Gradient Descent** (mini-batch SGD, a mini-batch is typically between 10 and 1,000 examples, chosen at random.) rather than *Full Gradient Descent.*

Given enough iterations, SGD works but is very noisy. 

Mini-batch SGD reduces the amount of noise in SGD but is still more efficient than full-batch.
