# PRODIGY_DS_04
## Understanding Public Opinion and Attitudes towards -Analyze and Visualise Sentiments in Social Media


### Introduction

This repository leverages cutting-edge Natural Language Processing (NLP) techniques to analyze and visualize sentiment patterns in social media data, providing valuable insights into public opinion on specific topics or brands. By utilizing advanced models like sentiment analysis with VADER and TF-IDF, this project aims to identify positive, negative, and neutral sentiments expressed in posts. This approach allows businesses, researchers, and analysts to better understand audience attitudes, track sentiment trends over time, and make data-driven decisions. For more details, please refer to the accompanying documentation and blog post.

Getting Started

To run this repo, be sure to install the following environment and library:

    Python 3.8
    Tensorflow=1.2.0
    Keras=2.1.1
    Pandas=0.20.3
    Numpy=1.13.3
    h5py=2.7.0
    sklearn=0.19.1

File Illustration
There are currently three different models:

    LSTM.py
    GRU.py
    CNN.py (1 dimensional CNN)

The validation result is plotted in:

    Plot_LSTM.ipynb
    Plot_GRU.ipynb
    Plot_CNN.ipynb

Data is collected from 

    DataCollection.ipynb
    PastSampler.ipynb

Run

To run the prediction model, select one of the model. For instance,

python CNN.py

To run iPython file, you need to run jupyter notebook

jupyter notebook

Be sure to run DataCollection.ipynb and PastSampler.ipynb first to create database for training models.
Input & Output & Loss

The input consists of a list of past Bitcoin data with step size of 256. The output is the predicted value of the future data with step size of 16. Note that since the data is ticked every five minutes, the input data spans over the past 1280 minutes, while the output cover the future 80 minutes. The datas are scaled with MinMaxScaler provided by sklearn over the entire dataset. The loss is defined as Mean Square Error (MSE).
Result
Model 	#Layers 	Activation 	Validation Loss 	Test Loss (Scale Inverted)
CNN 	2 	ReLU 	0.00029 	114308
CNN 	2 	Leaky ReLU 	0.00029 	115525
CNN 	3 	ReLU 	0.00029 	201718
CNN 	3 	Leaky ReLU 	0.00028 	108700
CNN 	4 	ReLU 	0.00030 	117947
CNN 	4 	Leaky ReLU 	0.03217 	12356304
LSTM 	1 	tanh + ReLU 	0.00007 	26649
LSTM 	1 	tanh + Leaky ReLU 	0.00004 	15364
GRU 	1 	tanh + ReLU 	0.00004 	17667
GRU 	1 	tanh + Leaky ReLU 	0.00004 	15474
Baseline (Lag) 	- 	- 	- 	19122
Linear Regression 	- 	- 	- 	19789

Each row of the above table is the model that derives the best validation loss from the total 100 training epochs. From the above result, we can observe that LeakyReLU always seems to yield better loss compared to regular ReLU. However, 4-layered CNN with Leaky ReLU as activation function creates a large validation loss, this can due to wrong deployment of model which might require re-validation. CNN model can be trained very fast (2 seconds/ epoch with GPU), with slightly worse performance than LSTM and GRU. The best model seems to be LSTM with tanh and Leaky ReLU as activation function, though 3-layered CNN seems to be better in capturing local temporal dependency of data.

LSTM with tanh and Leaky ReLu as activation function.

3-layered CNN with Leaky ReLu as activation function.

Baseline

Linear Regression
Update
Regularization has been done, which can be viewed in PlotRegularization.ipynb.
