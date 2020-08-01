I am Swayam Bukharia, 2nd year undergrad IITG.

This model is made for predicting flair of the post on india subreddit.

I have finally used "TITLE" field only to predict the flair as, Body is not available in most of the posts and most of the times 
comments seems to be misleading and diverting, which can reduce the accuracy of the model.

This is multi-class classification problem -

Total 13 classes

flair are mapped to their correponding labels-
{'AskIndia': 2,
 'Business/Finance': 7,
 'Coronavirus': 13,
 'Demonetization': 6,
 'Food': 5,
 'Non-Political': 1,
 'Not in English.': 10,
 'Photography': 4,
 'Policy/Economy': 12,
 'Politics': 3,
 'Science/Technology': 11,
 'Sports': 9,
 '[R]eddiquette': 0,
 'other': 8}

I have trained the model on basically 4 Machine Learning algo and other using recurrent neural network with LSTM units with 
GlobalMaxPooling layer.

Machine Learning Algos used- Logistic regression, Multinomial NAIVE- BAYES, Linear SVM, SVM with non-linear kernel(used rgb) whose 
accuracy and f1-score results along with result for RNN are given below. I am using CountVector with TFIDF.

1. Logistic Regression- 
   Accuracy - 52.8 %, f1 - 53 %
   
2. Multinomial Naive Bayes-
   Accuracy - 45.9 %, f1 - 41.4 %
   
3. Linear SVM-
   Accuracy - 51.7 %, f1 - 52.1 %
   
4. SVM with non-linear kernel(used rgb)
   Accuracy - 53.3 %, f1 - 53.8 %
   
RNN with LSTM layer-
Trained word2vec embedding on reddit corpus from 4 years data using gensim
Main libraries used gensim, nltk. Deep-Learning Framework used keras.
Using GlobalMaxPooling layer improved the performance by nearly 2 %. Spatial Dropout Layer introduced to reduce the risk of overfitting.

RNN Model-
Accuracy - 58 %, f1 - 57.4 %

loss functions - tried both categorical cross-entropy and huber loss. Both give nearly same results.

So RNN Model is used for prediction.

This problem comes under the category where human level accuracy is low which is often considered as a threshold.

The result obtained here are well comparable with other models(not using pre-trained embedding)for flair prediction.

Note- Using pre-trained embedding can improve accuracy but due to limited resourced cannot use it in my model.


   
 
