#Sentiment-Analysis-of-Musical-Tracks


INTRODUCTION 

Music has always been a powerful tool for expressing and eliciting emotions - It can transport listeners to different emotional states, it uplifts people in their hours of sorrow, it calms peoples’ nerves before an important event - The sheer influence music has on our lives is impalpable. It, thus, can evoke a wide range of moods in one’s mind and body. By classifying the moods of songs, we can better understand the emotional impact of music and how it affects our behavior, thoughts, and feelings.

Firstly, by identifying the mood of a song, we can better understand its intended purpose and the emotions it is meant to convey. For example, a song with a somber or melancholic mood might be used to express feelings of sadness, while a song with a lively and upbeat mood might be used to evoke feelings of happiness or excitement. By understanding the intended mood of a song, we can better connect with the emotions it is meant to express. 

Secondly, by categorizing the moods of songs, we can create playlists or curated music experiences that cater to specific emotional states or activities. For example, a workout playlist might include songs with a high-energy, upbeat mood, while a relaxation playlist might include songs with a calm and soothing mood. By curating playlists based on mood, we can create a more personalized and effective musical experience that can enhance our mood and improve our overall well being.

Lastly, classifying the moods of songs can also be useful for music producers, marketers, and advertisers who are trying to understand the emotional impact of music on their audience. By analyzing the mood of a song and its impact on listeners, they can create more effective advertising campaigns or music marketing strategies that target specific emotional states or moods. In this way, understanding the moods of songs can have practical applications beyond simply enjoying music for its emotional content.

Methodology

Since the data is imbalanced we have used stratified sampling and divided the dataset into 80:20 which have the same proportion of all 3 classes in the Training and Testing Group.


Before understanding and selecting the models we have used 2 Algorithms for the process of stemming which are  :

●	Porter : The purpose of stemming is to reduce words to their base or root form, which can help in the sentiment analysis of the song lyrics

●	Snowball : Like Porter, the Snowball algorithm works by applying a series of rules to reduce words to their base or root form, which can improve the accuracy of tasks such as text classification and information retrieval.

Results

Multinomial Naive Bayes Classification (baseline) 
The code snippet provided trains three Multinomial Naive Bayes classifiers on different vectorizers - CountVec, CountVec porter, and CountVec snowball.The first for loop creates a list of pipelines, where each pipeline consists of a vectorizer, a DenseTransformer (which converts the sparse vector output of the vectorizer to a dense array), and a Multinomial Naive Bayes classifier.The second for loop iterates through each pipeline, and performs a 3-fold cross validation on the training data (X_train, y_train) using the cross_validate function from scikit-learn. The accuracy scores for each fold are averaged and printed out for each pipeline.The output of the code snippet shows that the CountVec vectorizer has the highest mean accuracy score of 73.79%, followed by the CountVec porter vectorizer with a score of 73.43%, and the CountVec snowball vectorizer with a score of 73.41%.
Random Forest
The code below shows the accuracy scores of the Random Forest Classifier model trained on three different vectorizers: CountVectorizer, CountVectorizer with Porter stemming, and CountVectorizer with Snowball stemming. The accuracy scores are printed for each model, and they are saved in a dictionary called 'd' that has the accuracy values and the corresponding data type.
The results indicate that the Random Forest Classifier model achieved an accuracy score of around 77.3% to 77.7% across all three vectorizers. The highest accuracy score was achieved by the CountVectorizer with Porter stemming. These results suggest that the Random Forest Classifier model is effective in classifying the sentiment of song lyrics.
