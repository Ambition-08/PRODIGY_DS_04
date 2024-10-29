
# # Social Media Sentiment Analysis
## Introduction

This project analyzes sentiment patterns in social media data to uncover public opinion and attitudes toward specific topics or brands. Using state-of-the-art Natural Language Processing (NLP) techniques, such as TF-IDF and sentiment analysis with VADER, this project provides insights into positive, negative, and neutral sentiments expressed in social media posts. The results are visualized to help stakeholders understand audience perceptions and track sentiment trends over time. This repository includes the code, dataset, and detailed documentation to guide you through the analysis process.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Data_Collection](#data_collection)
- [Dataset_Description](#dataset_description)
- [Column_Definitions](#column_definitions)
- [Data cleaning](#data_cleaning)
- [Data_Analysis](#data_analysis)
- [Sample_Outputs](#sample_outputs)
- [ License](#license)
  
## Features
- EDA_Twitter
- Entity-Wise Sentiment Analysis
- Sentiment Distribution
- TF-IDF for keyword extraction

## Getting Started
###  Installation
Follow the instructions in the setup guide to install dependencies and run the analysis. Check out the examples provided for guidance on replicating the analysis or customizing it for your own data.

To run this repo, be sure to install the following environment and library:

**Python**: 3.11.8
- **TensorFlow**: 2.18.0
- **Keras**: 3.6.0
- **Pandas**: 2.2.2
- **NumPy**: 1.26.4
- **h5py**: 3.12.1
- **scikit-learn**: 1.5.2
And also the **important libraries** for this project are
- [libraries.ipynb](./libraries.ipynb): Jupyter notebook listing libraries used in the project.

## File_Illustration
### Data_Collection
Data is collected from poloniex and parse to h5py file:
You can use the data uploaded in this repository [twitter_training.csv](./twitter_training.csv): or you can access the dataset used in this project on Kaggle: [Twitter Entity Sentiment Analysis Dataset](https://www.kaggle.com/datasets/jp797498e/twitter-entity-sentiment-analysis).

## Dataset_Description

Sample of the data set:

| iD  | entity       | sentiment | text                                  |
|-----|--------------|-----------|---------------------------------------|
| 0   | 2401         | Borderlands| Positive  | I'm getting Borderlands murder.       |
| 1   | 2401         | Borderlands| Positive  | I'm coming borders, I kill all.      |
| 2   | 2401         | Borderlands| Positive  | I'm getting Borderlands, kill all.   |
| 3   | 2401         | Borderlands| Positive  | I'm coming Borderlands, murder all.  |
| 4   | 2401         | Borderlands| Positive  | I'm getting Borderlands 2, murder all.|

### Column_Definitions
- **iD**: A unique identifier for each entry.
- **entity**: The entity being referred to, as example, "TomClancysRainbowSix, MaddenNFL, Borderlands.LeagueOfLegends,CallOfDuty,Verizon,CallOfDutyBlackopsColdWar,Facebook...."
- **sentiment**: The sentiment expressed in the text (Positive,Neutral,Negative).
- **text**: The user-generated text reflecting their opinion.

### Data_cleaning 
Before diving directly ton data analysis it is good to have readly available data fro further operations, so data cleaning python file is  included in the repository.
- [loading_data_And_Data_Cleaning.ipynb](./loading_data_And_Data_Cleaning.ipynb): Jupyter notebook for loading and cleaning the data.
- 
### Data_Analysis
- Exploratory data analysis on Twitter data [EDA_Twitter.ipynb](./EDA_Twitter.ipynb): 
- sentiment analysis by entity [Entity-Wise Sentiment Analysis.ipynb](./Entity-Wise%20Sentiment%20Analysis.ipynb)
- TF-IDF keyword extraction, [TF-IDF for keyword extraction.ipynb](./TF-IDF%20for%20keyword%20extraction.ipynb)

### Sample_Outputs

This repository contains sample outputs of the data analysis

- Negative sentiment words [Negative Sentiment Words.png](./Negative%20Sentiment%20Words.png)
- Entity-wise sentiment analysis [outputEntity-Wise Sentiment Analysis.png](./outputEntity-Wise%20Sentiment%20Analysis.png)
- Positive sentiment words [Positive Sentiment Words.png](./Positive%20Sentiment%20Words.png)
- sentiment distribution [Sentiment Distribution.png](./Sentiment%20Distribution.png)

## How_to-Contribute

If you'd like to contribute to this dataset or improve the analysis, feel free to open a pull request or submit issues.

## License

This dataset is available under the [MIT License](LICENSE).
 # Social Media Sentiment Analysis
   Analyze sentiment patterns in social media data to understand public opinion on specific topics or brands.
