# Twitter Sentiment Analysis with R

## Goal: The goal of this project is to predict the sentiment in the tweets.


![Screenshot 2023-04-19 110752](https://user-images.githubusercontent.com/125946256/233135312-c46b9fb7-7716-46b6-99cb-587b5e563718.jpg)

 This image shows the frequent words in the document term matrix


Naive bayes algorithm is used to predict the sentiment in the tweets.

### Dataset.

The data contains more than 99,989 rows. Training data is divided into 69,992 instances and the blind hold data set into 29,997 instances.

### Data Preprocessing:

Data preprocessing includes changing the encoding to universal encoding, creating text corpus for text mining, cleaning data to reduce the dimensionality,
(because dimensionality might be a problem here as the dataset too big) this data cleaning includes removing the punctation, urls, numbers, usernames, stopwords. 
Further redction in dimensionality is done by stemming. 

After preprocessing, tokenization(creating document term matrix) is done. Now there are 32,035 columns which means there are 32,035 words and 69,992 instances
to train and validate the model in order to predict the sentiment in the test data.

The training data set is divided as 75% for training (52494 instances) the model and 25% to evaluate the model.  
The most frequent words are identified from the document term matrix, these words are extracted from the both the training and validation datsets.  

Now using the frequent words the dimensionality is reduced to approx. 4k columns for the training set. The document term has created the binary attributes, 
they are converted to categorical

Now the training set is ready to go into the naive bayes classifier along with labels that are extracted into a separate vector.

The preproceesing is done

### Training the model


These labels and the preprocessed training data are used in the naive bayes algorithm to train the model.


### Evaluation


The evaluation is done using the validation set and trained model to predict the sentiment. 
The results are evaluated using confusion matric and crosstable function.


### Hyperparametric Tuning

After Evaluation, the model is trained again using hyperparametric tuning, which improved the accuracy for the model
the improved accuracy is confirmed by confusion matrix using accuracy as the metric.

### Deployment of the model with best accuracy.

The second model is the best in predicting the sentiment in blind hold datset.

This model won second place in kaggle competetion condcuted by our professor.



