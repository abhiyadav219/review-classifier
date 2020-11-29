# review-classifier

This is restaurant review classifier using NLTK

# Scikit

Scikit-learn is a free software machine learning library for Python programming language. Scikit-learn is largely written in Python, with some core algorithms written in Cython to achieve performance. Cython is a superset of the Python programming language, designed to give C-like performance with code that is written mostly in Python.

# Dataset

The dataset is from Kaggle, a collection of Restaurant Reviews dataset, with 1000 reviews, all classified as either ‘0’ or ‘1’. The dataset contains 50% like reviews and 50% dislike reviews.

# Steps involved

Step 1: Import dataset with setting delimiter as ‘\t’ as columns are separated as tab space. Reviews and their category(0 or 1) are not separated by any other symbol but with tab space as most of the other symbols are is the review (like $ for price, ….!, etc) and the algorithm might use them as delimiter, which will lead to strange behavior (like errors, weird output) in output.

Step 2: Text Cleaning or Preprocessing.

Step 3: Tokenization, involves splitting sentences and words from the body of the text.

Step 4: Making the bag of words via sparse matrix.

Step 5: Splitting Corpus into Training and Test set. For this, we need class train_test_split from sklearn. cross_validation. Split can be made 70/30 or 80/20 or 85/15 or 75/25, here I choose 80/20 via “test_size”.

Step 6: Fitting a Predictive Model (here MultinomialNB).

Step 7: Predicting Final Results via using. predict() method with attribute X_test

Step 8: To know the accuracy, confusion matrix is needed.

# Conclusion

A model with an 84% accuracy has been built. Accuracy is preferred so that review messages will not be misclassified as dislike.
A more customized pre-processing step will contribute to a more precise model.
For this dataset, linear models with high bias and low variance like the Logistic Regression and Naïve Bayes classifier have performed better than non-linear models like k-Nearest Neighbor classifier and Random Forest classifier.


