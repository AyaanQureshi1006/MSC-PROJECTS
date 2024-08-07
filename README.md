Sentiment Analysis on Chat Data Using Naive Bayes Classifier
Introduction
This project focuses on sentiment analysis of chat data using the Naive Bayes classifier. Sentiment analysis is a crucial natural language processing (NLP) technique used to determine the emotional tone behind a series of words. It is commonly used in applications such as opinion mining, customer feedback analysis, and social media monitoring.

Dataset
The dataset used for this project is sourced from Kaggle and consists of chat messages with corresponding sentiment labels. The dataset contains various chat messages classified into different sentiment categories, such as positive, negative, and neutral.

Preprocessing
To ensure the data is clean and suitable for modeling, we performed several preprocessing steps:

Removing Non-ASCII Characters: Eliminated junk characters, such as emojis, that were converted into non-ASCII characters in the CSV file.
Lowercasing: Converted all text to lowercase to maintain uniformity.
Punctuation Removal: Stripped punctuation to focus on the core text.
Number Removal: Removed numerical values as they do not contribute to sentiment.
Stop Words Removal: Excluded common words that do not add significant meaning to the text.
Feature Extraction
For transforming text data into numerical features, we used two vectorization techniques:

Count Vectorizer: This method converts the text into a matrix of token counts.

Binary=True: Converts the text into a binary format where the presence of a word is marked as 1, and absence as 0.
Binary=False: Counts the frequency of words in the text.
TF-IDF Vectorizer: This technique measures the importance of a word in a document relative to a collection of documents (corpus). It helps in downscaling the impact of frequently occurring words that may not be as significant.

Model
The primary model used for this project is the Multinomial and Bernoulli Naive Bayes Classifier. This model is well-suited for text classification tasks and handles the categorical nature of the data effectively.

Hyperparameter Tuning
To optimize the model, we performed hyperparameter tuning using GridSearchCV. The alpha parameter, which controls the smoothing in the Naive Bayes classifier, was tuned to find the best-performing value.

Results
After training and evaluating the model with different preprocessing and vectorization techniques, we achieved an accuracy of 82%+ with the optimized Naive Bayes classifier. The model performance indicates a good balance between precision and recall, making it suitable for real-world sentiment analysis tasks.

Conclusion
This project demonstrates the effectiveness of the Naive Bayes classifier for sentiment analysis on chat data. By carefully preprocessing the data and optimizing the model, we achieved a robust and reliable sentiment classification system. Future improvements could include experimenting with different models, such as deep learning techniques, and further refining the preprocessing steps.

Usage
To run this project, follow these steps:

Clone the repository.
Install the necessary libraries: pandas, scikit-learn, re.
Run the Jupyter notebook or Python script provided in the repository.
Acknowledgements
We acknowledge Kaggle for providing the dataset used in this project.
