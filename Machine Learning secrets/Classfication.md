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
* best attribute:more predictiveness, less impurity, lower entropy after splitting
* splitting is a process of decrease in impurity of nodes
* constructing a decision tree is all about finding attributes that return the highest information gain.
## how to measure pure
* entropy: measure of randomness or uncertainty of certain *node* (low entropy, purer node)
* information gain: entropy of a tree(result entropy) before the split minus the weighted entropy after the split by an attribute
>can increases the level of certainty after splitting

# Logistic Regression
* Logistic Regression measures the probability of a case belonging to a specific class.
* Taking the linear regression and transforming the numeric estimate into a probability with the following function, which is called sigmoid function 𝜎
## Good candidate
1. binary classification
2. need probabilistic results
3. understand the impact of a feature
## Logistic VS linear
* Logistic regression is Sigmoid function of linear regerssion
* Sigmoid function output is always between 0 and 1
<img width="500" alt="Screen Shot 2019-04-23 at 4 45 36 PM" src="https://user-images.githubusercontent.com/27160394/56614556-49b59b00-65e7-11e9-9d3c-589cb8009678.png">

## Train process
1. initialize coefficients
2. Calculate preditct result
3. Compare the predict result and actual one and record it as error
4. calculate the error for all customers(cost function)
5. update(coefficients) to minimize costs
6. go back to step 2
* how change coefficients in order to minimize costs: gradient descent
* when should we stop the iterations:meet the requirement
* Cost function: The difference between the actual values of y and our model output y hat
# Tuning parameter
1. should calculate the minimum point of this cost function
  1. gradient descent:using taking steps in the current direction of the slope, and the learning rate is like the length of the step you take.
 
 # SVM
 * a supervised algorithm that can classify cases by finding a separator.
 ## Challenges
 1. how do we mapping data into a higher-dimensional space: kernal function
 2. how can we find the best separator: find biggest margin
 
 ## Pros and Cons
* Pros: 
1. accurate in high-dimensional spaces
2. memory efficient(subset of training points)
* Cons
1.Prone to over-fitting
2.small datasets
3. no probability estimation

## Applications
1. Image recognition
2. Text category assignment
3. Detecting spam
4. Sentiment analysis
5. Gene expression classification
 2. how can we find the best separator: fin 
 2. how can we find the best separator: fin 
