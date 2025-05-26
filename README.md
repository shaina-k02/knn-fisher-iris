# Knn Investigation using the Fisher-Iris Dataset

Objective: In this project, We will apply the K-Nearest Neighbors (KNN) algorithm to the Iris dataset. Our goal is to explore how sensitive the algorithm is to the parameter k (the number of neighbors). We'll use Stratified K-Fold Cross-Validation to assess the model performance for different values of k, ranging from 1 to 20, and analyze the results.

The Fisher-Iris Dataset

The dataset is composed of 150 samples of irises (flowers) with four attributes per flower. There are three species of iris with 50 samples of each kind. The dataset is a simple one to use for classification tasks where the goal is to predict the label (species) by using the four attributes.

## 1. Load the Iris Dataset and Preprocess the Data

We use the Iris dataset, which contains 150 samples of 3 different species of iris flowers, with 4 features per sample (sepal length, sepal width, petal length, petal width). Standardization is performed using StandardScaler to ensure all features have a mean of 0 and standard deviation of 1. This is important for KNN since it is a distance-based algorithm.

## 2. K-Fold Cross-Validation:

We use Stratified K-Fold Cross-Validation with 50 folds. Stratified sampling ensures that the class proportions remain balanced in both the training and testing sets.

For each value of k, we:

Train a KNN model on the training set (created by combining k−1 folds).

Test the model on the remaining fold.

Repeat this process for all 50 folds and compute the mean accuracy for each value of k.

## 3. Plot the Mean Accuracy vs. k

This function generates a plot of the mean accuracy vs. k (the number of neighbors). The plot helps visualize how the performance of the KNN model changes as we vary the value of k. The x-axis shows the different k k values, and the y-axis shows the mean accuracy across the 50 folds for each k.
