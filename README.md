# SOEN471-PROJECT - Suicide and Depression Sentiment Analysis - Team 13

## Abstract

**Please note that we were intially supposed to do Promly project, but due to their unprofessional behavior, we decide to opt on doing our own project.**

Social media has become a very powerful tool in our everyday lives. It helps us build new connections, allows us to network ourselves better, and also enjoy banter with other people around the world. However, not all social media is beneficial to us. Many people online are subject to cyberbullying, death threats, and even hacking attempts. This leads to an increased chance of a person being depressed and even sometimes going to the extreme of wanting to kill themselves. Our project wants to be able to prevent this as we want to implement a sentiment analysis project, where through various text messages, we will predict if that person is suicidal or not. 


# 1. Research Question and Personal Objectives

Our main research question for the project will be that **are we able to create a proper sentiment analysis algorithm which accurately identifies suicidal and non-suicidal messages?**

Some personal goals that we want to acheive from this project are the following:

1. Will our project be able to receive an accuracy measure of atleast 90%, as we want to classify the most amounts of messages properly?
2. What are the keywords from a corpus which would lead to a message being clasified as suicidal/non-sucidal?

# 2. Dataset Information
![image](https://user-images.githubusercontent.com/59709752/220502250-1d5899dc-47d8-4034-bfeb-79b3aff2e541.png)

The dataset that we have chosen is [Suicide and Depression Detection](https://www.kaggle.com/datasets/nikhileswarkomati/suicide-watch) on Kaggle. This dataset has two features that we will use are text, which are the messages that has been retreived from various different social media platforms, and the class, which is the classification of the text into sucidial and non-suicidal labels. In terms of the size of the dataset, we have 232 074 unique values, and it is around 177 MB.

# 3. Data Preprocessing

The data will be preprocessed in order to remove noise in the text region. Such noise includes stop words, email adresses, special characters. Moreover, all text will be transformed to lowercase and split into words based on the space character. Furthermore, lemmatization will be applied to the words to better group them later.

For the pre-processing, we will be using the ``neattext`` package itself, which will aid to remove special characters and stop words. We will also be using some of the libraries from nltk such as the ``WordNetLemmatizer`` package which, based on conext and usage, will lemmatize words. We will also be using the ``tqdm`` library in order to create progress bars.


# 4. Materials and Algorithms

Since we will be doing a sentiment analysis, we know that we will need to not only come up with good classification models, but also we would need to come up with alternatives as well. The two main ones that we will choose will be highlighted in bold. 

| Model             | Algorithm to use | Why we feel it would work for our project?                 |
| -------------------- | ---------- | ------------------------------------------------------------- |
| **Naive Bayes**  | ``sklearn.naive_bayes.MultinomialNB``  |  **Very widely used in NLP tasks, one of them being sentiment analysis. Allows for faster computation time than other models, as well relatively low amount of training required. We would also use this model with the Bag of Words Model (BOW) to better improve our numbers at the end.**                |
| **Random Forest Algorithm**| ``sklearn.ensemble.RandomForestClassifier`` | **It's widely used for regression and classification purposes. In order to do that, the algorithm works by constructing multiple training trees which would then allow the data to be classified. In this case, it will be classified using regression which gives a score of similarity between the text in question and those that were previously identified to having depression and/or suicidal thoughts in the dataset.** |
|   Logistic Regression   | ``sklearn.linear_model.LogisticRegression``   |     The algorithm estimates the probability of the binary output from a set of independent variables. Since the outcome is a probability, it is bound between 1 and 0. This is useful when the dependent variable is categorical, suicidal (1) or non-suicidal (0).        |
| Long short-term memory (LSTM) | ``tf.keras.layers.LSTM`` | This type of recurrent neural network (RNN) has been successfully applied to NLP. LSTM retains a long-term memory from previous data anaylized, thus in the context of sentiment anaylsis there is a better understanding of the overall context of the text.          |



# 5. Team Members
| Name                 | Student ID | GitHub Page                                                   |
| -------------------- | ---------- | ------------------------------------------------------------- |
| Mohammad Ali Zahir   | 40077619   | [AliZ786](https://github.com/AliZ786)                         |
| Samantha Guillemette | 26609198   | [SamanthaGuillemette](https://github.com/SamanthaGuillemette) |
| Marita Brichan       | 40138194   | [maritabrichan](https://github.com/maritabrichan)            |
| Souvik Polol Alam    | 40044092   | [Checkz97](https://github.com/Checkz97)          |

# 6. Presentation Slides
### [Link to the slides](https://docs.google.com/presentation/d/1-NyPbjZ2oDabuDr8Y1fpIdkZFN4VMQawfb6UM8jtqr0/edit?usp=sharing)
