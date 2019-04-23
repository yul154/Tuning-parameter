# Basic conception
* Categorizing items into a discrete set of "classes"
* Target attribute is a categorical variable

# Classification algorithms
1. Decision Trees
2. Naive Bayes
3. Linear Discriminant Analysis
4. KNN
5. Logistic Regression
6. Neural Networks
7. SVM

# K-Nearest-Neighbours
> Majority vote from K neighbor
1. pick a value for K
2. Calculate the distance of unknown case from all cases
3. Select the k-observations in the training data that are 'nearest' the unknown data point
4. predict the unknown point by most popular label
## K choice
* low: overfitting
* high: underfitting
* solutions: chose k =1, use the training part for modeling, and calculate the accuracy of prediction using all samples in your test set. Repeat this process, increasing the k, and see which k is the best for your model.

## Evaluation metrics in Classification
1. Jaccard index
<img width="305" alt="Screen Shot 2019-04-22 at 10 15 56 PM" src="https://user-images.githubusercontent.com/27160394/56547748-4a4d2380-654c-11e9-9643-2cdb2f4cfc03.png">
2. F1 score
<img width="310" alt="Screen Shot 2019-04-22 at 10 19 16 PM" src="https://user-images.githubusercontent.com/27160394/56547921-be87c700-654c-11e9-8701-1f1294af2578.png">
3. log loss: measures the performance of a classifier where the predicted output is a probability value between 0 and 1.

# Decision Trees
## Algoritm
1. calculate the significance of attribute in splitting of data
2. split the data into subsets based on 'best attribute'
3. go to step 1
* the method uses recursive partitioning to split data into segments by minimizing the impurity at each step. 
## find `best` attribute
* best attribute:more predictiveness, less impurity, lower entropy
* splitting is a process of decrease in impurity of nodes
## ho
w


