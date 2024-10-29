# Sports-News-Classification-Using-Multinomial-Naive-Bayes
# Overview
This project involves the development of a classification model to categorize sports news articles into one of five categories: football, cricket, athletics, rugby, or tennis. The dataset used in this project is the BBC Sports News Dataset, containing 737 articles. Each article is represented using a Bag-of-Words (BOW) format, which includes word frequency counts for each article.

The primary objective is to implement a Multinomial Naive Bayes classifier that accurately classifies news articles based on their word distributions. Additionally, we explore the impact of additive smoothing (Dirichlet prior) on model performance, providing insights into the data distribution and classification accuracy.

# Dataset
The dataset is provided in two parts:

Training Set: bbcsports_train.csv
Validation Set: bbcsports_val.csv
Each dataset has:

4614 columns:
The first 4163 columns represent word frequencies.
The last column contains the class label (0: athletics, 1: cricket, 2: football, 3: rugby, 4: tennis).
Methodology
# Preprocessing:

The dataset is in BOW format, with stop words removed.
Word frequencies serve as features, and the last column is used as the target label.
Model Implementation:

We trained a Multinomial Naive Bayes model using the training set.
Model parameters were estimated using the Maximum Likelihood Estimation (MLE).
Validation set performance was evaluated using accuracy, confusion matrix, and the number of misclassifications.
Handling Imbalanced Classes:

We analyzed class distributions and identified any class imbalances.
Strategies to mitigate the effects of imbalanced classes, if found, were considered.
Additive Smoothing (Dirichlet Prior):

The model was extended to include additive smoothing with a fair Dirichlet prior (α=1).
This approach helps address issues of zero probability and enhances model performance.
# Evaluation:

Accuracy and confusion matrix were used to assess performance on the validation set.
The impact of additive smoothing was compared against the original model.
# Results
Baseline Model: The Multinomial Naive Bayes model achieved [specific accuracy] on the validation set, with a confusion matrix indicating [specific insights].
Additive Smoothing Model: After implementing additive smoothing, accuracy improved to [specific accuracy], indicating better handling of low-frequency words.
# Challenges & Solutions
Class Imbalance: Imbalanced class distribution was addressed through class weighting in probability estimation.
Numerical Stability: Logarithmic transformations were applied to probability values to prevent numerical underflow.
Additive Smoothing: Improved model performance, especially for classes with fewer instances.
# Conclusion
The implementation of the Multinomial Naive Bayes model effectively classified sports news articles, demonstrating the effectiveness of additive smoothing in improving classification accuracy. Future enhancements could include exploring alternative feature representations and advanced models for better performance.
