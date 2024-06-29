**This is a simple model for creating a Fake news detection distinguishing Fake and Real News. I have used the Vectorisation method and Random Forest Classifier for classifying Real and fake news from the dataset.
The Prediction probability is around 90% detecting most of news articles correctly.**

# What is the main principle behind this model?
  The model aims to identify specific types of words that are commonly found in fake news and real news through the provided dataset. Based on this analysis, It classifies the news into two categories: fake and real.
  
# How does it work?
 1. After importing our `Fake.csv` and `True.csv` datasets, We need to pre-process our data to prevent the unnecessary tokens (punctuation marks, uppercase letters, etc) from clashing during the classification process.
 2. We combine the two datasets into one.
 3. As we know the computer does not understand the formal language in this case the strings in the datasets. For that, we will be converting each news article into vectors for each token (a word) using vectorization.
    - What is the vectorisation of tokens? For this, we will be using TF-IDF `(Term Frequency-Inverse Document Frequency)` which is the product of the Total occurrence of that word in that news article (TF) and the Logarithmic Function of the Total news articles present in the dataset divided by the Total number of news articles containing that word (IDF).
    - Words with higher TF-IDF scores are considered to be more significant or relevant to a specific document (news article).
      
 5. Using Random Forest Classifier we classify the dataset into Fake and Real.
 6. We evaluate the test data we created during the pre-processing with the classification model we created using the Random Forest Classifier.
