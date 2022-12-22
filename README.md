# CS-433: ML Project 2 - ML4Science project: Vote prediction

# Intro

This project aims at predicting the votes of each deputy of the Valaisan consituante, for a given article. We used a dataset with the information of each deputy and the votes they had for each of the selected votes. We have chosen the votes of quivotequoi.ch which is a site that gives the results and explanations on important votes. 

You will find more information about our source codes and methods in this readme.md file.

### Authors

- _Nicolas Jimenez_
- _Blanche Marion_

## Setting up

This code was tested with Python 3.8 or higher and below is the list of libraries used for this project.

    sklearn
    numpy
    matplotlib
    padas
    seaborn
    keras

As a default `numpy` is installed. For other packages, you will need to run `requirements.pip` to download the necessary packages. To do this, you will need to make a python virtual environment then run the command below:

    pip install -r requirements.pip

## Repo Structure

The folder structure has to be the following:

    ├── Data              # Data files, in .csv
    |    ├── train.csv
    |    └── test.csv
    ├── Code     # column names for train, test data.
    |    ├── new_data_processing.ipynb      #Data processing and creation of the dataset
    |    └── Binary Classification.ipynb    #Classification algorithm and optimization
    |    └── Creation NLP Dataset.ipynb     #NLP file (not to use)
    |    └── Traduction_and_Classification.ipynb    #NLP file (not to use)
    |    └── Binary Classification.ipynb    #NLP file (not to use)
    └── README.md

### NLP files
We tried to use pre-train models found with the huggingsface library to classify our articles. We had to translate our articles first and then classify them according to themes. However, the themes proposed by the article were not consistent with the themes of the Valaisan constituent. We therefore preferred not to use this method. 

### New data processing.ipynb
In this file, we process the original csv and use it to build a dataset with the information of each article and each voter. Then we do some one hot encoding and embedding to process the categorical features.

### Binary classification.ipynb
In this file, we tested different models with embedded dataset and one hot encoded dataset, made PCA in order to find the best performing algorithms. Then, we did some optimization on the extreme gradient boosting by doing feature selection.

