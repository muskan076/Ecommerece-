# E-commerce Text categorisation

This task includes the following steps:

1. Data Cleaning
2. EDA and Text preprocessing
3. Model Building and evaluation
4. Imporvement


In first step, I did the following things: 
* droppped duplicate rows
* checked for null values if available
* converted text labels into numeric values i.e 0 for Electronics, 1 for Households, 2 for Books, 3 for Clothing and Accesories category
* and other basic changes required for further steps

In second step, we explored about our dataset by
* checking the distribution of each category
* In text preprocessing, 
   + I converted all the text of a column into lower case 
   + The next step included the tokenisation based on the words.
   + Now, I removed all the stopwords(stopwords are the words which help in senctence formation but don't have any meaning like is, are am, you'll etc. Hence, it's reuired to remove such words otherwise these words may dominant and will not good results on our algorithm.
   + I also removed punctuations by using string library
   + At last, I used stemming. Stemming converts the word into its root form like waiting, waited  both will  wait.
   
* Also, I created some visual like wordcloud, barplot, pie chart to know more about the data.

In 3rd step,
* used bag of words and tf-idf for text vectorisation
* splitted the dataset into training and test dataset.(80% data into training  and 20% of the data into test dataset)
* tried different machine learning algorithms.
* selected the one which gave maximum precision score as the data is imbalanced, we should tend to ignore Accuracy score.

Note that I kept the model simple there is still a room to improve the model's performance. For instance,
* We could have done more hyperparameter tuning and could have used cross validation instead of train_test_split to see how the model is performing. Maybe, we could also have tried for grid search or random search for hypertuning parameters.
* I firstly used bag of words and now used tfidf to see whether algorithms performance is improving or not and guess what it improved. We could also have tried for word2vec. In tf-idf I added max_features argument and changed it and at max_features = 4000 it gave good results.
* We could also have used different techniques to balance the data and then apply machine learning algorithm.


The best performing algorithms:
1. Support Vector Machine
2. Multinomial Naive Bayes

# References:

* https://www.youtube.com/watch?v=tYZ6cpatw-w&t=209s
* https://www.youtube.com/watch?v=Qbd7U9F0QQ8&t=2544s
* https://www.youtube.com/watch?v=YncZ0WwxyzU&t=5006s
* https://www.geeksforgeeks.org/bag-of-words-bow-model-in-nlp/
* https://stackoverflow.com
* https://www.analyticsvidhya.com/blog/2017/09/naive-bayes-explained/
* https://medium.com/




