Twitter Sentiment Analysis Using Logistic Regression

Project Description:

This project is a Twitter sentiment analysis model designed to classify tweets as either positive or negative, providing insights into public opinion across various topics. By processing Twitter data, we developed a machine learning model capable of capturing and analyzing social sentiment.

The dataset used consists of over 1.6 million tweets, each labeled with a sentiment (positive or negative), which is ideal for a binary classification problem. The data required extensive preprocessing, such as text cleaning, symbol removal, and case normalization. Additionally, using tools like the Porter Stemmer and NLTK’s stopwords, we refined the data further by reducing words to their root forms and removing common stopwords, ensuring the model focuses on meaningful content.

Data Preprocessing:
1.	Text Cleaning: Regular expressions were used to remove unwanted symbols, converting the text to lowercase to maintain consistency.

2.	Stemming: We employed the Porter Stemmer to reduce words to their root forms. This method was selected for its speed and simplicity for English text. More complex stemmers, like the Lancaster Stemmer, may over-stem, potentially losing important meanings in the process.

3.	Stopword Removal: To reduce noise, we removed common English stopwords. This step focuses the model on relevant words, enhancing prediction accuracy.

4.	Vectorization: We used the TF-IDF Vectorizer to transform the text into numerical features. TF-IDF highlights important words by their frequency and relevance, emphasizing unique words across tweets and reducing the impact of commonly used ones. It was chosen over CountVectorizer for its ability to capture word significance across documents, enhancing model performance on sentiment analysis.

Machine Learning Model Used: Logistic Regression:

Logistic Regression was chosen for its efficiency, interpretability, and suitability for binary classification. With this large dataset, Logistic Regression provides a linear decision boundary and handles the vectorized text data effectively. While other models, such as Decision Trees or Neural Networks, might yield slightly higher accuracy, they would also increase computational requirements and model complexity, which is unnecessary for this specific problem. Logistic Regression balances simplicity and accuracy, making it a widely preferred model for binary sentiment classification.
Although other algorithms like SVM or Naive Bayes could achieve similar results, they often require more computational resources or yield probabilities that are less intuitive. This makes Logistic Regression the optimal choice for our sentiment analysis task.
 
Model Training and Accuracy:

The data was divided into an 80/20 split, with 80% used for training and 20% for testing. Stratified sampling ensured class balance in both sets. The model was trained with a maximum of 1000 iterations, achieving:
Training Data Accuracy : 81%
Test Data Accuracy.    : 77.8%
These results demonstrate the model's ability to generalize well to new, unseen tweets while maintaining simplicity and efficiency.

Model Persistence: Saving and Loading:

To enable reuse without retraining, we saved the model using Python's `pickle` library. This approach is lightweight and effectively preserves model state, making the model easily deployable in real-time applications for social media sentiment analysis.

Conclusion:

This Twitter sentiment analysis project successfully produced a robust and accurate model using Logistic Regression. With straightforward processing and efficient classification, this model provides a reliable foundation for sentiment analysis in social media. In the future, exploring advanced models like neural networks may enhance accuracy and broaden the application scope for sentiment analysis tasks.

