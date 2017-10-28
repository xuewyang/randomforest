# Random Forest and Decision Tree
A tutorial on random forest and decision tree.
Before talking about Random Forest, let's discuss DT first.
<p align="center"><img alt="$$&#10;\frac{n!}{k!(n-k)!} = {n \choose k}&#10;$$" src="https://rawgit.com/xuewyang/randomforest (fetch/svgs/svgs/32737e0a8d5a4cf32ba3ab1b74902ab7.svg?invert_in_darkmode" align=middle width="127.89183pt" height="39.30498pt"/></p>
## What is a decision tree?
Decision tree is a type of supervised learning algorithm that is mostly used in classification problems. In this technique, we split the population or sample into two or more homogeneous sets (or sub-populations) based on most significant splitter / differentiator in input variables.

example:
Let’s say we have a sample of 30 students with three variables Gender (Boy/ Girl), Class( IX/ X) and Height (5 to 6 ft). 15 out of these 30 play cricket in leisure time. Now, I want to create a model to predict who will play cricket during leisure period? In this problem, we need to segregate students who play cricket in their leisure time based on highly significant input variable among all three.

![example](/img/dt1.png)

This is where decision tree helps, it will segregate the students based on all values of three variable and identify the variable, which creates the best homogeneous sets of students (which are heterogeneous to each other). In the snapshot below, you can see that variable Gender is able to identify best homogeneous sets compared to the other two variables.
![formula](/svgs/32737e0a8d5a4cf32ba3ab1b74902ab7.svg)

As mentioned above, decision tree identifies the most significant variable and it’s value that gives best homogeneous sets of population. Now the question which arises is, how does it identify the variable and the split? To do this, decision tree uses various algorithms, which we will shall discuss in the following section.

### Types of Decision Trees
1. Item 1 **Categorical Variable Decision Tree:** Decision Tree which has categorical target variable. Example:- In above scenario of student problem, where the target variable was “Student will play cricket or not” i.e. YES or NO.
2. **Continuous Variable Decision Tree:** Decision Tree has continuous target variable. Example:- Predict customer income based on occupation.

### Terminologies
See the below figure
![terminology](/img/dt2.png)
1. **Root Node:** It represents entire population and this further gets divided into two or more homogeneous sets.
2. **Splitting:** Dividing a node into two or more sub-nodes.
3. **Decision Node:** When a sub-node splits into further sub-nodes, then it is called decision node.
4. **Leaf/ Terminal Node:** Nodes do not split is called Leaf or Terminal node.
5. **Pruning:** When we remove sub-nodes of a decision node, this process is called pruning. You can say opposite process of splitting.
6. **Branch / Sub-Tree:** A sub section of entire tree is called branch or sub-tree.
7. **Parent and Child Node:** A node, which is divided into sub-nodes is called parent node of sub-nodes where as sub-nodes are the child of parent node.

## CART - Classification and Regression Trees
Regression trees are used when dependent variable is continuous. Classification trees are used when dependent variable is categorical.

### How does a tree decide where to split ?
Decision trees use multiple algorithms to decide to split a node in two or more sub-nodes. The creation of sub-nodes increases the homogeneity of resultant sub-nodes. In other words, we can say that purity of the node increases with respect to the target variable. Decision tree splits the nodes on all available variables and then selects the split which results in most homogeneous sub-nodes.

The algorithm selection is also based on type of target variables. Let’s look at the four most commonly used algorithms in decision tree:

#### Gini Index
Gini index is the cost function used to evaluate the splits in dataset. It measures the impurity of data partition K.

Formula:
where n is the number of classes, and P_{i} is the probability that an observation in K belongs to the class.Gini Index assumes a binary split for each of the attribute in S, let say T1 & T2. The Gini index of K given this partitioning is given by 
Which is nothing but a weighted sum of each of the impurities in split nodes. The reduction in impurity is given by:


## Example - Banknote classification

### Banknote dataset

The banknote dataset involves predicting whether a given banknote is authentic given a number of measures taken from a photograph.

The dataset contains 1,372 with 5 numeric variables. It is a binary classification problem.

Below provides a list of the five variables in the dataset.
1. variance of Wavelet Transformed image (continuous).
2. skewness of Wavelet Transformed image (continuous).
3. kurtosis of Wavelet Transformed image (continuous).
4. entropy of image (continuous).
5. class (integer).
Below is a sample from the dataset

3.2414,0.40971,1.4015,1.1952,0
2.2504,3.5757,0.35273,0.2836,0
-1.3971,3.3191,-1.3927,-1.9948,1
0.39012,-0.14279,-0.031994,0.35084,1
