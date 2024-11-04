# Disaster Tweets Classification

This project aims to classify tweets as either related to a real disaster or not. It uses a machine learning approach, specifically Logistic Regression, to train a model on a dataset of tweets labeled with their disaster status.

## Dataset

The project uses two datasets:

- **train (1).csv:** This dataset contains tweets labeled as either real disaster (1) or fake disaster (0). It is used for training the model.
- **test (1).csv:** This dataset contains tweets without labels. It is used to predict the disaster status of new tweets.

Both datasets have the following columns:

- **id:** A unique identifier for each tweet.
- **keyword:** A keyword associated with the tweet.
- **location:** The location where the tweet was posted.
- **text:** The actual content of the tweet.
- **target:** (Only in train (1).csv) The label indicating whether the tweet is related to a real disaster (1) or not (0).


## Methodology

1. **Data Preprocessing:**
    - Missing values in the 'keyword' and 'location' columns are dropped.
    - The 'keyword', 'location', and 'text' columns are merged into a new column called 'content'.
    - The 'content' column is cleaned by removing special characters, converting to lowercase, and applying stemming using the PorterStemmer. Stop words are also removed.
2. **Feature Extraction:**
    - The TF-IDF (Term Frequency-Inverse Document Frequency) vectorizer is used to convert the text data into numerical features.
3. **Model Training:**
    - A Logistic Regression model is trained using the preprocessed training data.
4. **Prediction:**
    - The trained model is used to predict the disaster status of tweets in the test dataset.
5. **Evaluation:**
    - The accuracy of the model is evaluated using the accuracy score metric on the training data.
6. **Output:**
    - The predictions for the test dataset are saved in a new CSV file named 'result.csv'.


## Libraries Used

- pandas
- numpy
- matplotlib
- re
- nltk
- sklearn

## Running the Code

1. Upload the 'train (1).csv' and 'test (1).csv' files to your Google Colab environment.
2. Execute the code cells in the provided notebook sequentially.
3. The output file 'result.csv' will be generated, containing the predictions for the test dataset.


## Note

- The accuracy of the model can be further improved by exploring different preprocessing techniques, feature engineering, and model selection.
- The code assumes that the necessary libraries are already installed. If not, you may need to install them using pip install.
