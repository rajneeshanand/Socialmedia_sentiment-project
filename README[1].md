# Social-Media-Sentiment-Analysis
Sentiment analyzer learns about various sentiments behind a “content piece”. (could be IM, email, tweet, or any other social media post) through machine learning and predicts the same.It is the interpretation and classification of emotions (positive, negative and neutral) within text data using text analysis techniques. Sentiment analysis allows organizations to identify public sentiment towards certain words or topics.

#Natural Language Processing (NLP): The discipline of computer science, artificial intelligence and linguistics that is concerned with the creation of computational models that process and understand natural language. These include: making the computer understand the semantic grouping of words (e.g. cat and dog are semantically more similar than cat and spoon), text to speech, language translation and many more

![image](https://user-images.githubusercontent.com/62300368/179838912-ee0eef28-33a5-4604-81b4-45787d012a00.png)

Procedure
1. Data Inspection
Dataset

2. Data Cleaning
Remove @user from tweets
Remove punctuations and numbers from tweets replace("[^a-zA-Z#]", " ")
Remove words whose length is less than 3 word < str.len(3)
Text Normalization using Porter Stemmer
Porter Stemmer

Tokenize the tweets
Normalize the tweets
Stich it back using nltk's Moses Detokenizer
Dataset cleaned

3. Story Generation
Most common words
Word Cloud
![image](https://user-images.githubusercontent.com/62300368/179839441-b6a8d0da-31b5-48d3-b9de-37e98a1991ec.png)



Most Popular Hashtags
Dataset cleaned

Bag of Words Features
Bag of Words (BOW) is a method to extract features from text documents. These features can be used for training machine learning algorithms. It creates a vocabulary of all the unique words occurring in all the documents in the training set. In simple terms, it’s a collection of words to represent a sentence with word count and mostly disregarding the order in which they appear.

TF-IDF Features
Term Frequency-Inverse Document Frequency. It Penalise the most common words by assigning them lower weights while giving imortance to words which are rare in corpus but apper in good number in few documents.

TF = (Number of times term 't' appears in a doc) / (Number of terms in doc)

IDF = log(N/n)

where, N = number of document

n = number of documents a term 't' has appeared in

TF-IDF = TF*IDF

Word2Vec Features
It represents each word as a vector(Word Emebddings). The objective is to redefine high dimensional word features into low dimensional features by preserving contexual similarity in corpus.

Advantages>

Dimensionality reduction: Significant reduction in number of features
It captures the meaning of word i.e., semantic erlations and different types of context
Word2Vec is combination of two algorithms:

4. Modeling
Evaluation Matrix: Different Classification Algorithms were run and one with best accuracy was zchosen for getting results.

5. Results
Accuracy

Linear SVC(Support Vector Machines) : 82%

Logistic Regression Model : 83%

BernoulliNB Model : 80%

We can clearly see that the BernoulliNB Model and Logistic Regression Model performs the best out of all the different models that we tried.But BernoulliNB Model Overfits the Data as its accuracy is . Where as Logistic Regression Model achieves nearly 83% accuracy while classifying the sentiment of a tweet.
