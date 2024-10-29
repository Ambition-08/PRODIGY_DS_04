
# # Social Media Sentiment Analysis
## Introduction

This project analyzes sentiment patterns in social media data to uncover public opinion and attitudes toward specific topics or brands. Using state-of-the-art Natural Language Processing (NLP) techniques, such as TF-IDF and sentiment analysis with VADER, this project provides insights into positive, negative, and neutral sentiments expressed in social media posts. The results are visualized to help stakeholders understand audience perceptions and track sentiment trends over time. This repository includes the code, dataset, and detailed documentation to guide you through the analysis process.

## Table of Contents
-[Features](#features)
   # Social Media Sentiment Analysis
   Analyze sentiment patterns in social media data to understand public opinion on specific topics or brands.

   ## Features
   - Sentiment EDA [Go to EDA_Twitter.ipynb section](#EDA_Twitter.ipynb)
   - TF-IDF for keyword extraction
   - Visualization of sentiment trends
   - [

   ## Installation

## Getting Started
Follow the instructions in the setup guide to install dependencies and run the analysis. Check out the examples provided for guidance on replicating the analysis or customizing it for your own data.

To run this repo, be sure to install the following environment and library:

**Python**: 3.11.8
- **TensorFlow**: 2.18.0
- **Keras**: 3.6.0
- **Pandas**: 2.2.2
- **NumPy**: 1.26.4
- **h5py**: 3.12.1
- **scikit-learn**: 1.5.2

File Illustration
There are currently three different Analysis:

    LSTM.py
    GRU.py
    CNN.py (1 dimensional CNN)

The validation result is plotted in:

- Exploratory data analysis on Twitter data [EDA_Twitter.ipynb](./EDA_Twitter.ipynb): 
- [Entity-Wise Sentiment Analysis.ipynb](./Entity-Wise%20Sentiment%20Analysis.ipynb): Jupyter notebook for performing sentiment analysis by entity.
    Plot_GRU.ipynb
    Plot_CNN.ipynb

Data is collected from poloniex and parse to h5py file:

   [twitter_training.csv](./twitter_training.csv): or you can access the dataset used in this project on Kaggle: [Twitter Entity Sentiment Analysis Dataset](https://www.kaggle.com/datasets/jp797498e/twitter-entity-sentiment-analysis).

# Sentiment Analysis Dataset

This repository contains a dataset for sentiment analysis, focusing on user sentiments expressed about the game "Borderlands." The dataset includes various attributes that capture user opinions.

## Dataset Description

Sample of the data set:

| iD  | entity       | sentiment | text                                  |
|-----|--------------|-----------|---------------------------------------|
| 0   | 2401         | Borderlands| Positive  | I'm getting Borderlands murder.       |
| 1   | 2401         | Borderlands| Positive  | I'm coming borders, I kill all.      |
| 2   | 2401         | Borderlands| Positive  | I'm getting Borderlands, kill all.   |
| 3   | 2401         | Borderlands| Positive  | I'm coming Borderlands, murder all.  |
| 4   | 2401         | Borderlands| Positive  | I'm getting Borderlands 2, murder all.|

### Column Definitions
- **iD**: A unique identifier for each entry.
- **entity**: The entity being referred to, as example, "TomClancysRainbowSix, MaddenNFL, Borderlands.LeagueOfLegends,CallOfDuty,Verizon,CallOfDutyBlackopsColdWar,Facebook...."
- **sentiment**: The sentiment expressed in the text (Positive,Neutral,Negative).
- **text**: The user-generated text reflecting their opinion.
## Usage

This dataset can be used for various applications, including:
## Project Files

This repository contains the following files: First be sure to run [twitter_training.csv](./twitter_training.csv): CSV file containing the training data for sentiment analysis.

- [Negative Sentiment Words.png](./Negative%20Sentiment%20Words.png): Image showing negative sentiment words.
- [Positive Sentiment Words.png](./Positive%20Sentiment%20Words.png): Image showing positive sentiment words.
- [Sentiment Distribution.png](./Sentiment%20Distribution.png): Image displaying the sentiment distribution.
- [TF-IDF for keyword extraction.ipynb](./TF-IDF%20for%20keyword%20extraction.ipynb): Jupyter notebook for TF-IDF keyword extraction.
- [libraries.ipynb](./libraries.ipynb): Jupyter notebook listing libraries used in the project.
- [loading_data_And_Data_Cleaning.ipynb](./loading_data_And_Data_Cleaning.ipynb): Jupyter notebook for loading and cleaning the data.
- [outputEntity-Wise Sentiment Analysis.png](./outputEntity-Wise%20Sentiment%20Analysis.png): Output image from the entity-wise sentiment analysis.
-

- Sentiment analysis
- Natural language processing tasks
- Machine learning model training

## How to Contribute

If you'd like to contribute to this dataset or improve the analysis, feel free to open a pull request or submit issues.

## License

This dataset is available under the [MIT License](LICENSE).



Run

To run the prediction model, select one of the model. For instance,

python CNN.py

To run iPython file, you need to run jupyter notebook

jupyter notebook
Jupyter notebook for exploratory data analysis on Twitter data.
## Project Files

This repository contains the following files:

- Jupyter notebook for exploratory data analysis on Twitter data.[EDA_Twitter.ipynb](./EDA_Twitter.ipynb): 
- [Entity-Wise Sentiment Analysis.ipynb](./Entity-Wise%20Sentiment%20Analysis.ipynb): Jupyter notebook for performing sentiment analysis by entity.
- [Negative Sentiment Words.png](./Negative%20Sentiment%20Words.png): Image showing negative sentiment words.
- [Positive Sentiment Words.png](./Positive%20Sentiment%20Words.png): Image showing positive sentiment words.
- [README.md](./README.md): This file.
- [Sentiment Distribution.png](./Sentiment%20Distribution.png): Image displaying the sentiment distribution.
- [TF-IDF for keyword extraction.ipynb](./TF-IDF%20for%20keyword%20extraction.ipynb): Jupyter notebook for TF-IDF keyword extraction.
- [libraries.ipynb](./libraries.ipynb): Jupyter notebook listing libraries used in the project.
- [loading_data_And_Data_Cleaning.ipynb](./loading_data_And_Data_Cleaning.ipynb): Jupyter notebook for loading and cleaning the data.
- [outputEntity-Wise Sentiment Analysis.png](./outputEntity-Wise%20Sentiment%20Analysis.png): Output image from the entity-wise sentiment analysis.
- [twitter_training.csv](./twitter_training.csv): CSV file containing the training data for sentiment analysis.



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
