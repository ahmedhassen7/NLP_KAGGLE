# NLP Disaster,Fine tuning Xgboost & Bert transformer
## ABstract

Kaggle, which is a web platform that organizes data science competitions, recently launched a competition called "Natural La Natural Language Processing with Disaster Tweets." This competition aims to develop a binary classification model of tweets posted by users. Using machine learning algorithms we will build a model that can distinguish between a tweet containing an alert message for a disaster or not. To be able to capture the content of each tweet we will develop two methods:
- First the one of the Ensembliste methods: The **XGBOOST** classifier from the **xgboost library**. We will use the vectorization techniques provided by Scikit-learn for the format input. The fine-tuning of the hyper-parameters will be held through the RanomizedSearchCV  method along with the cross-validation technique. 
- **Transformers**: As a second method we will discover the **BERT** encoder from **HuggingFace library** for the binary classifications of the sequences (tweet) provided.

## Data Overview

### Dataset
Number of rows in tweets.csv = 10900
Features:
     id - a unique identifier for each tweet
     text - the text of the tweet
     location - the location the tweet was sent from (may be blank)
     keyword - a particular keyword from the tweet (may be blank)
     target - in train.csv only, this denotes whether a tweet is about a real disaster (1) or not (0)


### tweets distribution

![image](https://user-images.githubusercontent.com/64875813/137587309-76e358e8-f159-40ee-bb4e-13a99a55c453.png)

we have roughly a balanced dataset

### WordCloud
Word Clouds are a visual representation of the frequency of words within a given tweet category.
We will be focusing on the disaster category.

![image](https://user-images.githubusercontent.com/64875813/137587429-a4cb04ee-6d16-4043-a479-5aff3fc392b3.png)


## Results


### XGBOOST
![image](https://user-images.githubusercontent.com/64875813/137587493-ed648281-57f3-45c1-9f6c-c317fc236c96.png)

We did reach a precision of 78% wich is a good result

### BERT 

![image](https://user-images.githubusercontent.com/64875813/137587526-cfe9c80c-ff2a-418d-8e88-361dd005e8ee.png)

WE have improved our results with an outstanding performance: 
- Accuracy: 84%
- Loss: 41%
We stopped the training in the fourth epochs in order not to overfit 

## Conclusion 

In this study we focused our research on fine tuning the classification models: 

- **XGBOOST**: through the RandomizedSearchCV along with the cross validation technique we did get the best combination of hyper-parameters 
- **BERT**: starting from the raw version of the classic BERTModel we did build some hidden Sequential layers on the top that performed the classification task 

Both approches performed weill! But we are going to choose the BERT Transfomer as our final candidat

## References




