**# Machine Learning-
ML algorithums daily study with explination step by step with pros cons and the codes 

_**Machine Learning**_ -ML is the barch of the AI where the machine laern from the past data and improve the performance without being explicitly programmed.

**why we go for ML?**
In the daily life there are some task which are  not able to do or completable by human (it take huge time )
where we use the machines (machine complete it within a sec ) it finds the patterns and work and give the results accordingly .

Algorithums -- A set of the code contains the steps and the rules to solve the real worls problem in the effective way .


Machine Learning
│
├── 1. Supervised Learning (has labels / answers)
│     │
│     ├── Regression (predict numbers)
│     │     ├── Linear Regression
│     │     └── Polynomial Regression
│     │
│     └── Classification (predict categories)
│           ├── Logistic Regression
│           ├── Decision Tree
│           ├── Random Forest
│           ├── K-Nearest Neighbors (KNN)
│           ├── Naive Bayes
│           └── Support Vector Machine (SVM)
│
├── 2. Unsupervised Learning (no labels)
│     │
│     ├── Clustering (grouping data)
│     │     ├── K-Means
│     │     ├── Hierarchical Clustering
│     │     └── DBSCAN
│     │
│     ├── Dimensionality Reduction
│     │     ├── PCA (Principal Component Analysis)
│     │     └── t-SNE
│     │
│     └── Association Rule Learning
│           ├── Apriori
│           └── FP-Growth
│
└── 3. Reinforcement Learning (reward-based learning)
      │
      ├── Q-Learning
      ├── Deep Q Network (DQN)
      └── Policy Gradient




__Supervised Learning __


The algorithm learns the relationship between input and output from past examples and then uses that learning to predict results for new data.
lets start with the Regression algorithums.

1.**Regression algorithum**------

_Regression is a type of supervised learning in which the model predicts a continuous numerical value based on input features._

_Linear Regression_ (Supervised Learning)

? What is Linear Regression ?
Linear Regression is a supervised learning algorithm used to predict a continuous numerical value based on input features.It finds the best fitting straight line between input (x) and output (y).

 Core Idea
Input → x (features)
Output → y (prediction)
Model learns relationship: x → y
📐 Mathematical Equation

               y=mx+b
Where:
y = predicted value
x = input feature
m = slope (weight)
b = bias (intercept)


 _How Linear Regression Works_

Takes input data (x, y)
Assumes a line (initial guess)
Predicts values using equation
Finds error between actual and predicted values
Adjusts m and b to reduce error
Repeats until best fit line is found


 _Types of Linear Regression_

1. Simple Linear Regression
One input feature → one output
Example:
marks = f(hours studied)

3. Multiple Linear Regression
Multiple input features → one output
Example:
marks = f(hours studied, sleep, practice)


_Evaluation Metrics_ 

_Used to check model performance:_

1. MAE (Mean Absolute Error): Average of absolute errors
Simple interpretation
2. MSE (Mean Squared Error): Squares errors (penalizes big mistakes)
3. RMSE (Root Mean Squared Error): Square root of MSE
Same unit as output → easy to understand
4. R² Score: Measures how well model fits data
Range: 0 → 1
Closer to 1 = better model














_Logistic Regression_ (Supervised Learning)

 What is Logistic Regression?

Logistic Regression is a supervised learning algorithm used for classification problems.It predicts the probability of an outcome (0 or 1) instead of a continuous value.Even though it has “regression” in the name, it is mainly used for classification.

Core Idea
Input → x (features)
Output → probability (0 to 1)
Model learns relationship: x → probability → class

Example:
Spam email detection → Spam / Not Spam
Disease prediction → Yes / No

 Mathematical Equation
First, linear equation:
                 
                  z=mx+b
Then apply sigmoid function:

                σ(z)=1+e−z1​
	
      
Output becomes probability between 0 and 1

_ How Logistic Regression Works_

Takes input data (x)
Computes linear combination (z = mx + b)
Applies sigmoid function
Converts result into probability (0 to 1)
Applies threshold:
≥ 0.5 → Class 1
< 0.5 → Class 0
Final prediction is a class label

_Types of Logistic Regression_

1. Binary Logistic Regression:(Two classes only)
Example:
Spam / Not Spam
Yes / No

3. Multinomial Logistic Regression:(More than 2 classes (no order))
Example:
Cat / Dog / Horse

3. Ordinal Logistic Regression:(More than 2 classes with order)
Example:
Low / Medium / High
Poor / Good / Excellent

_Evaluation Metrics_

Used to check classification performance:
1. Accuracy: Percentage of correct predictions
2. Precision: How many predicted positives are actually correct
3. Recall: How many actual positives are correctly predicted
4. F1 Score: Balance between precision and recall
5. Confusion Matrix

Shows:
True Positive (TP)
True Negative (TN)
False Positive (FP)
False Negative (FN)















**2) Classification **-----


_Classification is a type of supervised learning in which the model predicts a category or class label instead of a number._



What is Decision Tree?

A Decision Tree is a supervised learning algorithm used for both:Classification (category output)
Regression (number output) It works like a flowchart of decisions (if–else rules) to make predictions.

Core Idea
Input → features (x)
Output → class (classification) OR value (regression)
Model learns: decision rules from data

It splits data step-by-step until it reaches a final answer.

_ Structure of Decision Tree_


Root Node → starting feature
Decision Nodes → conditions (if/else)
Branches → outcomes of conditions
Leaf Node → final prediction


_How Decision Tree Works_


Select best feature to split data
Split dataset into groups
Repeat splitting for each group
Stop when:
Data becomes pure (same class), OR
Maximum depth is reached
Give final output at leaf node

Example (Simple)
Predict: Will customer buy product?

_Rules:_
If income > 50K → Buy
If income < 50K AND age < 25 → Not Buy
If browsing time > 10 min → Buy

libThis is how tree creates if–else logic





_How it chooses best split?_

It uses impurity measures:
1. Gini Impurity


          Gini=1−∑pi2​
	​


Measures how mixed the data is
Lower value = better split

2. Entropy (Information Gain)



        Entropy=−∑pi​log2​(pi​)
   
Measures randomness in data
Tree selects split with highest information gain

_Adantages_
Easy to understand (human-readable rules)
No need for scaling data
Works for both classification & regression
Handles numerical + categorical data

_Disadvantages_
Can overfit (very deep trees)
Small data changes can change tree structure
Less accurate compared to ensemble models




