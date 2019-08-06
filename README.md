# Face-recognition
Y.T Tao and B.H Chen's learning project of face recognition.

## First step

A **label** is the thing we're predicting (y). A **feature** is an input variable (x). An example is a particular instance of data, **x**. There are two kinds of examples: 
- labeled examples: A labeled example includes both feature(s) and the label.
- unlabeled examples: An unlabeled example contains features but not the label.
We use labeled examples to train the model and use use that model to predict the label on unlabeled examples.

A **model** defines the relationship between features and label. 

**Training** means creating or learning the model. Training a model simply means learning (determining) good values for all the weights and the bias from labeled examples.

**Inference** means applying the trained model to unlabeled examples.

A **regression** model predicts continuous values while a **classification** model predicts discrete values.

**Loss** is a number indicating how bad the model's prediction was on a single example.
