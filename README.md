# SOEN471-PROJECT - Suicide and Depression Sentiment Analysis

## Abstract

**Please note that we were intially supposed to do Promly project, but due to their unprofessional behavior, we decide to opt on doing our own project.**

Social media has become a very powerful tool in our everyday lives. It helps us build new connections, allows us to network ourselves better, and also enjoy banter with other people around the world. However, not all social media is beneficial to us. Many people online are subject to cyberbullying, death threats, and even hacking attempts. This leads to an increased chance of a person being depressed and even sometimes going to the extreme of wanting to kill themselves. Our project wants to be able to prevent this as we want to implement a sentiment analysis project, where through various text messages, we will predict if that person is suicidal or not. 


# 1. Objectives

For our project, we want to answer the following research questions:

1. Will our project be able to receive an accuracy measure of atleast 90%, as we want to classify the most amounts of messages properly?
2. What are the keywords from a corpus which would lead to a message being clasified as suicidal/non-sucidal?

# 2. Dataset Information
![image](https://user-images.githubusercontent.com/59709752/220502250-1d5899dc-47d8-4034-bfeb-79b3aff2e541.png)

The dataset that we have chosen is [Suicide and Depression Detection](https://www.kaggle.com/datasets/nikhileswarkomati/suicide-watch) on Kaggle. This dataset has two features that we will use are text, which are the messages that has been retreived from various different social media platforms, and the class, which is the classification of the text into sucidial and non-suicidal labels. In terms of the size of the dataset, we have 232 074 unique values, and it is around 177 MB.

# 3. Data Preprocessing

The data will be preprocessed in order to remove noise in the text region. Such noise includes stop words, email adresses, special characters. Moreover, all text will be transformed to lowercase and split into words based on the space character. Furthermore, lemmatization will be applied to the words to better group them later.

For the pre-processing, we will also be using some of the librairies from SKLearn such as ``sklearn.preprocessing.LabelEncoder`` to fit our training and test data once we have removed the special characters. We will also be using the ``neattext`` package itself, which will aid to remove special characters and stop words.


# 4. Materials and Algorithms

Since we will be doing a sentiment analysis, we know that we will need to not only come up with good classification models, but also we would need to come up with alternatives as well. The two main ones that we will choose will be highlighted in bold. 

| Model             | Algorithm to use | Why we feel it would work for our project?                 |
| -------------------- | ---------- | ------------------------------------------------------------- |
| Naive Bayes  | ``sklearn.naive_bayes.MultinomialNB``  |  Very widely used in NLP tasks, one of them being sentiment analysis. Allows for faster computation time than other models, as well relatively low amount of training required. We would also use this model with the Bag of Words Model (BOW) to better improve our numbers at the end.                 |
|  |    |  |
|      |    |             |
|     |    |           |



# 5. Team Members
| Name                 | Student ID | GitHub Page                                                   |
| -------------------- | ---------- | ------------------------------------------------------------- |
| Mohammad Ali Zahir   | 40077619   | [AliZ786](https://github.com/AliZ786)                         |
| Samantha Guillemette | 26609198   | [SamanthaGuillemette](https://github.com/SamanthaGuillemette) |
| Marita Brichan       | 40138194   | [maritabrichan](https://github.com/maritabrichan)            |
| Souvik Polol Alam    | 40044092   | [Checkz97](https://github.com/Checkz97)          |
