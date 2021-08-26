# 1299 Machine Learning, Data Science & Python Interview Questions (ANSWERED) To Land Your Next Six-Figure Job Offer from [MLStack.Cafe](https://www.mlstack.cafe)

[MLStack.Cafe](https://www.mlstack.cafe) is the biggest hand-picked collection of top Machine Learning, Data Science, Python and Coding interview questions for Junior and Experienced data analyst, machine learning engineers/developers and data scientists with more that 1299 ML & DS interview questions and answers. Prepare for your next ML, DS & Python interview and land 6-figure job offer in no time.

🔴  Get All 1299 Answers + PDFs + Latex formulas on [MLStack.Cafe - Kill Your ML, DS & Python Interview](https://www.mlstack.cafe/?utm_source=github&utm_medium=mlsciq)

---

## <a name='toc'>Table of Contents</a>
 * [Anomaly Detection](#AnomalyDetection)
 * [Autoencoders](#Autoencoders)
 * [Bias & Variance](#Bias&Variance)
 * [Big Data](#BigData)
 * [Big-O Notation](#Big-ONotation)
 * [Classification](#Classification)
 * [Clustering](#Clustering)
 * [Cost Function](#CostFunction)
 * [Data Structures](#DataStructures)
 * [Databases](#Databases)
 * [Datasets](#Datasets)
 * [Decision Trees](#DecisionTrees)
 * [Deep Learning](#DeepLearning)
 * [Dimensionality Reduction](#DimensionalityReduction)
 * [Ensemble Learning](#EnsembleLearning)
 * [Genetic Algorithms](#GeneticAlgorithms)
 * [Gradient Descent](#GradientDescent)
 * [K-Means Clustering](#K-MeansClustering)
 * [K-Nearest Neighbors](#K-NearestNeighbors)
 * [Linear Algebra](#LinearAlgebra)
 * [Linear Regression](#LinearRegression)
 * [Logistic Regression](#LogisticRegression)
 * [Machine Learning](#MachineLearning)
 * [Model Evaluation](#ModelEvaluation)
 * [Natural Language Processing](#NaturalLanguageProcessing)
 * [Naïve Bayes](#NaïveBayes)
 * [Neural Networks](#NeuralNetworks)
 * [NumPy](#NumPy)
 * [Optimization](#Optimization)
 * [Pandas](#Pandas)
 * [Probability](#Probability)
 * [Python](#Python)
 * [Random Forests](#RandomForests)
 * [SQL](#SQL)
 * [SVM](#SVM)
 * [Scikit-Learn](#Scikit-Learn)
 * [Searching](#Searching)
 * [Sorting](#Sorting)
 * [Statistics](#Statistics)
 * [Supervised Learning](#SupervisedLearning)
 * [TensorFlow](#TensorFlow)
 * [Unsupervised Learning](#UnsupervisedLearning)
## [[⬆]](#toc) <a name=AnomalyDetection>Anomaly Detection</a> Interview Questions
#### Q1: Explain what is Anomaly Detection? ⭐
##### Answer:
**Anomaly detection** (or outlier detection) is the identification of rare items, events or observations which raise suspicions by differing significantly from the majority of the data.

![](https://miro.medium.com/max/732/1*J-ds9KYQBheiBaIJn78seg.gif)

**Source:** _towardsdatascience.com_

#### Q2: Why do we care about Anomalies? ⭐⭐
##### Answer:
* The goal of anomaly detection is to identify cases that are unusual within data that is seemingly comparable hence anomaly detection can be used effectively as a tool for risk mitigation and fraud detection. 
* When preparing datasets for machine learning models, it is really important to detect all the outliers and either get rid of them or analyze them to know why you had them there in the first place.

**Source:** _towardsdatascience.com_

#### Q3: What's the difference between _Normalisation_ and _Standardisation_? ⭐⭐
##### Answer:
**Normalization** rescales the values into a range of \[0,1\].  This might be useful in some cases where all parameters need to have the same positive scale. However, the _outliers_ from the data set _are lost._

$$
X_{changed} = \frac{X - X_{min}}{X_{max}-X_{min}}
$$ 

**Standardization** rescales data to have a mean ($\mu$) of 0 and standard deviation ($\sigma$) of 1 (unit variance).

$$
X_{changed} = \frac{X - \mu}{\sigma}
$$        

For most applications standardization is recommended.

![](https://i.stack.imgur.com/WqU1U.png)

**Source:** _stats.stackexchange.com_

#### Q4: Why would you use the _Median_ as a measure of central tendency? ⭐⭐
##### Answer:
The **Median** is the most suitable measure of _central tendency_ for **skewed distributions** or distributions with **outliers**. For example, the median is often used as a measure of central tendency for income distributions, which are generally highly skewed.

Because the median only uses one or two values, it’s unaffected by extreme _outliers_ or _non-symmetric distributions_ of scores. In contrast, the **_mean_** and **_mode_** can vary in skewed distributions.

![https://miro.medium.com/max/754/0*wHMvuwRa_YF9SFwY.png](https://miro.medium.com/max/754/0*wHMvuwRa_YF9SFwY.png)

**Source:** _en.wikipedia.org_

#### Q5: Explain how to use _Standard Deviation_ for Anomalies Detection? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q6: What Are some _types_ of Anomalies? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q7: What are some _categories_ of outlier detection approaches? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q8: How to use _one-class SVM_ for Anomalies Detections? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: Explain the difference between _Outlier Detection_ vs _Novelty Detection_ ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: Compare *SVM* and *Logistic Regression* in handling outliers ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: How to use _Isolation Forest_ for Anomalies detection? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: What are some _advantages_ of using _Isolation Forest_ algorithm for outliers detection?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: How would you deal with _Outliers_ in your dataset? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: Imagine that you know there are _outliers_ in your data, would you use _Logistic Regression_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: How is *PCA* used for *Anomaly Detection*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: How does *Dictionary Learning* perform *Anomaly Detection*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: What types of _Robust Regression Algorithms_ do you know? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=Autoencoders>Autoencoders</a> Interview Questions
#### Q1: Describe the approach used in *Denoising Autoencoders* ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q2: How can *Neural Networks* be used to create *Autoencoders*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q3: Can you use *Batch Normalisation* in *Sparse Auto-encoders*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q4: What are the main differences between *Sparse Autoencoders* and *Convolution Autoencoders*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q5: What are some differences between the *Undercomplete Autoencoder* and the *Sparse Autoencoder*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q6: How can *Neural Networks* be _Unsupervised_? 
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=Bias&Variance>Bias & Variance</a> Interview Questions
#### Q1: What is _Bias_ in Machine Learning? ⭐⭐
##### Answer:
In supervised machine learning an algorithm learns a model from training data.

The goal of any supervised machine learning algorithm is to best estimate the mapping function (f) for the output variable (Y) given the input data (X). The mapping function is often called the target function because it is the function that a given supervised machine learning algorithm aims to approximate.

**Bias** are **the simplifying assumptions** made by a model to make the target function easier to learn.

Generally, linear algorithms have a high bias making them fast to learn and easier to understand but generally less flexible.

* Examples of **low\-bias** machine learning algorithms include: Decision Trees, k\-Nearest Neighbors and [Support Vector Machines](https://machinelearningmastery.com/support-vector-machines-for-machine-learning/).

* Examples of **high\-bias** machine learning algorithms include: Linear Regression, Linear Discriminant Analysis and Logistic Regression.

**Source:** _machinelearningmastery.com_

#### Q2: What is the *Bias-Variance* tradeoff? ⭐⭐
##### Answer:
* **High Bias** can cause an algorithm to miss the relevant relations between features and target outputs (*underfitting*).
* **High Variance** may result from an algorithm modeling random noise in the training data (*overfitting*).
![https://community.alteryx.com/t5/image/serverpage/image-id/52874iE986B6E19F3248CF?v=v2](https://community.alteryx.com/t5/image/serverpage/image-id/52874iE986B6E19F3248CF?v=v2)


* The **Bias-Variance tradeoff** is a central problem in _supervised learning_. Ideally, a model should be able to accurately capture the regularities in its training data, but also generalize well to unseen data.
* It is called a *tradeoff* because it is typically impossible to do both simultaneously:  
  * Algorithms with _high variance_ will be prone to _overfitting_ the dataset, but 
  * Algorithms with *high bias* will _underfit_ the dataset.

![bias_variance_tradeoff](https://miro.medium.com/max/883/1*8sV6Sr9uc0Ef39YBivLzrw.jpeg)

**Source:** _en.wikipedia.org_

#### Q3: Provide an intuitive explanation of the _Bias-Variance Tradeoff_ ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q4: Name some types of _Data Biases_ in Machine Learning? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q5: What to do if you have _High Variance Problem_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q6: What to do if you have _High Bias Problem_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q7: What's the difference between _Bagging_ and _Boosting_ algorithms? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q8: How can you relate the _KNN Algorithm_ to the _Bias-Variance tradeoff_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: What is the *Bias Error*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: What is the *Variance Error*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: When you sample, what potential _Sampling Biases_ could you be inflicting? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=BigData>Big Data</a> Interview Questions
## [[⬆]](#toc) <a name=Big-ONotation>Big-O Notation</a> Interview Questions
#### Q1: What is _Big O_ notation? ⭐
##### Answer:
**Big-O** notation (also called "asymptotic growth" notation) is a relative representation of the complexity of an algorithm. It shows how an algorithm *scales* based on input size. We use it to talk about how thing _scale_. Big O complexity can be visualized with this graph:


![](https://i.stack.imgur.com/WcBRI.png)


**Source:** _stackoverflow.com_

#### Q2: Provide an example of <code><i>O</i>(<i>1</i>)</code> algorithm ⭐
##### Answer:
Say we have an array of `n` elements:

```cs
int array[n];
```

If we wanted to access the first (or any) element of the array this would be <code><i>O</i>(<i>1</i>)</code> since it doesn't matter how big the array is, it always takes the same constant time to get the first item:
```cs
x = array[0];
```

**Source:** _stackoverflow.com_

#### Q3: What is Worst Case? ⭐⭐
##### Answer:
Big-O is often used to make statements about functions that measure the worst case behavior of an algorithm. **Worst case** analysis gives the maximum number of basic operations that have to be performed during execution of the algorithm. It assumes that the input is in the _worst possible state_ and maximum work has to be done to put things right.

**Source:** _stackoverflow.com_

#### Q4: What the heck does it mean if an operation is <code><i>O</i>(<i>log n</i>)</code>? ⭐⭐
##### Answer:
**<code><i>O</i>(<i>log n</i>)</code>** means for every element, you're doing something that only needs to look at **log N** of the elements. This is usually because you know something about the elements that let you make an _efficient choice_ (for example to reduce a _search space_). 
The most common attributes of logarithmic running\-time function are that:
*   the choice of the next element on which to perform some action is one of several possibilities, and
*   only one will need to be chosen

or

*   the elements on which the action is performed are digits of `n`

Most efficient sorts are an example of this, such as **merge sort**. ​It is `O(log n)` when we do divide and conquer type of algorithms e.g binary search. Another example is **quick sort** where each time we divide the array into two parts and each time it takes `O(N)` time to find a pivot element. Hence it `N O(log N)`

Plotting `log(n)` on a plain piece of paper, will result in a graph where the rise of the curve decelerates as `n` increases:
![](https://i.stack.imgur.com/qPNNp.png)


**Source:** _stackoverflow.com_

#### Q5: Why do we use Big O notation to compare algorithms?  ⭐⭐
##### Answer:
The fact is it's difficult to determine the exact runtime of an algorithm. It depends on the speed of the computer processor. So instead of talking about the runtime directly, we use Big O Notation to talk about _how quickly the runtime grows_ depending on input size.

With Big O Notation, we use the size of the input, which we call `n`. So we can say things like the runtime grows “on the order of the size of the input” (<code><i>O</i>(<i>n</i>)</code>) or “on the order of the square of the size of the input” (<code><i>O</i>(<i>n</i><sup>2</sup>)</code>). Our algorithm may have steps that seem expensive when `n` is small but are eclipsed eventually by other steps as `n` gets larger. For Big O Notation analysis, we care more about the stuff that grows fastest as the input grows, because everything else is quickly eclipsed as `n` gets very large.

**Source:** _medium.com_

#### Q6: What exactly would an <code><i>O</i>(<i>n</i><sup>2</sup>)</code> operation do? ⭐⭐
##### Answer:
**<code><i>O</i>(<i>n</i><sup>2</sup>)</code>** means for every element, you're doing something with _every_ other element, such as comparing them. Bubble sort is an example of this.

**Source:** _stackoverflow.com_

#### Q7: What is complexity of this code snippet? ⭐⭐
##### Details:
Let's say we wanted to find a number in the list:
```js
for (int i = 0; i < n; i++){
    if(array[i] == numToFind){ return i; }
}
```
What will be the time complexity (Big O) of that code snippet?

##### Answer:
This would be <code><i>O</i>(<i>n</i>)</code> since at most we would have to look through the entire list to find our number. The Big-O is still <code><i>O</i>(<i>n</i>)</code> even though we might find our number the first try and run through the loop once because Big-O describes the upper bound for an algorithm.

**Source:** _stackoverflow.com_

#### Q8: What is complexity of `push` and `pop` for a Stack implemented using a LinkedList? ⭐⭐
##### Answer:
<code><i>O</i>(<i>1</i>)</code>. Note, you don't have to insert at the end of the list. If you insert at the front of a (singly-linked) list, they are both `O(1)`.

Stack contains 1,2,3:

```py
[1]->[2]->[3]
```

Push 5:

```js
[5]->[1]->[2]->[3]
```

Pop:

```js
[1]->[2]->[3] // returning 5
```


**Source:** _stackoverflow.com_

#### Q9: Explain the difference between _`O(1)`_ vs _`O(n)`_ space complexities  ⭐⭐
##### Answer:
Let's consider a traversal algorithm for traversing a list.

* <code><i>O</i>(<i>1</i>)</code> denotes _constant_ space use: the algorithm allocates the same number of pointers irrespective to the list size. That will happen if we move (reuse) our pointer along the list.
* In contrast, <code><i>O</i>(<i>n</i>)</code> denotes _linear_ space use: the algorithm space use grows together with respect to the input size `n`. That will happen if let's say for some reason the algorithm needs to allocate 'N' pointers (or other variables) when traversing a list.

**Source:** _stackoverflow.com_

#### Q10: What is the big O notation of this function? ⭐⭐
##### Details:
Consider:
```js
f(x) = log n + 3n
```
What is the big O notation of this function?

##### Answer:
It is simply <code><i>O</i>(<i>n</i>)</code>.

When you have a composite of multiple parts in Big O notation which are added, you have to choose the biggest one. In this case it is _`O(3n)`_, but there is no need to include constants inside parentheses, so we are left with _`O(n)`_.

**Source:** _stackoverflow.com_

#### Q11: What is an algorithm? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: What is complexity of this code snippet? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: What is the time complexity for "Hello, World" function? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: What is meant by "Constant Amortized Time" when talking about time complexity of an algorithm? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: Why do we use Big O instead of Big Theta (Θ)? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: Name some types of Big O complexity and corresponding algorithms ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: What is complexity of "Reading a Book"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: Explain your understanding of "Space Complexity" with examples ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: What is the difference between Lower bound and Tight bound? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: What does it mean if an operation is <code><i>O</i>(<i>n!</i>)</code>? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: Provide an example of algorithm with time complexity of <code><i>O</i>(<i>c</i><sup>k</sup>)</code>? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: What are some algorithms which we use daily that has _`O(1)`_, _`O(n log n)`_ and _`O(log n)`_ complexities? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=Classification>Classification</a> Interview Questions
#### Q1: Why Naive Bayes is called _Naive_? ⭐⭐
##### Answer:
We call it **naive** because its assumptions (it assumes that all of the features in the dataset are equally important and independent) are really optimistic and rarely true in most real-world applications:
- we consider that these _predictors_ are _independent_
- we consider that all the predictors have an _equal effect_ on the outcome (like the day being windy does not have more importance in deciding to play golf or not)

**Source:** _towardsdatascience.com_

#### Q2: What is a *Perceptron*? ⭐⭐
##### Answer:
* A **Perceptron** is a fundamental unit of a Neural Network that is also a single-layer Neural Network.
* Perceptron is a linear _classifier_. Since it uses already labeled data points, it is a *supervised learning algorithm*.  
* The _activation function_ applies a step rule (convert the numerical output into +1 or -1) to check if the output of the weighting function is greater than zero or not.

A **Perceptron** is shown in the figure below:

![perception](https://www.programmersought.com/images/258/633dca25508a646a6df343339c3d4eaa.png)


**Source:** _towardsdatascience.com_

#### Q3: What is a _Decision Boundary_? ⭐⭐
##### Answer:
A **decision boundary** is a line or a hyperplane that separates the classes. This is what we expect to obtain from _logistic regression_, as with any other classifier. With this, we can figure out some way to split the data to allow for an accurate prediction of a given observation’s class using the available information.

In the case of a generic two-dimensional example, the split might look something like this: 

![](https://miro.medium.com/max/340/0*hyR0M6QP5OvedMkd.png)

**Source:** _medium.com_

#### Q4: What types of _Classification Algorithms_ do you know? ⭐⭐
##### Answer:
- **Logistic regression**: ideally used for classification of _binary_ variables. Implements the _sigmoid function_ to calculate the probability that a data point belongs to a certain class. 

- **K-Nearest Neighbours (kNN)**: calculate the distance of one data point from every other data point and then takes a majority vote from _k-nearest neighbors_ of each data points to classify the output.

- **Decision trees**: use multiple _if-else statements_ in the form of a tree structure that includes _nodes_ and _leaves_. The nodes breaking down the one major structure into smaller structures and eventually providing the final outcome.

- **Random Forest**: uses multiple _decision trees_ to predict the outcome of the target variable. Each decision tree provides its own outcome and then it takes the majority vote to classify the final outcome. 

- **Support Vector Machines**: it creates an _n-dimensional space_ for the _n number of features_ in the dataset and then tries to create the hyperplanes such that it divides and classifies the data points with the maximum margin possible.

**Source:** _www.upgrad.com_

#### Q5: What is the difference between _KNN_ and _K-means Clustering_? ⭐⭐
##### Answer:
- **_K-nearest neighbors_** or _KNN_ is a _supervised classification algorithm_. This means that we need labeled data to classify an unlabeled data point. It attempts to classify a data point based on its proximity to other `K`-data points in the feature space.

- **_K-means Clustering_** is an _unsupervised classification algorithm_. It requires only a set of unlabeled points and a threshold `K`, so it gathers and groups data into `K` number of clusters.

**Source:** _www.quora.com_

#### Q6: How do you choose the optimal _k_ in _k-NN_? ⭐⭐
##### Answer:
There is not a rule of thumb to choose a standard optimal **_k_**. This value depends and varies from dataset to dataset, but as a general rule, the main goal is to keep it:
- small enough to exclude the samples of the other classes but 
- large enough to minimize any noise in the data.

A way to looking for this optimal parameter, commonly called the _Elbow method_, consist in creating a _for loop_ that trains various **_KNN_** models with different **_k values_**, keeping track of the error for each of these models, and use the model with the **_k value_** that achieves the best accuracy.

![https://i.stack.imgur.com/ct2ie.jpg](https://i.stack.imgur.com/ct2ie.jpg)

**Source:** _medium.com_

#### Q7: How would you make a prediction using a _Logistic Regression_ model? ⭐⭐
##### Answer:
In **Logistic regression** models, we are modeling the _probability_ that an input `(X)` belongs to the default class `(Y=1)`, that is to say:

$$
P(X) = P(Y=1|X)
$$

where the `P(X)` values are given by the **_logistic function_**,

$$
P(X) = \frac{e^{\beta_0 + \beta_1X}}{1 + e^{\beta_0 + \beta_1X}}
$$

The `β0` and `β1` values are estimated during the training stage using _maximum-likelihood_ estimation or _gradient descent_. Once we have it, we can make predictions by simply putting numbers into the _logistic regression equation_ and calculating a result.

For example, let's consider that we have a model that can predict whether a person is male or female based on their height, such as if `P(X) ≥ 0.5` the person is male, and if `P(X) < 0.5` then is female.  

During the training stage we obtain `β0 = -100` and `β1 = 0.6`, and we want to evaluate what's the probability that a person with a height of `150cm` is male, so with that intention we compute: 

$$
y = \frac{e^{-100 + 0.6\cdot 150}}{1 + e^{-100 + 0.6\cdot 150}} = 0.00004539 \cdots
$$

Given that logistic regression solves a _classification_ task, we can use directly this value to predict that the person is a female. 

**Source:** _machinelearningmastery.com_

#### Q8: Why would you use the _Kernel Trick_? ⭐⭐
##### Answer:
When it comes to **classification** problems, the goal is to establish a decision boundary that maximizes the margin between the classes. However, in the real world, this task can become difficult when we have to treat with **non-linearly separable data**. One approach to solve this problem is to perform a data transformation process, in which we map all the data points to a **higher dimension** find the boundary and make the classification.

That sounds alright, however, when there are more and more dimensions, computations within that space become more and more expensive. In such cases, the **kernel trick allows us to operate in the original feature space without computing the coordinates of the data** in a higher-dimensional space and therefore offers a more efficient and less expensive way to transform data into higher dimensions.

There exist different kernel functions, such as:
- _linear_, 
- _nonlinear_, 
- _polynomial_, 
- _radial basis function (RBF)_, and 
- _sigmoid_. 

Each one of them can be suitable for a particular problem depending on the data.  


**Source:** _medium.com_

#### Q9: What is the *Hinge Loss* in SVM? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: Name some _classification metrics_ and when would you use each one ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: What is the difference between a _Weak Learner_ vs a _Strong Learner_ and why they could be usefu? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: What's the difference between _Bagging_ and _Boosting_ algorithms? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: Provide an intuitive explanation of _Linear Support Vector Machines (SVMs)_ ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: Could you _convert_ Regression into Classification and vice versa? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: What's the difference between _One-vs-Rest_ and _One-vs-One_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: Can you choose a _classifier_ based on the _size of the training set_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: How would you use _Naive Bayes_ classifier for categorical features? What if some features are numerical? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: What's the difference between _Generative Classifiers_ and _Discriminative Classifiers_? Name some examples of each one ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: How does the _Naive Bayes_ classifier work? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: How does the _AdaBoost_ algorithm work? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: What's the difference between _Softmax_ and _Sigmoid_ functions? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: How do you use a supervised *Logistic Regression* for Classification? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: What is a *Confusion Matrix*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: How does *ROC* curve and *AUC* value help measure how good a model is? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: What are some advantages and disadvantages of using *AUC* to measure the _performance_ of the model? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q26: What is the *F-Score*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q27: How is _AUC - ROC_ curve used in classification problems?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q28: Name some advantages of using _Support Vector Machines_ vs _Logistic Regression_ for classification ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q29: When would you use _SVM_ vs _Logistic regression_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q30: Are there any problems using _Naive Bayes_ for Classification? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q31: What's the difference between _Random Oversampling_ and _Random Undersampling_ and when they can be used? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q32: How would you use a _Confusion Matrix_ for determining a model performance? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q33: How would you deal with classification on _Non-linearly Separable_ data? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q34: What are the trade-offs between the different types of _Classification Algorithms_? How would do you choose the best one? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q35: Compare _Naive Bayes_ vs with _Logistic Regression_ to solve classification problems ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q36: How would you _Calibrate Probabilities_ for a classification model? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q37: How would you choose an evaluation metric for an _Imbalanced classification_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q38: What is *AIC*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q39: Can _Logistic Regression_ be used for an _Imbalanced Classification_ problem? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q40: Why would you use _Probability Calibration_? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q41: What's the difference between _ROC_ and _Precision-Recall_ Curves? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q42: How to interpret _F-measure_ values? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=Clustering>Clustering</a> Interview Questions
#### Q1: Define what is *Clustering*? ⭐
##### Answer:
* **Cluster analysis** is also called **clustering**.
* It is the task of grouping a set of objects in such a way that *objects* in the same *cluster* are *more similar* to each other than to those in other clusters.
* Cluster analysis itself is *not* one specific algorithm, but the general task to be solved. It can be achieved by various algorithms that differ significantly in their understanding of what constitutes a cluster and how to efficiently find them.

![clustering](https://media.geeksforgeeks.org/wp-content/uploads/merge3cluster.jpg)

**Source:** _Handbook of Cluster Analysis from Chapman and Hall/CRC_

#### Q2: What is *Similarity-based Clustering*? ⭐⭐
##### Answer:
* Clustering, when the data are similar pairs of points is called **similarity-based clustering**.
* A typical example of similarity-based clustering is community detection in social networks, where the observations are individual links between people, which may be due to friendship, shared interests, and work relationships. The *strength* of a link can be the frequency of interactions, for example, communications by e-mail, phone, or other social media, co-authorships, or citations.
* In this clustering paradigm, the points to be clustered are not assumed to be part of a vector space. Their attributes (or features) are incorporated into a single dimension, the *link strength*, or *similarity*, which takes a numerical value $$S_{ij}$$ for each pair of points `i`, `j`. Hence, the natural representation for this problem is by means of the similarity matrix given below:
$$
S=[S_{ij}]_{i,j=1}^n
$$
The similarities are symmetric $$S_{ij} = S_{ji}$$ and nonnegative $$S_{ij} \geq 0$$.

**Source:** _Handbook of Cluster Analysis from Chapman and Hall/CRC_

#### Q3: Give examples of using *Clustering* to solve real-life problems ⭐⭐
##### Answer:
* **Identifying cancerous data:** Initially we take known samples of a cancerous and non-cancerous dataset, and label both the samples dataset. Then both the samples are mixed and different clustering algorithms are applied to the mixed samples dataset. It has been found through experiments that a cancerous dataset gives the best results with unsupervised non-linear clustering algorithms.
* **Search engines:** Search engines try to group similar objects in one cluster and the dissimilar objects far from each other. It provides results for the searched data according to the nearest similar object which is clustered around the data to be searched.
* **Wireless sensor network's based application:** Clustering algorithm can be used effectively in *Wireless Sensor Network's based application*. One application where it can be used is in *Landmine detection*. The clustering algorithm plays the role of finding the Cluster heads (or cluster center) which collects all the data in its respective cluster.

**Source:** _sites.google.com_

#### Q4: What is *Mean-Shift Clustering*? ⭐⭐
##### Answer:
* **Mean Shift** is a non-parametric feature-space analysis technique for locating the maxima of a *density function*. What we're trying to achieve here is, to keep shifting the window to a region of _higher density_.

![https://iq.opengenus.org/content/images/2019/02/pdf.png](https://iq.opengenus.org/content/images/2019/02/pdf.png)

* We can understand this algorithm by thinking of our data points to be represented as a probability density function. Naturally, in a probability function, higher density regions will correspond to the regions with more points, and lower density regions will correspond to the regions with less points.
In clustering, we need to find clusters of points, i.e the regions with a lot of points together. More points together mean higher density. Hence, we observe that clusters of points are more like the higher density regions in our probability density function.

 So, we must iteratively go from lower density to higher density regions, in order to find our clusters.

* The mean shift method is an iterative method, and we start with an initial estimate `x`. Let a *kernel function* $$K(x_i - x)$$ be given. This function determines the weight of nearby points for re-estimation of the mean. Typically a *Gaussian kernel* on the distance to the current estimate is used,
$$
K(x_i-x)= e^{-c|x_i-x|^2}
$$
The weighted mean of the density in the window determined by `K` is
$$
m(x) = \frac{\sum_{x_i \in N(x)} K(x_i - x) x_i}{\sum_{x_i \in N(x) K(x_i - x)}}
$$
where `N(x)` is the neighborhood of `x`, a set of points for which $$K(x_i) \neq 0$$.

* The difference `m(x) - x` is called *mean shift*. The *mean-shift algorithm* now sets $$m(x) \to x$$, and repeats the estimation until `m(x)` converges. It means, after a sufficient number of steps, the position of the centroid of all the points, and the current location of the window will coincide. This is when we reach convergence, as no new points are added to our window in this step.


**Source:** _en.wikipedia.org_

#### Q5: What are *Self-Organizing Maps*? ⭐⭐
##### Answer:
* **Self-Organizing Maps** (**SOMs**) are a class of *self-organizing* clustering techniques.
* It is an _unsupervised form of artificial neural networks_. A self-organizing map consists of a set of neurons that are arranged in a rectangular or hexagonal grid. Each neuronal unit in the grid is associated with a numerical vector of fixed dimensionality. The learning process of a self-organizing map involves the adjustment of these vectors to provide a suitable representation of the input data.
* Self-organizing maps can be used for clustering numerical data in vector format.

![som](https://www.researchgate.net/profile/Mohamed-Zair/publication/329337931/figure/fig1/AS:915377227849728@1595254346086/Structural-model-of-self-organizing-map-neural-network-Figure-2-Experimental-benchmark.png)

**Source:** _medium.com_

#### Q6: Why do you need to perform *Significance Testing* in *Clustering*? ⭐⭐
##### Answer:
* **Significance testing** addresses an important aspect of cluster validation. Many cluster analysis methods will deliver clusterings even for homogeneous data. They assume implicitly that clustering has to be found, regardless of whether this is meaningful or not. 

>A critical and challenging question in cluster analysis is whether the identified clusters represent important underlying structure or are artifacts of natural sampling variation.

* **Significance testing** is performed to distinguish between a clustering that reflects meaningful _heterogeneity_ in the data and an artificial clustering of _homogeneous_ data.
* Significance testing is also used for more specific tasks in cluster analysis, such as; estimating the number of clusters, and for interpreting some or all of the individual clusters, to show the significance of the individual clusters.

**Source:** _www.ncbi.nlm.nih.gov_

#### Q7: What is the difference between a _Multiclass problem_ and a _Multilabel problem_? ⭐⭐
##### Answer:
**Multiclass classification** means a classification task with more than two classes; e.g., classify a set of images of fruits which may be oranges, apples, or pears. Multiclass classification makes the assumption that each sample is _assigned to one and only one label_: a fruit can be either an apple or a pear but not both at the same time.

**Multilabel classification** assigns to each sample a set of target labels. This can be thought of as predicting properties of a data-point that are _not mutually exclusive_, such as topics that are relevant for a document. A text might be about any of religion, politics, finance or education at the same time or none of these.

![https://i.stack.imgur.com/XghaO.png](https://i.stack.imgur.com/XghaO.png)

**Source:** _stats.stackexchange.com_

#### Q8: What is the _Jaccard Index_? ⭐⭐
##### Answer:
The **Jaccard index**, also known as the Jaccard similarity coefficient, is a statistic used for gauging the similarity and diversity of sample sets. The Jaccard coefficient measures **similarity** between finite sample sets, and is defined as the size of the intersection divided by the size of the union of the sample sets:

![https://wikimedia.org/api/rest_v1/media/math/render/svg/eaef5aa86949f49e7dc6b9c8c3dd8b233332c9e7](https://wikimedia.org/api/rest_v1/media/math/render/svg/eaef5aa86949f49e7dc6b9c8c3dd8b233332c9e7)

![https://upload.wikimedia.org/wikipedia/commons/c/c7/Intersection_over_Union_-_visual_equation.png](https://upload.wikimedia.org/wikipedia/commons/c/c7/Intersection_over_Union_-_visual_equation.png)

![](https://upload.wikimedia.org/wikipedia/commons/e/e6/Intersection_over_Union_-_poor%2C_good_and_excellent_score.png)

**Source:** _en.wikipedia.org_

#### Q9: What is the difference between the two types of *Hierarchical Clustering*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: While performing *K-Means* Clustering, how do you determine the value of *K*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: What are some different types of *Clustering Structures* that are used in *Clustering Algorithms*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: When would you use *Hierarchical Clustering* over *Spectral Clustering*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: Compare *Hierarchical Clustering* and *k-Means Clustering* ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: Where do the *Similarities* come from in *Similarity-based Clustering*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: What is a *Mixture Model*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: What is the *Mixture* in *Gaussian Mixture Model*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: What is *Latent Class Model*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: How would you perform an *Observation-Based Clustering* for *Time-Series Data*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: Name some pros and cons of _Mean Shift Clustering_ ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: How can *Evolutionary Algorithms* be used for *Clustering*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: What is _Silhouette Analysis_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: Why does *K-Means* have a higher *bias* when compared to *Gaussian Mixture Model*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: Explain how a cluster is formed in the *DBSCAN* Clustering Algorithm ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: What makes the distance measurement of *k-Medoids* better than *k-Means*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: When using various Clustering Algorithms, why is *Euclidean Distance* not a good metric in _High Dimensions_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q26: When would you use *Hierarchical Clustering* over *k-Means Clustering*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q27: How would you choose the number of *Clusters* when designing a *K-Medoid Clustering Algorithm*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q28: Explain the *Dirichlet Process Gaussian Mixture Model* ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q29: Why is *Euclidean Distance* not good for *Sparse Data*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q30: When would you use *Segmentation* over *Clustering*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q31: How to tell if data is _clustered_ enough for clustering algorithms to produce meaningful results? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q32: How to choose among the various clustering _Distance Measures_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q33: Explain the different frameworks used for *k-Means Clustering* ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q34: What is the motivation behind the *Expectation-Maximization Algorithm*? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q35: What is the relationship between *k-Means Clustering* and *PCA*? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=CostFunction>Cost Function</a> Interview Questions
#### Q1: Provide an analogy for a _Cost Function_ in real life ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q2: Explain what is _Cost (Loss) Function_ in Machine Learning? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q3: What is the difference between _Cost Function_ vs _Gradient Descent_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q4: What is the difference between _Objective function_, _Cost function_ and _Loss function_ ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q5: Why don’t we use _Mean Squared Error_ as a cost function in Logistic Regression? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q6: How would you fix Logistic Regression _Overfitting_ problem? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q7: What is the *Hinge Loss* in SVM? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q8: What type of *Cost Functions* do *Greedy Splitting* use? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: How would you choose the *Loss Function* for a Deep Learning model? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=DataStructures>Data Structures</a> Interview Questions
#### Q1: Define Stack ⭐
##### Answer:
A **Stack** is a container of objects that are inserted and removed according to the last-in first-out (**LIFO**) principle. In the pushdown stacks only two operations are allowed: push the item into the stack, and pop the item out of the stack.

There are basically three operations that can be performed on stacks. They are:
 
1. inserting an item into a stack (**push**). 
2. deleting an item from the stack (**pop**). 
3. displaying the contents of the stack (**peek** or **top**).

A stack is a limited access data structure - elements can be added and removed from the stack only at the top. push adds an item to the top of the stack, pop removes the item from the top. A helpful analogy is to think of a stack of books; you can remove only the top book, also you can add a new book on the top.

![](https://user-images.githubusercontent.com/13550565/85218531-fea33d80-b3cd-11ea-8ba4-77c37d446d07.png)


**Source:** _www.cs.cmu.edu_

#### Q2: Explain why Stack is a recursive data structure ⭐
##### Answer:
A **stack** is a **recursive** data structure, so it's:

* a stack is either empty or
* it consists of a top and the rest which is a stack by itself;

**Source:** _www.cs.cmu.edu_

#### Q3: Define Linked List ⭐
##### Answer:
A **linked list** is a linear data structure where each element is a separate object. Each element (we will call it a **node**) of a list is comprising of two items - the **data** and a **reference (pointer)** to the next node. The last node has a reference to **null**. The entry point into a linked list is called the **head** of the list. It should be noted that _head is not a separate node,_ but the reference to the first node. If the list is empty then the head is a null reference.

**Source:** _www.cs.cmu.edu_

#### Q4: Name some characteristics of Array Data Structure ⭐
##### Answer:
Arrays are: 
* **Finite (fixed-size)** - An array is finite because it contains only limited number of elements.
* **Order** -All the elements are stored one by one , in contiguous  location of computer memory in a linear order and fashion
* **Homogenous** - All  the elements of an array are of  same  data types only  and hence  it is termed as collection of homogenous

**Source:** _codelack.com_

#### Q5: What is Queue? ⭐
##### Answer:
A **queue** is a container of objects (a _linear_ collection) that are inserted and removed according to the first-in first-out (FIFO) principle. The process to add an element into queue is called **Enqueue** and the process of removal of an element from queue is called **Dequeue**.

![](https://user-images.githubusercontent.com/13550565/85218641-9d2f9e80-b3ce-11ea-8c1b-a9c058057a70.png)


**Source:** _www.cs.cmu.edu_

#### Q6: What is Heap? ⭐
##### Answer:
A **Heap** is a special Tree-based data structure which is an almost complete tree that satisfies the heap property:

* in a **max heap**, for any given node C, if P is a parent node of C, then the key (the value) of P is greater than or equal to the key of C. 
* In a **min heap**, the key of P is less than or equal to the key of C. The node at the "top" of the heap (with no parents) is called the root node.


A common implementation of a heap is the binary heap, in which the tree is a **binary tree.**


![](https://www.techiedelight.com/wp-content/uploads/2016/11/Min-Max-Heap.png)


**Source:** _www.geeksforgeeks.org_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
#### Q7: What is Hash Table? ⭐
##### Answer:
A **hash table** (hash map) is a data structure that implements an **associative** array abstract data type, a **structure** that can **map keys to values**. Hash tables implement an associative array, which is indexed by arbitrary objects (keys). A hash table uses a **hash function** to compute an **index**, also called a **hash value**, into an **array of buckets** or slots, from which the desired **value** can be found.


![](https://i.stack.imgur.com/0yjYd.png)


**Source:** _en.wikipedia.org_

#### Q8: What is Priority Queue? ⭐
##### Answer:
A **priority queue** is a data structure that stores **priorities** (comparable values) and perhaps associated information.  A **priority queue** is different from a "normal" queue, because instead of being a "first-in-first-out" data structure, values come out in order by **priority**. Think of a priority queue as a kind of bag that holds priorities. You can put one in, and you can take out the current highest priority.

![](https://cdn.programiz.com/sites/tutorial2program/files/Introduction.png)


**Source:** _pages.cs.wisc.edu_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
#### Q9: Define Tree Data Structure ⭐
##### Answer:
**Trees** are well-known as a _non-linear_ data structure. They don’t store data in a linear way. They organize data _hierarchically_.

A **tree** is a collection of entities called **nodes**. Nodes are connected by **edges**. Each node contains a **value** or **data** or **key**, and it may or may not have a **child** node. The first node of the tree is called the **root**. **Leaves** are the last nodes on a tree. They are nodes without children.



![](https://miro.medium.com/max/975/1*PWJiwTxRdQy8A_Y0hAv5Eg.png)


**Source:** _www.freecodecamp.org_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
#### Q10: What is a Graph? ⭐
##### Answer:
A **graph** is a common data structure that consists of a finite set of **nodes** (or **vertices**) and a set of **edges** connecting them. A pair `(x,y)` is referred to as an edge, which communicates that the **x vertex** connects to the **y vertex**.

Graphs are used to solve real-life problems that involve representation of the problem space as a **network**. Examples of networks include telephone networks, circuit networks, social networks (like LinkedIn, Facebook etc.).



![](https://miro.medium.com/max/1640/1*4s5Z7gVwVqmKcslgiamRyw.png)


**Source:** _www.educative.io_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
#### Q11: What is String in Data Structures? ⭐
##### Answer:
A **string** is generally considered as a **data type** and is often implemented as an **array data structure** of bytes (or words) that stores a sequence of elements, typically characters, using some character encoding. String may also denote more general arrays or other sequence (or list) data types and structures.

**Source:** _dev.to_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
#### Q12: What is Trie? ⭐
##### Answer:
**Trie** (also called **digital tree **or **prefix tree**) is a _tree-based data structure_, which is used for efficient _retrieval_ of a key in a large data-set of strings. Unlike a binary search tree, no node in the tree stores the key associated with that node; instead, its position in the tree defines the key with which it is associated; i.e., **the value of the key is distributed across the structure**. All the descendants of a node have a common prefix of the string associated with that node, and the root is associated with the empty string. Each complete English word has an arbitrary integer value associated with it (see image).

<br/>

![](https://upload.wikimedia.org/wikipedia/commons/thumb/a/ae/Patricia_trie.svg/1200px-Patricia_trie.svg.png)
<br/>

**Source:** _medium.com_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
#### Q13: Define Binary Tree ⭐
##### Answer:
A normal tree has no restrictions on the number of children each node can have. A **binary tree** is made of nodes, where each node contains a "left" pointer, a "right" pointer, and a data element. 

There are three different types of binary trees:

* **Full binary tree**: Every node other than leaf nodes has 2 child nodes.
* **Complete binary tree**: All levels are filled except possibly the last one, and all nodes are filled in as far left as possible.
* **Perfect binary tree**: All nodes have two children and all leaves are at the same level.



![](https://study.com/cimages/multimages/16/0e0646ba-30e5-40d9-b45c-a138f038f05b_full_complete_perfect.png)



**Source:** _study.com_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
#### Q14: Why and when should I use Stack or Queue data structures instead of Arrays/Lists? ⭐⭐
##### Answer:
Because they help manage your data in more a _particular_ way than arrays and lists. It means that when you're debugging a problem, you won't have to wonder if someone randomly inserted an element into the middle of your list, messing up some invariants.

Arrays and lists are random access. They are very flexible and also easily *corruptible*. If you want to manage your data as FIFO or LIFO it's best to use those, already implemented, collections.

More practically you should:
* Use a queue when you want to get things out in the order that you put them in (FIFO)
* Use a stack when you want to get things out in the reverse order than you put them in (LIFO)
* Use a list when you want to get anything out, regardless of when you put them in (and when you don't want them to automatically be removed).

**Source:** _stackoverflow.com_

#### Q15: What is Complexity Analysis of Queue operations?  ⭐⭐
##### Answer:
* Queues offer random access to their contents by shifting the first element off the front of the queue. You have to do this repeatedly to access an arbitrary element somewhere in the queue. Therefore, **access** is <code><i>O</i>(<i>n</i>)</code>.
* Searching for a given value in the queue requires iterating until you find it. So **search** is <code><i>O</i>(<i>n</i>)</code>.
* Inserting into a queue, by definition, can only happen at the back of the queue, similar to someone getting in line for a delicious Double-Double burger at In 'n Out. Assuming an efficient queue implementation, queue **insertion** is <code><i>O</i>(<i>1</i>)</code>.
* Deleting from a queue happens at the front of the queue. Assuming an efficient queue implementation, queue **deletion** is `<code><i>O</i>(<i>1</i>)</code>.

**Source:** _github.com_

#### Q16: What are some types of Queue? ⭐⭐
##### Answer:
 Queue can be classified into following types:

* **Simple Queue** - is a linear data structure in which removal of elements is done in the same order they were inserted i.e., the element will be removed first which is inserted first.

![](https://scanftree.com/Data_Structure/queues.png)

* **Circular Queue** - is a linear data structure in which the operations are performed based on FIFO (First In First Out) principle and the last position is connected back to the first position to make a circle. It is also called **Ring Buffer**. Circular queue avoids the wastage of space in a regular queue implementation using arrays.


![](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d9/Ring_buffer.svg/794px-Ring_buffer.svg.png)


* **Priority Queue** - is a type of queue where each element has a priority value and the deletion of the elements is depended upon the priority value

![](https://www.aoprogrammer.com/wp-content/uploads/2018/07/enqueue-priority-queue.png)

  * In case of **max-priority queue**, the element will be deleted first which has the largest priority value
  * In case of **min-priority queue** the element will be deleted first which has the minimum priority value.
* **De-queue (Double ended queue)** - allows insertion and deletion from both the ends i.e. elements can be added or removed from rear as well as front end.

![](https://i.imgur.com/AF3RVpP.png)

  * **Input restricted deque** - In input restricted double ended queue, the insertion operation is performed at only one end and deletion operation is performed at both the ends.

![](https://i.imgur.com/dSJUHFE.png)

  * **Output restricted deque** - In output restricted double ended queue, the deletion operation is performed at only one end and insertion operation is performed at both the ends.


![](https://i.imgur.com/vyHyffe.png)

 


**Source:** _www.ques10.com_

#### Q17: What are some types of Linked List? ⭐⭐
##### Answer:
* A **singly linked list**

![](https://www.andrew.cmu.edu/course/15-121/lectures/Linked%20Lists/pix/linkedlist.bmp)
* A **doubly linked list** is a list that has two references, one to the next node and another to previous node.

![](https://www.andrew.cmu.edu/course/15-121/lectures/Linked%20Lists/pix/doubly.bmp)
* A **multiply linked list** - each node contains two or more link fields, each field being used to connect the same set of data records in a different order of same set(e.g., by name, by department, by date of birth, etc.).
* A **circular linked list** - where last node of the list points back to the first node (or the head) of the list.

![](https://i2.wp.com/algorithms.tutorialhorizon.com/files/2016/03/Circular-Linked-List.png)


**Source:** _www.cs.cmu.edu_

#### Q18: What are Dynamic Arrays? ⭐⭐
##### Answer:
A **dynamic array** is an array with a big improvement: _automatic resizing_.

One limitation of arrays is that they're _fixed_ size, meaning you need to specify the number of elements your array will hold ahead of time. A dynamic array expands as you add more elements. So you don't need to determine the size ahead of time.

**Source:** _www.interviewcake.com_

#### Q19: Return the N-th value of the Fibonacci sequence. Solve in _`O(n)`_ time ⭐⭐
##### Answer:
The easiest solution that comes to mind here is iteration: 

```js
function fib(n){
  let arr = [0, 1];
  for (let i = 2; i < n + 1; i++){
    arr.push(arr[i - 2] + arr[i -1])
  }
 return arr[n]
}
```
And output:
```
fib(4)
=> 3
```


Notice that two first numbers can not really be effectively generated by a for loop, because our loop will involve adding two numbers together, so instead of creating an empty array we assign our arr variable to `[0, 1]` that we know for a fact will always be there. After that we create a loop that starts iterating from i = 2 and adds numbers to the array until the length of the array is equal to `n + 1`. Finally, we return the number at n index of array.

**Source:** _medium.com_

##### Complexity Analysis:
**Time Complexity**: O(n)
**Space Complexity**: O(n)

An algorithm in our iterative solution takes linear time to complete the task. Basically we iterate through the loop n-2 times, so Big O (notation used to describe our worst case scenario) would be simply equal to O`(n)` in this case. The space complexity is `O(n)`.
##### Implementation:
##### _JS_

```js
function fib(n){
  let arr = [0, 1]
  for (let i = 2; i < n + 1; i++){
    arr.push(arr[i - 2] + arr[i -1])
  }
 return arr[n]
}
```

##### _Java_

```java
double fibbonaci(int n){
    double prev=0d, next=1d, result=0d;
    for (int i = 0; i < n; i++) {
        result=prev+next;
        prev=next;
        next=result;
    }
    return result;
}
```

##### _PY_

```py
def fib_iterative(n):
    a, b = 0, 1
    while n > 0:
        a, b = b, a + b
        n -= 1
    return a
```

#### Q20: Name some disadvantages of Linked Lists? ⭐⭐
##### Answer:
Few disadvantages of linked lists are :

* They use more memory than arrays because of the storage used by their pointers.
* Difficulties arise in linked lists when it comes to reverse traversing. For instance, singly linked lists are cumbersome to navigate backwards and while doubly linked lists are somewhat easier to read, memory is wasted in allocating space for a back-pointer.
* Nodes in a linked list must be read in order from the beginning as linked lists are inherently sequential access.
* Random access has linear time.
* Nodes are stored incontiguously (no or poor cache locality), greatly increasing the time required to access individual elements within the list, especially with a CPU cache.
* If the link to list's node is accidentally destroyed then the chances of data loss after the destruction point is huge. Data recovery is not possible.
* Search is linear versus logarithmic for sorted arrays and binary search trees.
* Different amount of time is required to access each element.
* Not easy to sort the elements stored in the linear linked list.

**Source:** _www.quora.com_

#### Q21: Return the N-th value of the Fibonacci sequence Recursively ⭐⭐
##### Answer:
Recursive solution looks pretty simple (see code).

Let’s look at the diagram that will help you understand what’s going on here with the rest of our code. Function fib is called with argument 5:

![](https://miro.medium.com/max/1400/1*LNBBacuaBFOVZXUV6VgEEg.png)

Basically our **fib** function will continue to recursively call itself creating more and more branches of the tree until it hits the base case, from which it will start summing up each branch’s return values bottom up, until it finally sums them all up and returns an integer equal to 5.

**Source:** _medium.com_

##### Complexity Analysis:
**Time Complexity**: O(2^n)

In case of recursion the solution take **exponential** time, that can be explained by the fact that the size of the tree exponentially grows when n increases. So for every additional element in the Fibonacci sequence we get an increase in function calls. Big O in this case is equal to <code><i>O</i>(<i>2</i><sup>n</sup>)</code>. Exponential Time complexity denotes an algorithm whose growth doubles with each addition to the input data set. 
##### Implementation:
##### _JS_

```js
function fib(n) {
  if (n < 2){
    return n
  }
  return fib(n - 1) + fib (n - 2)
}
```

##### _Java_

```java
public int fibonacci(int n)  {
    if (n < 2) return n;

    return fibonacci(n - 1) + fibonacci(n - 2);
}
```

##### _PY_

```py
def F(n):
    if n == 0: return 0
    elif n == 1: return 1
    else: return F(n-1)+F(n-2)
```

#### Q22: What is the space complexity of a Hash Table? ⭐⭐
##### Answer:
The space complexity of a datastructure indicates how much space it occupies in relation to the amount of elements it holds. For example a space complexity of `O(1)` would mean that the datastructure alway consumes constant space no matter how many elements you put in there. `O(n)` would mean that the space consumption grows linearly with the amount of elements in it.

A **hashtable** typically has a space complexity of `O(n)`.

**Source:** _stackoverflow.com_

#### Q23: What is Binary Heap? ⭐⭐
##### Answer:
A **Binary Heap** is a _Binary Tree_ with following properties:

* It’s a _complete_ tree (all levels are completely filled except possibly the last level and the last level has all keys as left as possible). This property of Binary Heap makes them suitable to be stored in an array.
* A Binary Heap is either **Min Heap** or **Max Heap**. In a Min Binary Heap, the key at root must be minimum among all keys present in Binary Heap. The same property must be recursively true for all nodes in Binary Tree. Max Binary Heap is similar to MinHeap.

```js
            10                      10
         /      \               /       \  
       20        100          15         30  
      /                      /  \        /  \
    30                     40    50    100   40
```

**Source:** _www.geeksforgeeks.org_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
#### Q24: What is Binary Search Tree? ⭐⭐
##### Answer:
**Binary search tree** is a data structure that quickly allows to maintain a _sorted list_ of numbers.

* It is called a _binary tree_ because each tree node has maximum of two children.
* It is called a _search tree_ because it can be used to search for the presence of a number in `O(log n)` time.

The properties that separates a binary search tree from a regular binary tree are:

* All nodes of left subtree are less than root node
* All nodes of right subtree are more than root node
* Both subtrees of each node are also BSTs i.e. they have the above two properties


![](https://cdn.programiz.com/sites/tutorial2program/files/bst-vs-not-bst.jpg)


**Source:** _www.programiz.com_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
#### Q25: What is the difference between Strings vs. Char arrays? ⭐⭐
##### Answer:
**Char arrays**: 
* Static-sized
* Fast access
* Few built-in methods to manipulate strings
* A char array doesn’t define a data type

**Strings**:
* Slower access
* Define a data type
* Dynamic allocation
* More built-in functions to support string manipulations

**Source:** _dev.to_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
#### Q26: How to implement a _Tree_ data-structure? Provide some code. ⭐⭐
##### Answer:
That is a basic (generic) tree structure that can be used for `String` or any other object:

**Source:** _stackoverflow.com_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
##### Implementation:
##### _Java_

```java
public class Tree<T> {
    private Node<T> root;

    public Tree(T rootData) {
        root = new Node<T>();
        root.data = rootData;
        root.children = new ArrayList<Node<T>>();
    }

    public static class Node<T> {
        private T data;
        private Node<T> parent;
        private List<Node<T>> children;
    }
}
```

##### _PY_


Generic Tree:

```py
class Tree(object):
    "Generic tree node."
    def __init__(self, name='root', children=None):
        self.name = name
        self.children = []
        if children is not None:
            for child in children:
                self.add_child(child)
    def __repr__(self):
        return self.name
    def add_child(self, node):
        assert isinstance(node, Tree)
        self.children.append(node)
#    *
#   /|\
#  1 2 +
#     / \
#    3   4
t = Tree('*', [Tree('1'),
               Tree('2'),
               Tree('+', [Tree('3'),
                          Tree('4')])])
```
Binary tree:

```py
class Tree:
    def __init__(self):
        self.left = None
        self.right = None
        self.data = None
```

#### Q27: Convert a _Singly Linked List_ to _Circular Linked List_ ⭐⭐
##### Answer:
To convert a singly linked list to a circular linked list, we will set the next pointer of the tail node to the head pointer.

*   Create a copy of the head pointer, let's say `temp`.
*   Using a loop, traverse linked list till tail node (last node) using temp pointer.
*   Now set the next pointer of the tail node to head node. `temp->next = head`

**Source:** _www.techcrashcourse.com_

##### Implementation:
##### _PY_

```py
def convertTocircular(head):
    # declare a node variable
    # start and assign head
    # node into start node.
    start = head
    
    # check that
    while head.next
    # not equal to null then head
    # points to next node.
    while(head.next is not None):
      head = head.next
    
    #
    if head.next points to null
    # then start assign to the
    # head.next node.
    head.next = start
    return start
```


#### Q28: What's the difference between the data structure Tree and Graph? ⭐⭐
##### Answer:
**Graph:**
* Consists of a set of vertices (or nodes) and a set of edges connecting some or all of them
* Any edge can connect any two vertices that aren't already connected by an identical edge (in the same direction, in the case of a directed graph)
* Doesn't have to be connected (the edges don't have to connect all vertices together): a single graph can consist of a few disconnected sets of vertices
* Could be directed or undirected (which would apply to all edges in the graph)

**Tree:**
* A type of graph (fit with in the category of Directed Acyclic Graphs (or a DAG))
* Vertices are more commonly called "nodes"
* Edges are directed and represent an "is child of" (or "is parent of") relationship
* Each node (except the root node) has exactly one parent (and zero or more children)
* Has exactly one "root" node (if the tree has at least one node), which is a node without a parent
* Has to be connected
* Is acyclic, meaning it has no cycles: "a cycle is a path [AKA sequence] of edges and vertices wherein a vertex is reachable from itself"
* Trees aren't a recursive data structure



![](https://miro.medium.com/max/2262/1*-yHATwTlY2hwceJ93-D-cw.jpeg)


**Source:** _stackoverflow.com_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
#### Q29: Under what circumstances are Linked Lists useful? ⭐⭐
##### Answer:
Linked lists are very useful when you need :
* to do a lot of insertions and removals, but not too much searching, on a list of arbitrary (unknown at compile\-time) length.
* splitting and joining (bidirectionally\-linked) lists is very efficient.
* You can also combine linked lists \- e.g. tree structures can be implemented as "vertical" linked lists (parent/child relationships) connecting together horizontal linked lists (siblings).

Using an array based list for these purposes has severe limitations:

*   Adding a new item means the array must be reallocated (or you must allocate more space than you need to allow for future growth and reduce the number of reallocations)
*   Removing items leaves wasted space or requires a reallocation
*   inserting items anywhere except the end involves (possibly reallocating and) copying lots of the data up one position

**Source:** _stackoverflow.com_

#### Q30: Implement _Pre-order Traversal_ of _Binary Tree_ using _Recursion_ ⭐⭐
##### Answer:
For traversing a (non-empty) binary tree in pre-order fashion, we must do these three things for every node `N` starting from root node of the tree:

* (N) Process `N` itself.
* (L) Recursively traverse its _left_ subtree. When this step is finished we are back at N again.
* (R) Recursively traverse its _right_ subtree. When this step is finished we are back at N again.

![](https://www.techiedelight.com/wp-content/uploads/Preorder-Traversal.png)

**Source:** _github.com_

##### Complexity Analysis:
**Time Complexity**: O(n)
**Space Complexity**: O(n)
##### Implementation:
##### _Java_

```java
// Recursive function to perform pre-order traversal of the tree
public static void preorder(TreeNode root)
{
    // return if the current node is empty
    if (root == null) {
        return;
    }
 
    // Display the data part of the root (or current node)
    System.out.print(root.data + " ");
 
    // Traverse the left subtree
    preorder(root.left);
 
    // Traverse the right subtree
    preorder(root.right);
}
```


##### _PY_

```py
# Recursive function to perform pre-order traversal of the tree
def preorder(root):
 
    # return if the current node is empty
    if root is None:
        return
 
    # Display the data part of the root (or current node)
    print(root.data, end=' ')
 
    # Traverse the left subtree
    preorder(root.left)
 
    # Traverse the right subtree
    preorder(root.right)
```


#### Q31: What is an Associative Array? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q32: What does Sparse Array mean? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q33: How to merge two sorted _Arrays_ into a _Sorted Array_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q34: Explain how _Heap Sort_ works ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q35: What is complexity of Hash Table? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q36: LIS: Find length of the _longest increasing subsequence (LIS)_ in the array. Solve using DP. ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q37: Compare Heaps vs Arrays to implement Priority Queue ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q38: How to check if two Strings (words) are _Anagrams_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q39: Name some application of Trie data structure ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q40: Find all the _Permutations_ of a String ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q41: What is AVL Tree? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q42: What is Balanced Tree and why is that important? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q43: Name some common types and categories of Graphs ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q44: Convert a Binary Tree to a Doubly Linked List ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q45: Can you do _Iterative Pre-order Traversal_ of a _Binary Tree_ without _Recursion_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q46: Explain how _QuickSort_ works ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q47: Binet's formula: How to calculate Fibonacci numbers without Recursion or Iteration?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q48: What are some main advantages of Tries over Hash Tables ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q49: How would you traverse a Linked List in <i><code>O(n<sup>1/2</sup>)</code></i>? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q50: Explain what is _Fibonacci Search_ technique? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q51: What are Pascal Strings? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q52: When is doubly linked list more efficient than singly linked list? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q53: What is Red-Black tree? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q54: How To Choose Between a Hash Table and a Trie (Prefix Tree)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q55: How to implement 3 _Stacks_ with one _Array_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q56: Find the _length_ of a Linked List which contains _Cycle (Loop)_ ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q57: What is Rope Data Structure is used for? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q58: Explain what is B-Tree? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q59: What is Bipartite Graph? How to detect one? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q60: Compare lookup operation in Trie vs Hash Table ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q61: How are B-Trees used in practice? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=Databases>Databases</a> Interview Questions
#### Q1: What is _Normalisation_? ⭐⭐
##### Answer:
**Normalization** is basically to design a database schema such that **duplicate and redundant data is avoided**. If the same information is repeated in multiple places in the database, there is the risk that it is updated in one place but not the other, leading to data corruption.

There is a number of normalization levels from 1. normal form through 5. normal form. Each normal form describes how to get rid of some specific problem.

By having a database with normalization errors, you open the risk of getting invalid or corrupt data into the database. Since data "lives forever" it is very hard to get rid of corrupt data when first it has entered the database.

**Source:** _stackoverflow.com_

#### Q2: What is the difference between _Data Definition Language (DDL)_ and _Data Manipulation Language (DML)_? ⭐⭐
##### Answer:
* **Data definition language (DDL)** commands are the commands which are used to define the database. **CREATE**, **ALTER**, **DROP** and **TRUNCATE** are some common DDL commands.

* **Data manipulation language (DML)** commands are commands which are used for manipulation or modification of data. **INSERT**, **UPDATE** and **DELETE** are some common DML commands.

**Source:** _en.wikibooks.org_

#### Q3: What are the advantages of NoSQL over traditional RDBMS? ⭐⭐
##### Answer:
**NoSQL is better** than RDBMS because of the following reasons/properities of NoSQL:

* It supports semi-structured data and volatile data
* It does not have schema
* Read/Write throughput is very high
* Horizontal **scalability** can be achieved easily
* Will support Bigdata in volumes of Terra Bytes & Peta Bytes
* Provides good support for Analytic tools on top of Bigdata
* Can be hosted in cheaper hardware machines
* In-memory caching option is available to increase the performance of queries
* Faster development life cycles for developers

Still, **RDBMS is better** than NoSQL for the following reasons/properties of RDBMS:
* Transactions with **ACID** properties - Atomicity, Consistency, Isolation & Durability
* Adherence to **Strong Schema** of data being written/read
* Real time query management ( in case of data size < 10 Tera bytes )
* Execution of complex queries involving **join** & **group by** clauses

**Source:** _stackoverflow.com_

#### Q4: Define ACID Properties ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q5: How a database index can help performance? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q6: What is Denormalization? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q7: What are the difference between _Clustered_ and a _Non-clustered_ index? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q8: What's the difference between a _Primary Key_ and a _Unique Key_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: When would you use NoSQL? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: When should I use a NoSQL database instead of a relational database? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: What is Optimistic locking? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: What Is ACID Property Of A System? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: What is the _cost_ of having a database _index_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: Explain the difference between _Exclusive Lock_ and _Update Lock_ ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: How does _B-trees Index_ work? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: Explain eventual consistency in context of NoSQL ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: How do you track record relations in NoSQL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: What Is Sharding? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: What Is BASE Property Of A System? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: How do you off load work from the Database? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: What are some _other_ types of Indexes (vs B-Trees)? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: Name some disadvantages of a _Hash index_ ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: What is _Optimistic Locking_ and _Pessimistic Locking_? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: How does database _Indexing_ work? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: What is the difference between _B-Tree_, _R-Tree_ and _Hash_ indexing? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q26: Explain the differences in conceptual data design with NoSQL databases? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q27: What Does Eventually Consistent Mean? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q28: Is the C in ACID is not the C in CAP? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q29: How do you make schema changes to a live database without downtime? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q30: Why you should never use GUIDs as part of clustered index? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=Datasets>Datasets</a> Interview Questions
#### Q1: What's the difference between _Covariance_ and _Correlation_? ⭐⭐
##### Answer:
- **Covariance** measures whether a **variation** in one _variable_ results in a variation in _another variable_, and deals with the linear relationship of only `2` variables in the dataset. Its value can take range from  `-∞` to `+∞`. Simply speaking **Covariance** indicates the direction of the linear relationship between variables. 

![](https://www.simplilearn.com/ice9/free_resources_article_thumb/covx-y.jpg)

- **Correlation** measures how strongly two or more variables are **related** to each other. Its values are between `-1` to `1`. **Correlation** measures both the strength and direction of the linear relationship between two variables. Correlation is a function of the covariance.


**Source:** _careerfoundry.com_

#### Q2: Would you use _K-NN_ for large datasets? ⭐⭐
##### Answer:
It's not recommended to perform **K-NN** on large datasets, given that the computational and memory cost can increase. To understand the reason why we should remember how the **K-NN** algorithm works:

1. Starts by calculating the distances to all vectors in a training set and store them.
2. Then, it sorts the calculated distances.
3. Then, we store the K nearest vectors.
4. And finally, calculate the most frequent class displayed by K nearest vectors.

So implement **K-NN** on a large dataset it is not only a bad decision to store a large amount of data but it is also computationally costly to keep calculating and sorting all the values. For that reason, **K-NN** is not recommended and another classification algorithm like _**Naive Bayes**_ or _**SVM**_ is preferred in such cases.


**Source:** _towardsdatascience.com_

#### Q3: What is *Cross-Validation* and why is it important in supervised learning? ⭐⭐
##### Answer:
* ***Cross-validation*** is a method of assessing _how the results of a statistical analysis will generalize on an independent dataset_,
* It can be used in machine learning tasks to _evaluate the predictive capability of the model_,
*   It also helps us to _avoid overfitting and underfitting_,
* A common way to cross-validate is to divide the dataset into *training*, *validation*, and *testing* where:

  * **Training dataset** is a dataset of known data on which the training is run.
  * **Validation dataset** is the dataset that is *unknown* against which the model is tested. The validation dataset is used after each epoch of learning to gauge the improvement of the model.
  * **Testing dataset** is also an unknown dataset that is used to test the model. The testing dataset is used to measure the performance of the model after it has finished learning.

![cross_validation](https://s3.ap-south-1.amazonaws.com/myinterviewtrainer-domestic/public_assets/assets/000/000/094/original/Cross-Validation.png?1614946006)

**Source:** _en.wikipedia.org_

#### Q4: How does _K-fold Cross Validation_ work? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q5: What is the difference between _Test Set_ and _Validation Set_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q6: What are the assumptions before applying the _OLS estimator_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q7: What are the difference between _Type I_ and _Type II_ errors? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q8: What's the difference between _Bagging_ and _Boosting_ algorithms? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: What's the difference between _One-vs-Rest_ and _One-vs-One_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: What are some _disadvantages_ of using Decision Trees and how would you solve them? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: Name some best practices for working with Datasets ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: When you sample, what potential _Sampling Biases_ could you be inflicting? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: How would you determine the needed _Sample Size_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: What are some variations of _Cross-Validation_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: Explain what is an _Unrepresentative Dataset_ and how would you diagnose it? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: How would you detect _Heteroskedasticity_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: How would you address the problem of _Heteroskedasticity_ caused for a _Measurement error_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: How would you deal with _Outliers_ in your dataset? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: How would you deal with an _Imbalanced Dataset_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: What's the difference between _Random Oversampling_ and _Random Undersampling_ and when they can be used? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: How would you use a _Confusion Matrix_ for determining a model performance? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: What is *Multidimensional Scaling*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: Is _mean imputation_ of missing data acceptable practice? Why or why not? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: When would you use *_chi-Square_* or an *_ANOVA_* test? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: How would you handle _Missing Data_ and perform _Data Imputation_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q26: Compare _ Causation_ vs _Correlation_ ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q27: Which measures of _Variability_ would you use on your data? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q28: How does an ANOVA test work? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=DecisionTrees>Decision Trees</a> Interview Questions
#### Q1: What are *Decision Trees*? ⭐
##### Answer:
* ***Decision trees*** is a tool that uses a *tree-like model* of decisions and their possible consequences. If an algorithm only contains *conditional control statements*, decision trees can model that algorithm really well.
* *Decision trees* are a *non-parametric*, _supervised_ learning method.
* *Decision trees* are used for *classification* and *regression* tasks.
* The diagram below shows an example of a decision tree (the dataset used is the Titanic dataset to predict whether a passenger survived or not):

![decision](https://miro.medium.com/max/540/1*XMId5sJqPtm8-RIwVVz2tg.png)

**Source:** _towardsdatascience.com_

#### Q2: Explain the _structure_ of a Decision Tree ⭐⭐
##### Answer:
A ***decision tree*** is a ***flowchart-like*** structure in which:
* Each *internal node* represents the ***test*** on an attribute (e.g. outcome of a coin flip).
* Each *branch* represents the **_outcome_** of the test.
* Each *leaf node* represents a ***class label***.
* The _paths_ from the root to leaf represent the ***classification rules***.

![https://aiaspirant.com/wp-content/uploads/2020/02/dt_struct.png](https://aiaspirant.com/wp-content/uploads/2020/02/dt_struct.png)

**Source:** _en.wikipedia.org_

#### Q3: How are the different nodes of decision trees _represented_? ⭐⭐
##### Answer:
A **decision tree** consists of three **types** of nodes:
* **Decision nodes:** Represented by **squares.** It is a node where a flow branches into several optional branches.
* **Chance nodes:** Represented by **circles.** It represents the probability of certain results.
* **End nodes:** Represented by **triangles.** It shows the final outcome of the decision path.

![decision_nodes](https://upload.wikimedia.org/wikipedia/commons/a/ad/Decision-Tree-Elements.png)

**Source:** _en.wikipedia.org_

#### Q4: What are some _advantages_ of using Decision Trees? ⭐⭐
##### Answer:
* It is **simple to understand** and interpret. It can be **visualized** easily.
* It **does not require as much data preprocessing** as other methods.
* It can handle both **numerical** and **categorical** data.
* It can handle **multiple output** problems.

**Source:** _scikit-learn.org_

#### Q5: What type of node is considered *Pure*? ⭐⭐
##### Answer:
* If the *Gini Index* of the data is `0` then it means that all the elements **belong to a specific class**. When this happens it is said to be *pure*.
* When all of the data belongs to a single class (*pure*) then the *leaf node* is reached in the tree.
* The leaf node represents the *class label* in the tree (which means that it gives the final output).

![pure_node](https://miro.medium.com/max/2000/1*k4qcPhr04dHjciI5nFdQrw.png)

**Source:** _medium.com_

#### Q6: How is a _Random Forest_ related to _Decision Trees_? ⭐⭐
##### Answer:
* ***Random forest*** is an ***ensemble learning*** method that works by constructing a multitude of ***decision trees***. A random forest can be constructed for both classification and regression tasks.
* Random forest **outperforms** decision trees, and it also does not have the habit of *overfitting* the data as decision trees do.
* A decision tree trained on a specific dataset will become very deep and cause overfitting. To create a random forest, decision trees can be trained on different subsets of the training dataset, and then the different decision trees can be averaged with the goal of _decreasing the variance_.

**Source:** _en.wikipedia.org_

#### Q7: What is the difference between *OOB* score and *validation* score? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q8: How would you deal with an _Overfitted Decision Tree_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: What are some _disadvantages_ of using Decision Trees and how would you solve them? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: What is *Greedy Splitting*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: What type of *Cost Functions* do *Greedy Splitting* use? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: How would you define the *Stopping Criteria* for decision trees? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: Why do you need to *Prune* the decision tree? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: What is *Entropy*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: How do we _measure_ the Information? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: What is *Gini Index* and how is it used in Decision Trees? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: What is the *Chi-squared test*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: How does the *CART* algorithm produce *Classification Trees*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: How does the *CART* algorithm produce *Regression Trees*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: What is the difference between *Post-pruning* and *Pre-pruning*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: Compare *Linear Regression* and *Decision Trees* ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: What is _Tree Bagging_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: What is _Tree Boosting_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: How to use _Isolation Forest_ for Anomalies detection? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: Imagine that you know there are _outliers_ in your data, would you use _Logistic Regression_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q26: What is the use of *Entropy* pertaining to Decision Trees? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q27: While building Decision Tree how do you choose which attribute to _split_ at each node? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q28: What is difference between _Gini Impurity_ and _Entropy_ in Decision Tree? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q29: When should I use _Gini Impurity_ as opposed to _Information Gain (Entropy)_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q30: Explain the *CHAID* algorithm ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q31: What are some disadvantages of the *CHAID* algorithm? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q32: Explain how can *CART* algorithm performs _Pruning_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q33: Explain how *ID3* produces *classification trees*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q34: How would you compare different _Algorithms_ to build _Decision Trees_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q35: Compare *ID3* and *C4.5* algorithms ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q36: Compare *C4.5* and *C5.0* algorithms ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q37: What is the relationship between *Information Gain* and *Information Gain Ratio*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q38: How do you _Gradient Boost_ decision trees? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q39: Compare *Decision Trees* and *Logistic Regression* ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q40: What are the differences between *Decision Trees* and *Neural Networks*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q41: Compare *Decision Trees* and *k-Nearest Neighbors* ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q42: What is the *Variance Reduction* metric in _Decision Trees_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q43: What is the difference between *Gradient Boosting* and *Adaptive Boosting*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q44: Explain the measure of _goodness"_ used by CART ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=DeepLearning>Deep Learning</a> Interview Questions
#### Q1: What is the difference between *Machine Learning* and *Deep Learning*? ⭐⭐
##### Answer:
* ***Machine Learning*** depends on humans to learn. Humans determine the hierarchy of *features* to determine the difference between the data input. It usually requires more structured data to learn.
* ***Deep Learning*** automates much of the _feature extraction_ piece of the process. It eliminates the manual human intervention required.
* ***Machine Learning*** is less dependent on the amount of data as compared to deep learning.
* ***Deep Learning*** requires a lot of data to give high accuracy. It would take thousands or millions of data points which are trained for days or weeks to give an acceptable accurate model.


**Source:** _ibm.com_

#### Q2: What advantages does *Deep Learning* have over *Machine Learning*? ⭐⭐
##### Answer:
* ***Deep Learning*** gives a _better performance_ compared to machine learning if the dataset is large enough.
* ***Deep Learning*** does not need the person designing the model to have a lot of *domain understanding for feature introspection*. Deep learning outshines other methods if there is _no feature engineering done_.
* ***Deep Learning*** really shines when it comes to _complex problems_ such as *image classification*, *natural language processing*, and *speech recognition*.

**Source:** _towardsdatascience.com_

#### Q3: Why does the performance of *Deep Learning* improve as more data is fed to it? ⭐⭐
##### Answer:
* One of the best benefits of **Deep Learning** is its ability to perform ***automatic feature extraction*** from raw data.
* When the number of data fed into the learning algorithm increases, there will be more *edge cases* taken into consideration and hence the algorithm will learn to make the right decisions in those edge cases.

**Source:** _machinelearningmastery.com_

#### Q4: What is the difference between *Deep Learning* and *Artificial Neural Networks*? ⭐⭐
##### Answer:
* When researchers started to create ***large*** artificial neural networks, they started to use the word **deep** to refer to them.
* As the term *deep learning* started to be used, it is generally understood that it stands for artificial neural networks which are **deep** as opposed to **shallow** artificial neural networks.
* ***Deep Artificial Neural Networks*** and ***Deep Learning*** are generally the _same thing_ and mostly used interchangeably.

**Source:** _machinelearningmastery.com_

#### Q5: What is *Early Stopping* in Deep Learning? ⭐⭐
##### Answer:
* ***Early stopping*** in deep learning is a type of regularization where the training is **stopped** after a few iterations.
* When training a large network, there will be a point during training when the _model will stop generalizing_ and start learning the statistical noise in the training dataset. This makes the networks unable to predict new data.
* Defining *early stopping* in a neural network will prevent the network from **overfitting**.
* One way of defining early stopping is to start training the model and if the performance of the model starts to _degrade_, then stopping the training process.

![https://miro.medium.com/max/567/1*2BvEinjHM4SXt2ge0MOi4w.png](https://miro.medium.com/max/567/1*2BvEinjHM4SXt2ge0MOi4w.png)



**Source:** _Neural Networks and Deep Learning: A Textbook by Charu C. Aggarwal_

#### Q6: What are *Ensemble* methods and how are they useful in Deep Learning? ⭐⭐
##### Answer:
* ***Ensemble*** methods are used to increase the *generalization* power of a model. These methods are applicable to both deep learning as well as machine learning algorithms.
* Some ensemble methods introduced in neural networks are ***Dropout*** and ***Dropconnect***. The improvement in the model depends on the type of data and the nature of neural architecture.

**Source:** _Neural Networks and Deep Learning: A Textbook by Charu C. Aggarwal_

#### Q7: Explain the working of a *Perceptron* ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q8: How would you choose the *Loss Function* for a Deep Learning model? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: What are *Computation Graphs*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: What happens when you trade the *Breadth* of a neural network for the *Depth*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: What does the hidden layer in a Neural Network compute? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: What does _1x1 convolution_ mean in a Neural Network? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: What is the difference between *Linear Activation Function* and *Non-linear Activation Function*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: What is the importance of using _Non-linear Activation_ function? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: What is the difference between _Deep Learning_ and _SVM_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: What are the advantages of _ReLU_ over _Sigmoid function_ in Deep Neural networks? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: How is *Fourier Transform* used to the benefit of Deep Learning? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: How can you optimise the architecture of a *Deep Learning* classifier using _Genetic Algorithms_? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: How would you choose the *Activation Function* for a deep learning model? 
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=DimensionalityReduction>Dimensionality Reduction</a> Interview Questions
#### Q1: What is the *Curse of Dimensionality* and how can Unsupervised Learning help with it? ⭐⭐
##### Answer:
* As the amount of data required to train a model increases, it becomes harder and harder for machine learning algorithms to handle. **As more features are added to the machine learning process, the more difficult the training becomes.**
* In very *high-dimensional* space, supervised algorithms learn to separate points and build function approximations to make good predictions. 

> When the number of *features* increases, this **search becomes expensive**, both from a time and compute perspective. It might become impossible to find a good solution fast enough. This is the *curse of dimensionality*.

* Using ***dimensionality reduction*** of unsupervised learning, the most _salient_ features can be discovered in the original feature set. Then the dimension of this feature set can be reduced to a more manageable number while losing very little information in the process. This will help supervised learning find the optimum function to approximate the dataset.

**Source:** _www.amazon.com_

#### Q2: What is *Principal Component Analysis (PCA)*? ⭐⭐
##### Answer:
* The ***Principal Component Analysis* (PCA)** is the process of computing principal components and using them to perform a change of basis on the data.
* The **Principal Component** of a collection of points in a *real coordinate space* are a sequence of `p` unit vectors, where the `i`-th vector is the direction of a line that best fits the data while being *orthogonal* to the `i - 1` vectors. The best-fitting line is defined as the line that minimizes the average squared distance from the points to the line.
* ***PCA*** is commonly used in _dimensionality reduction_ by projecting each data point onto only the first few principal components to obtain lower-dimensional data while preserving as much of the data's variation as possible.

![https://wiki.math.uwaterloo.ca/statwiki/images/4/4f/PCA_in_Neuroscience.png](https://wiki.math.uwaterloo.ca/statwiki/images/4/4f/PCA_in_Neuroscience.png)

**Source:** _en.wikipedia.org_

#### Q3: What are some advantages of using *LLE* over *PCA*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q4: How does an *Isomap* perform *Dimensionality Reduction*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q5: What are the two branches of *Dimensionality Reduction*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q6: Why is _Centering_ and _Scaling_ the data important before performing *PCA*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q7: What is *Singular Value Decomposition*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q8: How does *Random Projection* reduce the dimensionality of a set of points? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: What is the difference between _PCA_ and _Random Projection_ approaches? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: Explain the *Sparse Random Projection* ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: Explain the *Locally Linear Embedding* algorithm for _Dimensionality Reduction_ ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: What is *Multidimensional Scaling*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: When would you use *Manifold Learning* techniques over *PCA*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: What is *Sparse PCA*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: What is *Kernel Principal Component Analysis*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: What are the rules for generating a random matrix when *Gaussian Random Projection* is used? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: What is *t-Distributed Stochastic Neighbour Embedding*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=EnsembleLearning>Ensemble Learning</a> Interview Questions
#### Q1: What is _Ensemble Learning_? ⭐
##### Answer:
**Ensemble learning** is a machine learning paradigm where multiple models (often called “weak learners”) are trained to solve the same problem and combined to get better results. The main hypothesis is that when weak models are correctly combined we can obtain more accurate and/or robust models.

**Source:** _towardsdatascience.com_

#### Q2: How would you define *Random Forest*? ⭐
##### Answer:
* **Random Forests** is a type of *ensemble* learning method for *classification*, *regression*, and other tasks.
* **Random Forests** works by constructing many **decision trees** at a training time. The way that this works is by averaging several decision trees at *different parts* of the same training set.

**Source:** _en.wikipedia.org_

#### Q3: What are _Weak Learners_? ⭐⭐
##### Answer:
In ensemble learning theory, we call **weak learners** (or **base models**) models that can be used as building blocks for designing more complex models by combining several of them. Most of the time, these basics models perform not so well by themselves either because they have a high bias (low degree of freedom models, for example) or because they have too much variance to be robust (high degree of freedom models, for example).

**Source:** _towardsdatascience.com_

#### Q4: What are *Ensemble Methods*? ⭐⭐
##### Answer:
* **Ensemble methods** is a machine learning technique that combines several base models in order to produce one optimal predictive model.
* **Random Forest** is a type of ensemble method.
* The number of component classifier in an ensemble has a great impact on the accuracy of the prediction, although there is a law of diminishing results in ensemble construction.

**Source:** _towardsdatascience.com_

#### Q5: How is a _Random Forest_ related to _Decision Trees_? ⭐⭐
##### Answer:
* ***Random forest*** is an ***ensemble learning*** method that works by constructing a multitude of ***decision trees***. A random forest can be constructed for both classification and regression tasks.
* Random forest **outperforms** decision trees, and it also does not have the habit of *overfitting* the data as decision trees do.
* A decision tree trained on a specific dataset will become very deep and cause overfitting. To create a random forest, decision trees can be trained on different subsets of the training dataset, and then the different decision trees can be averaged with the goal of _decreasing the variance_.

**Source:** _en.wikipedia.org_

#### Q6: What's the similarities and differences between _Bagging_, _Boosting_, _Stacking_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q7: Explain the concept behind *BAGGing* ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q8: What is the difference between *OOB* score and *validation* score? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: What is the difference between a _Weak Learner_ vs a _Strong Learner_ and why they could be usefu? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: What's the difference between _Bagging_ and _Boosting_ algorithms? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: How does the _AdaBoost_ algorithm work? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: What are some _disadvantages_ of using Decision Trees and how would you solve them? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: What is _Tree Bagging_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: What is _Tree Boosting_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: How is *Gradient Boosting* used to improve supervised learning? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: Give some reasons to choose *Random Forests* over *Neural Networks* ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: What are the trade-offs between the different types of _Classification Algorithms_? How would do you choose the best one? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: How do you _Gradient Boost_ decision trees? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: How would you find the optimal *number of random features* to consider at each split? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=GeneticAlgorithms>Genetic Algorithms</a> Interview Questions
#### Q1: How are *Genetics* represented in the Genetic Algorithm? ⭐⭐
##### Answer:
* Each individual is represented by a ***chromosome*** represented by a collection of genes.
* A ***chromosome*** is represented by a string of bits, where each ***bit*** represents a single ***gene***.
* A ***population*** is shown as a group of binary strings where each string represents an individual.

![gene](https://miro.medium.com/max/1112/1*vIrsxg12DSltpdWoO561yA.png)

#### Q2: How would you describe what _Genetic Algorithms_ are? ⭐⭐
##### Answer:
A **Genetic Algorithm (GA)** is a heuristic _search algorithm_ used to **solve search and optimization problems**. This algorithm is a subset of [evolutionary algorithms](https://en.wikipedia.org/wiki/Evolutionary_algorithm), which are used in the computation. Genetic algorithms employ the concept of genetics and natural selection to provide solutions to problems.

These algorithms have better intelligence than **random search algorithms** because they use historical data to take the search to the best performing region within the solution space.

GAs are also based on the behavior of chromosomes and their genetic structure. Every chromosome plays the role of providing a possible solution. The fitness function helps in providing the characteristics of all individuals within the population. The greater the function, the better the solution.

**Source:** _www.section.io_

#### Q3: Explain some basic concepts and terms related to _Genetic Algorithm_ ⭐⭐
##### Answer:
There are some of the basic terminologies related to genetic algorithms:

- **Population:** This is a subset of all the _probable_ solutions that can solve the given problem.
- **Chromosomes:** A chromosome is one of the solutions in the population.
- **Gene:** This is an element in a chromosome.
- **Allele:** This is the value given to a gene in a specific chromosome.
- **Fitness function:** This is a function that uses a specific _input_ to produce an improved _output_. The solution is used as the input while the output is in the form of solution suitability.
- **Genetic operators:** In genetic algorithms, the best individuals mate to reproduce an offspring that is better than the parents. Genetic operators are used for _changing the genetic composition_ of this next generation.

![https://miro.medium.com/max/1112/1*vIrsxg12DSltpdWoO561yA.png](https://miro.medium.com/max/1112/1*vIrsxg12DSltpdWoO561yA.png)

**Source:** _www.section.io_

#### Q4: What is a *Fitness Function*? ⭐⭐
##### Answer:
* A ***fitness function*** is a function that maps the ***chromosome*** representation into a scalar value.
* At each iteration of the algorithm, each individual is evaluated using a ***fitness function***.
* The individuals with a better ***fitness score*** are more likely to be chosen for _reproduction_ and be represented in the next generation.
* The ***fitness function*** seeks to optimize the problem that is being solved.



**Source:** _ai.stackexchange.com_

#### Q5: What is a *Mutation* and why is it programmed into the algorithm? ⭐⭐
##### Answer:
* ***Mutation*** introduces new patterns in the chromosomes, and it helps to find solutions in uncharted areas.
* ***Mutations*** are implemented as _random_ changes in the chromosomes. It may be programmed, for example, as a *bit flip* where a single bit of the chromosome changes.
* The purpose of *mutation* is to periodically _refresh_ the population.

![https://www.researchgate.net/profile/Chun-Liu-8/publication/272093243/figure/fig8/AS:329956690284546@1455679213204/Mutation-operators-applied-to-chromosomes-in-the-proposed-genetic-algorithm.png](https://www.researchgate.net/profile/Chun-Liu-8/publication/272093243/figure/fig8/AS:329956690284546@1455679213204/Mutation-operators-applied-to-chromosomes-in-the-proposed-genetic-algorithm.png)

**Source:** _www.amazon.com_

#### Q6: What are some _advantages_ of *Genetic Algorithms*? ⭐⭐
##### Answer:
* It has the capability to **globally optimize the problem** instead of just finding the local minima or maxima.
* It can _handle_ problems with _complex mathematical representation_.
* It can _handle_ problems that _lack mathematical representation_.
* It is **resilient to noise**.
* It can support **parallel** and **distributed processing**.
* It is suitable for **continuous learning**.
* It provides answers that improve over time.
* A genetic algorithm does not need _derivative_ information.

**Source:** _www.amazon.com_

#### Q7: Explain the concept of *Elitism* in _Genetic Algorithms_ ⭐⭐
##### Answer:
* While the *average fitness* of the genetic algorithm increases as the generations go by, the best individuals from the current generations will be lost due to *selection*, *crossover*, and *mutation* operators. This problem is solved by the process known as **Elitism**.
* **Elitism** **guarantees** that the best individuals always make it to the next generation.
* `n` predefined number of individuals are _duplicated_ into the next generation. These individuals selected for duplication are also eligible to be parents of the new individuals.

**Source:** _en.wikipedia.org_

#### Q8: How are *Crossover* and *Mutation* methods performed for *Real-Coded Chromosomes*? ⭐⭐
##### Answer:
The **crossover** and **mutation** operations are applied separately for each *dimension* of the array that forms the real-coded chromosome.

For example, if `[1.23, 9.81, 6.34]` and `[-30.23, 12.67, -42.69]` are selected for the crossover operation, the crossover will be done for between; `1.23` and `-30.23` (first dimension), `9.81` and `12.67` (second dimension), and `6.34` and `-42.69` (third dimension).

**Source:** _www.amazon.com_

#### Q9: Explain the *Schema Theorem* ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: What are the differences between *Genetic Algorithms* and *Traditional Search and Optimization Algorithms*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: When are Genetic Algorithms _useful_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: What are some disadvantages of *Genetic Algorithms*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: What are some *Stopping Conditions* that a genetic algorithm may implement? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: What is *Roulette Wheel Selection*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: What is the difference between *Stochastic Universal Sampling* and *Roulette Wheel Selection*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: How to perform _Rank Based Selection_ in a Genetic Algorithm? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: How do you perform the *Tournament Selection*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: What is the difference between _Mutation_ and _Crossover_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: What are *Evolution Strategies*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: What are _Variation Operators_ in _Genetic Algorithms _? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: How can *Genetic Algorithms* be used to improve the _accuracy_ of other ML algorithms? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: What is the *Vehicle Routing Problem* in the context of *Search Algorithms*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: What is the *Travelling Salesman Problem* in the context of *Search Algorithms*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: Can you explain _Elitism_ in a context of _Genetic Algorithms_ and it's impact on GA performance? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: What is the difference between _Tournament Selection_ and _Elitism_ in _Genetic Algorithm_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q26: What are the advantages of using *Floating-Point* number to represent chromosomes instead of *Binary* numbers? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q27: Name some _types_ of _Mutation_ in GA ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q28: What is a *Uniform Crossover*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q29: Compare the *Single-Point* and *Two-Point* crossover ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q30: How can *Evolutionary Algorithms* be used for *Clustering*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q31: Compare *Roulette Wheel Selection* and *Rank-Based Selection* ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q32: Why is _Cross-over_ a part of Genetic Algorithms? Wouldn't _Mutation_ be enough? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q33: How do _Mutation_ and _Crossover_ work with _real-valued_ chromosomes? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q34: How is *Differential Evolution* different from *Genetic Algorithms*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q35: What are the distinctions between _Genetic Algorithms_ and _Evolution Strategies_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q36: What is *Genetic Programming*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q37: Can you explain how _Genetic Algorithms_ related to _Darwinian Natural Selection_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q38: What are *Constraint Satisfaction Problems* and why is Genetic Algorithms suited to solve them? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q39: What is _Time Complexity_ of a basic _Genetic Algorithm_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q40: What is *Niching* in a _Genetic Algorithm_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q41: Explain _BLX-α algorithm_ for _Crossover_ implementation ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q42: How can you optimise the architecture of a *Deep Learning* classifier using _Genetic Algorithms_? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q43: How would you encode the structure of a _Neural Network_ into a _genome_? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q44: What is _NEAT (Neuroevolution of Augmenting Topologies)_ algorithm? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q45: What is the difference between _Memetic Algorithms_ and _Genetic Algorithms_? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=GradientDescent>Gradient Descent</a> Interview Questions
#### Q1: What is the idea behind the *Gradient Descent*? ⭐⭐
##### Answer:
* A **Gradient Descent** is a type of optimization algorithm used to find the *local minimum* of a differentiable function.
* The main idea behind the gradient descent is to take steps in the *negative* direction of the gradient. This will lead to the steepest descent and eventually it will lead to the minimum point.
* It is shown as an equation by:

$$a_{n+1} = a_n - \gamma \nabla F(a_n)$$

Where:
- **a** is the point.
- $$\gamma$$ is the **step size**.
- **F(x)** is the multi-variable function.

![](http://rasbt.github.io/mlxtend/user_guide/general_concepts/gradient-optimization_files/ball.png)

**Source:** _en.wikipedia.org_

#### Q2: What is the difference between _Cost Function_ vs _Gradient Descent_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q3: What are some _types_ of _Gradient Descent_ do you know? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q4: Compare the *Mini-batch Gradient Descent*, *Stochastic Gradient Descent*, and *Batch Gradient Descent* ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q5: Explain how does the _Gradient descent_ work in _Linear Regression_ ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q6: Name some _Evaluation Metrics_ for Regression Model and when you would use one? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q7: In which case you would use  _Gradient Descent method_ or _Ordinary Least Squares_ and why? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q8: Explain the intuition behind Gradient Descent algorithm ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: How is *Gradient Boosting* used to improve supervised learning? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: What is the difference between _Gradient Descent_ and _Stochastic Gradient Descent_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: Does gradient descent always converge to an _optimum_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: How is the *Adam Optimization Algorithm* different when compared to *Stochastic Gradient Descent*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: Name some advantages of using _Gradient descent_ vs _Ordinary Least Squares_ for Linear Regression ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=K-MeansClustering>K-Means Clustering</a> Interview Questions
#### Q1: What is the difference between _KNN_ and _K-means Clustering_? ⭐⭐
##### Answer:
- **_K-nearest neighbors_** or _KNN_ is a _supervised classification algorithm_. This means that we need labeled data to classify an unlabeled data point. It attempts to classify a data point based on its proximity to other `K`-data points in the feature space.

- **_K-means Clustering_** is an _unsupervised classification algorithm_. It requires only a set of unlabeled points and a threshold `K`, so it gathers and groups data into `K` number of clusters.

**Source:** _www.quora.com_

#### Q2: What is *Similarity-based Clustering*? ⭐⭐
##### Answer:
* Clustering, when the data are similar pairs of points is called **similarity-based clustering**.
* A typical example of similarity-based clustering is community detection in social networks, where the observations are individual links between people, which may be due to friendship, shared interests, and work relationships. The *strength* of a link can be the frequency of interactions, for example, communications by e-mail, phone, or other social media, co-authorships, or citations.
* In this clustering paradigm, the points to be clustered are not assumed to be part of a vector space. Their attributes (or features) are incorporated into a single dimension, the *link strength*, or *similarity*, which takes a numerical value $$S_{ij}$$ for each pair of points `i`, `j`. Hence, the natural representation for this problem is by means of the similarity matrix given below:
$$
S=[S_{ij}]_{i,j=1}^n
$$
The similarities are symmetric $$S_{ij} = S_{ji}$$ and nonnegative $$S_{ij} \geq 0$$.

**Source:** _Handbook of Cluster Analysis from Chapman and Hall/CRC_

#### Q3: How does *K-Means* perform Clustering? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q4: While performing *K-Means* Clustering, how do you determine the value of *K*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q5: Compare *Hierarchical Clustering* and *k-Means Clustering* ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q6: What is a *Mixture Model*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q7: What makes the distance measurement of *k-Medoids* better than *k-Means*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q8: When would you use *Hierarchical Clustering* over *k-Means Clustering*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: How to tell if data is _clustered_ enough for clustering algorithms to produce meaningful results? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: Explain the different frameworks used for *k-Means Clustering* ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: What is the relationship between *k-Means Clustering* and *PCA*? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=K-NearestNeighbors>K-Nearest Neighbors</a> Interview Questions
#### Q1: How do you choose the optimal _k_ in _k-NN_? ⭐⭐
##### Answer:
There is not a rule of thumb to choose a standard optimal **_k_**. This value depends and varies from dataset to dataset, but as a general rule, the main goal is to keep it:
- small enough to exclude the samples of the other classes but 
- large enough to minimize any noise in the data.

A way to looking for this optimal parameter, commonly called the _Elbow method_, consist in creating a _for loop_ that trains various **_KNN_** models with different **_k values_**, keeping track of the error for each of these models, and use the model with the **_k value_** that achieves the best accuracy.

![https://i.stack.imgur.com/ct2ie.jpg](https://i.stack.imgur.com/ct2ie.jpg)

**Source:** _medium.com_

#### Q2: What's the difference between _k-Nearest Neighbors_ and _Radius Nearest Neighbors_? ⭐⭐
##### Answer:
- **KNN**: 
  - The _k-neighbors classification_ is a very commonly used technique and is _widely applied_ in various scenarios. 
  - _KNN_ implements learning based on the `k` nearest neighbors of each _query point_, where `k` is a hyperparameter of an _integer value_.
  - The optimal choice of the value `k` is highly data-dependent: in general, a larger `k` suppresses the effects of _noise_ but makes the classification boundaries _less distinct_.


- **RNN**:
  - The _r-neighbors classification_ is used in cases where the data is not _uniformly sampled_ or is _sparse_.
  - _RNN_ implements learning based on the number of neighbors within a _fixed radius_ `r` of each training point, where `r` is a hyperparameter of the type _float_. 
  - The optimal fixed radius `r` is chosen such that points in _sparser neighborhoods_ use _fewer nearest neighbors_ for the classification.


**Source:** _scikit-learn.org_

#### Q3: Would you use _K-NN_ for large datasets? ⭐⭐
##### Answer:
It's not recommended to perform **K-NN** on large datasets, given that the computational and memory cost can increase. To understand the reason why we should remember how the **K-NN** algorithm works:

1. Starts by calculating the distances to all vectors in a training set and store them.
2. Then, it sorts the calculated distances.
3. Then, we store the K nearest vectors.
4. And finally, calculate the most frequent class displayed by K nearest vectors.

So implement **K-NN** on a large dataset it is not only a bad decision to store a large amount of data but it is also computationally costly to keep calculating and sorting all the values. For that reason, **K-NN** is not recommended and another classification algorithm like _**Naive Bayes**_ or _**SVM**_ is preferred in such cases.


**Source:** _towardsdatascience.com_

#### Q4: What is *k-Nearest Neighbors* algorithm? ⭐⭐
##### Answer:
* ***k-Nearest Neighbors*** is a supervised machine learning algorithm that can be used to solve both *classification* and *regression* problems.
* It assumes that _similar things are closer to each other_ in certain feature spaces, in other words, similar things are in close proximity.

![knn](https://miro.medium.com/max/917/1*wW8O-0xVQUFhBGexx2B6hg.png)

* The image above shows how similar points are closer to each other. KNN hinges on this assumption being true enough for the algorithm to be useful.
* There are many different ways of calculating the distance between the points, however, the straight line distance (Euclidean distance) is a popular and familiar choice.

**Source:** _towardsdatascience.com_

#### Q5: Compare *K-Nearest Neighbors (KNN)* and *SVM* ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q6: How can you relate the _KNN Algorithm_ to the _Bias-Variance tradeoff_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q7: How do you select the value of *K* for *k-Nearest Neighbors*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q8: What are some _advantages_ and _disadvantages_ of *k-Nearest Neighbors*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: Compare *Decision Trees* and *k-Nearest Neighbors* ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=LinearAlgebra>Linear Algebra</a> Interview Questions
#### Q1: Why is _Centering_ and _Scaling_ the data important before performing *PCA*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=LinearRegression>Linear Regression</a> Interview Questions
#### Q1: What is _Linear Regression_? ⭐
##### Answer:
**Linear Regression** is a supervised machine learning algorithm where the predicted output is continuous and has a constant slope. It’s used to predict values within a _continuous range_, (e.g. sales, price) rather than trying to classify them into categories (e.g. cat, dog). 

**Source:** _ml-cheatsheet.readthedocs.io_

#### Q2: What are _types_ of Linear Regression? ⭐⭐
##### Answer:
* Simple **linear** regression uses traditional slope-intercept form. 𝑥 represents our input data and 𝑦 represents our prediction.

 > 𝑦 = 𝑚𝑥+𝑏

* A more complex, **multi-variable** linear equation might look like this, where 𝑤 represents the coefficients, or weights, our model will try to learn.

 > 𝑓(𝑥,𝑦,𝑧) = 𝑤1𝑥+𝑤2𝑦+𝑤3𝑧

 The variables 𝑥, 𝑦, 𝑧 represent the attributes, or distinct pieces of information, we have about each observation. For sales predictions, these attributes might include a company’s advertising spend on radio, TV, and newspapers.

 > 𝑆𝑎𝑙𝑒𝑠 = 𝑤1*𝑅𝑎𝑑𝑖𝑜+𝑤2*𝑇𝑉+𝑤3*𝑁𝑒𝑤𝑠

**Source:** _ml-cheatsheet.readthedocs.io_

#### Q3: How can you check if the Regression model fits the data well?  ⭐⭐
##### Answer:
We can use the following statistics to test the model’s fitness:

1. **R-squared**: It is a statistical measure of how close the data points are to the fitted regression line. Its value is always between `0` and `1`. The closer to `1`, the better the regression model fits the observations.


2. **F-test**: It evaluates the null hypothesis that the data is described by an intercept-only model, which is a regression with all the coefficients equal to zero versus the alternative hypothesis that at least one is not. If the **P-value** for the _F-test_ is less than the significance level, we can reject the null hypothesis and conclude that the model provides a better fit than the intercept-only model.


3. **Root Mean Square Error (RMSE)**: It measures the average deviation of the estimates from the observed value. How _good_ this value is must be assessed for each project and context. For example, an _RMSE_ of `1,000` for a house price prediction is probably good as houses tend to have prices over `$100,000`, but an _RMSE_ of `1,000` for a life expectancy prediction is probably terrible as the average life expectancy is around `78`.

**Source:** _en.wikipedia.org_

#### Q4: What is the difference between _Mean Absolute Error (MAE)_ vs _Mean Squared Error (MSE)_? ⭐⭐
##### Answer:
- The **Mean Squared Error** measures the variance of the residuals and is used when we want to punish the outliers in the dataset. It's defined as:

 $$MSE = \frac{1}{N} \sum_{i=1}^N(y_i - \hat{y})^2$$

- The **Mean Absolute Error** measures the average of the residuals in the dataset. Is used when we don’t want outliers to play a big role. It can also be useful if we know that our distribution is multimodal, and it’s desirable to have predictions at one of the modes, rather than at the mean of them. It's defined as:

 $$MAE = \frac{1}{N} \sum_{i=1}^n |y_i -\hat{y}|$$


**Source:** _medium.com_

#### Q5: How would you detect _Overfitting_ in Linear Models? ⭐⭐
##### Answer:
The common pattern for **overfitting** can be seen on **learning curve** plots, where model performance on the training dataset continues to improve (e.g. loss or error continues to fall) and performance on the test or validation set improves to a point and then begins to get worse. 

![](https://miro.medium.com/max/1140/1*72c0UVyvEbxLNB1J43id5Q.png)

So an overfit model will have **extremely low training error but a high testing error**.

**Source:** _towardsdatascience.com_

#### Q6: What's the difference between _Covariance_ and _Correlation_? ⭐⭐
##### Answer:
- **Covariance** measures whether a **variation** in one _variable_ results in a variation in _another variable_, and deals with the linear relationship of only `2` variables in the dataset. Its value can take range from  `-∞` to `+∞`. Simply speaking **Covariance** indicates the direction of the linear relationship between variables. 

![](https://www.simplilearn.com/ice9/free_resources_article_thumb/covx-y.jpg)

- **Correlation** measures how strongly two or more variables are **related** to each other. Its values are between `-1` to `1`. **Correlation** measures both the strength and direction of the linear relationship between two variables. Correlation is a function of the covariance.


**Source:** _careerfoundry.com_

#### Q7: Provide an intuitive explanation of the _Learning Rate_? ⭐⭐
##### Answer:
The **Learning Rate** is a **hyper-parameter** that can determine the _speed_ or step size at each _iteration_ while moving towards a minimal point in **Gradient Descent**. This value should not be too _small_ or _too high_ because if it's too small then it takes too much time to _converge_ and if it's too large then the step size will increase and it moves quickly and never reach a _global minima point_ even after repeated iterations.

![](https://miro.medium.com/max/1200/1*Q-2Wh0Xcy6fsGkbPFJvMhQ.gif)

**Source:** _priyaroychowdhury.medium.com_

#### Q8: How is the _Error_ calculated in a Linear Regression model? ⭐⭐
##### Answer:
1. Measuring the distance of the observed _y-values_ from the predicted _y-values_ at each value of _x_.
2. Squaring each of these distances.
3. Calculating the _mean_ of each of the squared distances.

MSE = (1/n) * Σ(actual – forecast)2

4. The smaller the **Mean Squared Error**, the closer you are to finding the _line of best fit_
5. How _bad_ or _good_ is this final value always depends on the context of the problem, but the main goal is that its value is so minimal as possible. 

![](https://www.jmp.com/en_ch/statistics-knowledge-portal/what-is-multiple-regression/fitting-multiple-regression-model/_jcr_content/par/styledcontainer_2069/par/lightbox_4130/lightboxImage.img.png/1548703926664.png)

**Source:** _www.scribbr.com_

#### Q9: What is *Linear Regression*? ⭐⭐
##### Answer:
* ***Linear regression*** is a linear approach for modeling the relationship between a *scalar* response and one or more *explanatory variables*.
* In a *supervised linear regression*, the model tries to find a linear relationship between the input and output data points. This linear relationship is a *straight line* if graphed.
* If there is only one *explanatory* variable it is called *simple linear regression*, and if there are more than one *explanatory* variable it is called *multiple linear regression*.
* A linear function is given by the following equation:
$$
y = X\beta + \epsilon
$$
where all the variables are matrices containing data points.

![linear_regression](https://miro.medium.com/max/1400/1*I-MxKoiWxJXLfExpvbT1eQ.png)

**Source:** _en.wikipedia.org_

#### Q10: How does a *Non-Linear* regression analysis differ from *Linear* regression analysis? ⭐⭐
##### Answer:
* ***Non-linear*** functions have variables with powers greater than `1`. Like $$x^2$$. If these non-linear functions are graphed, they do not produce a straight line (their direction changes constantly).
* ***Linear*** functions have variables with only powers of `1`. They form a straight line if it is graphed.
###

* ***Non-linear*** regression analysis tries to model a non-linear relationship between the independent and dependent variables.
* A simple non-linear relationship is shown below:

![non_linear_function](https://machinelearningmastery.com/wp-content/uploads/2020/10/Plot-of-Fifth-Degree-Polynomial-Fit-to-Economic-Dataset.png)

* ***Linear*** regression analysis tries to model a linear relationship between the independent and dependent variables.
* A simple linear relationship is shown below:

![linear_function](https://chartio.com/assets/4d44f9/tutorials/charts/scatter-plots/1642e681117c0b68d135cf4eca136846ced8b859b46b1055e4158281942d76b8/scatter-plot-options-1.png)

**Source:** _www.columbia.edu_

#### Q11: Explain what the _Intercept Term_ means ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: Name a disadvantage of _R-squared_ and explain how would you address it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: What is the difference between _Ordinary Least Squares_ and _Ridge Regression?_ ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: What is the difference between _Ordinary Least Squares_ and _Lasso regression?_ ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: Why use _Root Mean Squared Error (RMSE)_ instead of _Mean Absolute Error (MAE)_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: How would you decide on the _importance_ of variables for the _Multivariate Regression_ model?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: What are the assumptions before applying the _OLS estimator_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: Explain how does the _Gradient descent_ work in _Linear Regression_ ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: Name some _Evaluation Metrics_ for Regression Model and when you would use one? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: What is the difference between a _Regression Model_ and an _ANOVA Model_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: How does it work the _Backward Selection Technique_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: What are the _Assumptions of Linear Regression_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: In which case you would use  _Gradient Descent method_ or _Ordinary Least Squares_ and why? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: How is _Hypothesis Testing_ using in _Linear Regression_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: What is the difference between _Linear Regression_ and _Logistic Regression_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q26: Why would you use _Normalisation_ vs _Standardisation_ for Linear Regression? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q27: Why can't a _Linear Regression_ be used instead of _Logistic Regression_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q28: Explain the intuition behind Gradient Descent algorithm ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q29: How would you fix Logistic Regression _Overfitting_ problem? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q30: Compare *Linear Regression* and *Decision Trees* ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q31: What are some challenges faced when using a *Supervised Regression Model*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q32: What's the difference between *Homoskedasticity* and *Heteroskedasticity*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q33: How would you detect _Collinearity_ and what is _ Multicollinearity_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q34: Explain the _Stepwise Regression_ technique ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q35: How would you deal with _Overfitting_ in Linear Regression models? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q36: Explain what is an _Unrepresentative Dataset_ and how would you diagnose it? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q37: How would you detect _Heteroskedasticity_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q38: How would you address the problem of _Heteroskedasticity_ caused for a _Measurement error_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q39: How would you compare models using the _Akaike Information Criterion_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q40: Name some advantages of using _Gradient descent_ vs _Ordinary Least Squares_ for Linear Regression ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q41: How would you deal with _Outliers_ in your dataset? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q42: How would you check if a Linear Model follows all Regression assumptions? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q43: How would you implement Linear Regression Function in SQL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q44: Provide an intuitive explanation of _RANSAC Regression_ algorithm ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q45: What types of _Robust Regression Algorithms_ do you know? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=LogisticRegression>Logistic Regression</a> Interview Questions
#### Q1: When _Logistic Regression_ can be used? ⭐⭐
##### Answer:
**Logistic regression** can be used in _classification_ problems where the output or dependent variable is _categorical_ or _binary_. However, in order to implement logistic regression correctly, the dataset must also satisfy the following properties: 

1. There should not be a high correlation between the independent variables. In other words, the predictor variables should be independent of each other. 
2. There should be a linear relationship between the `logit` of the outcome and each predictor variable. The `logit` function is given as `logit(p) = log(p/(1-p))`, where `p` is the probability of the outcome.
3. The sample size must be large. How large depends on the number of independent variables of the model. 


When all the requirements above are satisfied, logistic regression can be used. 

**Source:** _careerfoundry.com_

#### Q2: Why is Logistic Regression called _Regression_ and not _Classification_? ⭐⭐
##### Answer:
Although the task we are targeting in logistic regression is a classification, _logistic regression does not actually individually classify things for you_: it just gives you probabilities (or log odds ratios in the logit form). 

The only way logistic regression can actually classify stuff is if you apply a rule to the probability output. For example, you may round probabilities greater than or equal to `50%` to `1`, and probabilities less than `50%` to `0`, and that’s your classification.

**Source:** _ryxcommar.com_

#### Q3: What is a _Decision Boundary_? ⭐⭐
##### Answer:
A **decision boundary** is a line or a hyperplane that separates the classes. This is what we expect to obtain from _logistic regression_, as with any other classifier. With this, we can figure out some way to split the data to allow for an accurate prediction of a given observation’s class using the available information.

In the case of a generic two-dimensional example, the split might look something like this: 

![](https://miro.medium.com/max/340/0*hyR0M6QP5OvedMkd.png)

**Source:** _medium.com_

#### Q4: How would you make a prediction using a _Logistic Regression_ model? ⭐⭐
##### Answer:
In **Logistic regression** models, we are modeling the _probability_ that an input `(X)` belongs to the default class `(Y=1)`, that is to say:

$$
P(X) = P(Y=1|X)
$$

where the `P(X)` values are given by the **_logistic function_**,

$$
P(X) = \frac{e^{\beta_0 + \beta_1X}}{1 + e^{\beta_0 + \beta_1X}}
$$

The `β0` and `β1` values are estimated during the training stage using _maximum-likelihood_ estimation or _gradient descent_. Once we have it, we can make predictions by simply putting numbers into the _logistic regression equation_ and calculating a result.

For example, let's consider that we have a model that can predict whether a person is male or female based on their height, such as if `P(X) ≥ 0.5` the person is male, and if `P(X) < 0.5` then is female.  

During the training stage we obtain `β0 = -100` and `β1 = 0.6`, and we want to evaluate what's the probability that a person with a height of `150cm` is male, so with that intention we compute: 

$$
y = \frac{e^{-100 + 0.6\cdot 150}}{1 + e^{-100 + 0.6\cdot 150}} = 0.00004539 \cdots
$$

Given that logistic regression solves a _classification_ task, we can use directly this value to predict that the person is a female. 

**Source:** _machinelearningmastery.com_

#### Q5: What is the difference between _Linear Regression_ and _Logistic Regression_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q6: Provide a mathematical intuition for Logistic Regression? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q7: Why is _Logistic Regression_ considered a _Linear Model_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q8: Why can't a _Linear Regression_ be used instead of _Logistic Regression_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: Compare *SVM* and *Logistic Regression* in handling outliers ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: What can you infer from each of the hand drawn decision boundary of _Logistic Regression_ below? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: Why don’t we use _Mean Squared Error_ as a cost function in Logistic Regression? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: How a _Logistic Regression_ model is trained? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: What's the difference between _Softmax_ and _Sigmoid_ functions? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: How do you use a supervised *Logistic Regression* for Classification? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: Explain the _Vectorized Implementation_ of _Logistic Regression_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: Explain the _Space Complexity Analysis_ of _Logistic Regression_  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: How can we avoid _Over-fitting_ in _Logistic Regression_ models? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: Imagine that you know there are _outliers_ in your data, would you use _Logistic Regression_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: Name some advantages of using _Support Vector Machines_ vs _Logistic Regression_ for classification ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: When would you use _SVM_ vs _Logistic regression_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: Compare _Naive Bayes_ vs with _Logistic Regression_ to solve classification problems ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: Compare *Decision Trees* and *Logistic Regression* ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: Can _Logistic Regression_ be used for an _Imbalanced Classification_ problem? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=MachineLearning>Machine Learning</a> Interview Questions
#### Q1: What is a _Machine Learning_? ⭐
##### Answer:
Essentially, Machine Learning is a method of teaching computers to make and improve predictions or behaviors based on some _data_. Machine Learning introduces a class of algorithms which is data-driven, i.e. unlike "normal" algorithms it is the data that "tells" what the "good answer" is. Machine learning creates a model based on sample data and use the model to make some prediction. 

More rigid explanation: Machine Learning is a field of computer science, probability theory, and optimization theory which allows complex tasks to be solved for which a logical/procedural approach would not be possible or feasible.

**Source:** _stackoverflow.com_

#### Q2: When we say that the machine learns, does it modify the code of itself? ⭐⭐
##### Answer:
- Machine learning **code** records "facts" or approximations in some sort of storage, and with the algorithms calculates different probabilities.
   
- The code **itself** (usually) will not be modified when a machine learns, only the database of what "it knows".
- One example of code actually being modified is **Genetic Programming**, where you essentially evolve a program to complete a task (of course, the program doesn't modify itself - but it does modify another computer program).

**Source:** _stackoverflow.com_

#### Q3: What is _Overfitting_ in Machine Learning? ⭐⭐
##### Answer:
* **Overfitting** refers to a model that models the training data too well.
* **Overfitting** happens when a model learns the detail and noise in the training data to the extent that it negatively impacts the performance of the model on new data. This means that the noise or random fluctuations in the training data is picked up and learned as concepts by the model. The problem is that these concepts do not apply to new data and negatively impact the model's ability to generalize.

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT0H97op-3IJaeTHm_p28tYVtXfl8iouB0ltrGv5Z6YIiii7s-5L0GCUj2eXcOXJISV_g&usqp=CAU)



**Source:** _machinelearningmastery.com_

#### Q4: What is _Underfitting_ in Machine Learning? ⭐⭐
##### Answer:
* **Underfitting** refers to a model that can neither model the training data nor generalizes to new data.
* An underfit machine learning model is not a suitable model and will be obvious as it will have poor performance on the training data.
* **Underfitting** is often not discussed as it is easy to detect given a good performance metric. The remedy is to move on and try alternate machine learning algorithms. 

**Source:** _machinelearningmastery.com_

#### Q5: What is _Hyper-Parameters_ in ML Model? ⭐⭐
##### Answer:
Every machine learning model has parameters and _can_ additionally have hyper\-parameters. **Hyper\-parameters** are those parameters that cannot be directly learned from the regular training process. These parameters express **higher\-level** properties of the model such as its _complexity_ or _how fast it should learn_.

If machine learning model was an AM radio, the knobs for tuning the station would be its parameters but things like angle of antenna, height of antenna, volume knob would be hyperparameters.

**Source:** _medium.com_

#### Q6: What are _Weak Learners_? ⭐⭐
##### Answer:
In ensemble learning theory, we call **weak learners** (or **base models**) models that can be used as building blocks for designing more complex models by combining several of them. Most of the time, these basics models perform not so well by themselves either because they have a high bias (low degree of freedom models, for example) or because they have too much variance to be robust (high degree of freedom models, for example).

**Source:** _towardsdatascience.com_

#### Q7: What is the difference between data mining, statistics, machine learning and AI? ⭐⭐
##### Details:
What exactly do they have in common and where do they differ? If there is some kind of hierarchy between them, what would it be?

##### Answer:
In short

*   **Statistics** *studies* probability
*   **Data Mining** *explains* patterns
*   **Machine Learning** *predicts* with models
*   **Artificial Intelligence** *behaves* and *reasons*

More detailed:

* **Statistics** is concerned with probabilistic models, specifically inference on these models using data.

* **Data Mining** is about using **Statistics** as well as other programming methods to find patterns hidden in the data so that you can *explain* some phenomenon. Data Mining builds intuition about what is really happening in some data and is still little more towards math than programming, but uses both.

* **Machine Learning** uses **Data Mining** techniques and other learning algorithms to build models of what is happening behind some data so that it can *predict* future outcomes. Math is the basis for many of the algorithms, but this is more towards programming.

* **Artificial Intelligence** uses models built by **Machine Learning** and other ways to *reason* about the world and give rise to intelligent *behavior* whether this is playing a game or driving a robot/car. Artificial Intelligence has some goal to achieve by predicting how actions will affect the model of the world and chooses the actions that will best achieve that goal. Very programming based.

**Source:** _stats.stackexchange.com_

#### Q8: How do you understand the saying that _Machine Learns_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: What is the difference between _Test Set_ and _Validation Set_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: What's the similarities and differences between _Bagging_, _Boosting_, _Stacking_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: What are the difference between _Type I_ and _Type II_ errors? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: What is *Entropy*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: How do we _measure_ the Information? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: When to stop? How to know that your Machine Learning problem is hopeless? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: Can you explain _PAC_ learning theory _intuitively_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: What is the use of *Entropy* pertaining to Decision Trees? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: What is the *Probably Approximately Correct* learning? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=ModelEvaluation>Model Evaluation</a> Interview Questions
#### Q1: What is _Overfitting_ in Machine Learning? ⭐⭐
##### Answer:
* **Overfitting** refers to a model that models the training data too well.
* **Overfitting** happens when a model learns the detail and noise in the training data to the extent that it negatively impacts the performance of the model on new data. This means that the noise or random fluctuations in the training data is picked up and learned as concepts by the model. The problem is that these concepts do not apply to new data and negatively impact the model's ability to generalize.

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT0H97op-3IJaeTHm_p28tYVtXfl8iouB0ltrGv5Z6YIiii7s-5L0GCUj2eXcOXJISV_g&usqp=CAU)



**Source:** _machinelearningmastery.com_

#### Q2: What is _Underfitting_ in Machine Learning? ⭐⭐
##### Answer:
* **Underfitting** refers to a model that can neither model the training data nor generalizes to new data.
* An underfit machine learning model is not a suitable model and will be obvious as it will have poor performance on the training data.
* **Underfitting** is often not discussed as it is easy to detect given a good performance metric. The remedy is to move on and try alternate machine learning algorithms. 

**Source:** _machinelearningmastery.com_

#### Q3: What is _Hyper-Parameters_ in ML Model? ⭐⭐
##### Answer:
Every machine learning model has parameters and _can_ additionally have hyper\-parameters. **Hyper\-parameters** are those parameters that cannot be directly learned from the regular training process. These parameters express **higher\-level** properties of the model such as its _complexity_ or _how fast it should learn_.

If machine learning model was an AM radio, the knobs for tuning the station would be its parameters but things like angle of antenna, height of antenna, volume knob would be hyperparameters.

**Source:** _medium.com_

#### Q4: What are the difference between _Type I_ and _Type II_ errors? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q5: What is a *Confusion Matrix*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q6: What _performance parameters_ can be calculated using Confusion Matrix? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q7: How does *ROC* curve and *AUC* value help measure how good a model is? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q8: What are some advantages and disadvantages of using *AUC* to measure the _performance_ of the model? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: What is the *F-Score*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: How do you reduce the risk of making a _Type I_ and _Type II_ error? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: How is _AUC - ROC_ curve used in classification problems?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: How would you use a _Confusion Matrix_ for determining a model performance? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: How would you choose an evaluation metric for an _Imbalanced classification_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: If one algorithm has _Higher Precision_ but _Lower Recall_ than other, how can you tell which algorithm is better? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: What is *AIC*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: What is *BIC*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: Compare *AIC* and *BIC* methods for model selection  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: What is *MDL*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: What are *Concordance* and *Discordance*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: What's the difference between _ROC_ and _Precision-Recall_ Curves? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: How to interpret _F-measure_ values? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=NaturalLanguageProcessing>Natural Language Processing</a> Interview Questions
#### Q1: Why is text preprocessing done in NLP? ⭐
##### Answer:
* **Text preprocessing** is done to transform a text into a more *digestible form* so that the machine learning algorithms can perform better. It is found that in tasks such as *sentiment analysis*, performing some preprocessing such as *removing stop-words* helps improve the *accuracy* of the machine learning model.
* Some common text preprocessing done are: 
  - removing HTML tags, 
  - removing stop-words, 
  - removing numbers, 
  - lower casing all letters, 
  - Lemmatization.

**Source:** _towardsdatascience.com_

#### Q2: What is the difference between _Lemmatisation_ and _Stemming_? ⭐⭐
##### Answer:
* **Stemming** just removes the *last few characters of a word*, often leading to incorrect meanings and spellings.

 Consider: 
 ```
eating -> eat, Caring -> Car.
 ```
* **Lemmatization** considers the *context* and converts the word to its meaningful base form, which is called *Lemma*.

 Consider: 

 ```
Stripes -> Strip (verb) -or- Stripe (noun), better -> good
 ```

**Source:** _stackoverflow.com_

#### Q3: When would you use _Stemming_ over _Lemmatisation_, and vice-versa? ⭐⭐
##### Answer:
* **Stemming** is not *computationally expensive*, so it should be used where the dataset is large and performance is an issue.
* **Lemmatization** is *computationally expensive* because it involves dictionary look-up or a rule-based system. It is recommended for smaller datasets where accuracy is more important.

**Source:** _stackoverflow.com_

#### Q4: What is the use of _PoS (Part of Speech)_ tagging? ⭐⭐
##### Answer:
* **PoS tagging** is used to classify each word into its part of speech.
* Parts of speech can be used to find *grammatical, or lexical patterns without specifying the word used*.
* In English especially, the *same word* can be *different parts of speech*, so hence, PoS tagging can be helpful to differentiate between them.

**Source:** _www.sketchengine.eu_

#### Q5: What are some of the advantages of using the _Bag-of-Words_ to extract features? ⭐⭐
##### Answer:
* It identifies the *occurrence of words* in a document. It identifies the *vocabulary* and the *presence* of *known* words. Hence, it is very simple and flexible.
* It is intuitive that documents consisting of *similar content will be similar in other ways such as meaning* too. So, the BoW process will create a simple and quick group of features that can be used.
* The BoW model can be made as simple, and as complicated as possible. The main difference is how the *vocabulary of words is maintained*, and how the *different words are scored*.

**Source:** _machinelearningmastery.com_

#### Q6: What are some of the advantages of using the _Bag-of-Words_ to extract features? ⭐⭐
##### Answer:
* It identifies the *occurrence of words* in a document. It identifies the *vocabulary* and the *presence* of *known* words. Hence, it is very simple and flexible.
* It is intuitive that documents consisting of *similar content will be similar in other ways such as meaning* too. So, the BoW process will create a simple and quick group of features which can be used.
* The BoW model can be made as simple, and as complicated as possible. The main difference is how the *vocabulary of words is maintained*, and how the *different words are scored*.

![](https://miro.medium.com/max/554/0*B9GC_f3BMtjGMdQ-.png)

**Source:** _machinelearningmastery.com_

#### Q7: What are the differences between _TF-IDF_ and _TF_? ⭐⭐
##### Answer:
Definition:
* **TF-IDF**: Term Frequency-Inverse Document Frequency
* **TF**: Term Frequency

Difference: 
* **TF-IDF** is a *numerical statistic* that is intended to reflect how *important* a word is to the document in a collection of the corpus.
* **TF** is a *count* of the number of times a word occurs in a document.
* **TF-IDF** is given by: 

$$
tfidf(t,d) = tf(t,d)*log(\frac{N}{(df+1)})
$$
* **TF** is given by the count of a word in the document by the number of words in d: 
$$
tf(t,d) = \frac{f_{t,d}}{\sum_{t'\in d} f_{t',d}}
$$

**Source:** _towardsdatascience.com_

#### Q8: What is a _One-Hot Vector_? How can they be used in Natural Language Processing? ⭐⭐
##### Answer:
* A **one-hot **is a group of *bits* which only has *one high `1` bit* and all *other bits are low `0`*.
* In **Natural Language Processing**, the one-hot vector can be used to represent a sentence in the form of a *matrix* of `1 x N` size where `N` is the number of *individual* words in the corpus.
* For example, the sentence "Peter picked a piece of pickled pepper" can be transformed into a matrix of `1 x 7` where each word is represented by the 7 columns. Hence the output of the sentence is: `[0000001, 0000010, 0000100, 0001000, 0010000, 0100000, 1000000]`
* An understandable representation of a one-hot vector is shown by the diagram below:

![one_hot](https://miro.medium.com/max/1225/0*QMGjp-fPYpPaE3eK)

**Source:** _en.wikipedia.org_

#### Q9: What are the different types of text _Preprocessing_? ⭐⭐
##### Answer:
Steps of **text preprocessing** can be divided into `3` major types:
* **Tokenization:** It is a process where a group of texts are divided into smaller pieces, or *tokens*. *Paragraphs* are tokenized into *sentences*, and *sentences* are tokenized into *words*.
* **Normalization:** Database normalization is where the structure of the database is converted to a series of *normal forms*. What it achieves is the organization of the data to appear similar across all records and fields. Similarly, in the field of *NLP*, normalization can be the process of converting all the words to its lowercase. This makes all the sentences and tokens appear the same and does not complicate the machine learning algorithm.
* **Noise Removal:** It is a process of *cleaning up the text*. Doing things such as *removing* characters which are not required, such as white spaces, numbers, special characters, etc.

![](https://raw.githubusercontent.com/satishgunjal/images/master/NLP_Text_Preprocessing.png)

**Source:** _towardsdatascience.com_

#### Q10: What is _Named Entity Recognition (NER)_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: What are some advantages of using _TF-IDF_ over _TF_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: What are some disadvantages of using a _One-Hot Vector_ for Natural Language Processing? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: What loss function would you use for *Sentiment Analysis*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: Name some types of *Text Summarisation* ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: How has *Translation* of words improved from the _Traditional methods_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: What are the uses of using *RNN* in NLP? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: What are the uses of *LSTM* in NLP? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: How is *Convolutional Neural Networks (CNN)* used in NLP? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: What is *Syntactic Analysis*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: What are some _ambiguities_ faced in NLP? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: What is _Latent Semantic Analysis_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: Explain what is _ROUGE_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: What is intuition behind using *CNN* for NLP? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: How would you create a *Neural Captioning Model*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: Explain the concept behind the *Neural Machine Translator* ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q26: What is an _Embedding_ in NLP? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q27: What is *Semantic Analysis*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q28: What are some of the differences between NLP and CUI (Conversational User Interface)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q29: What causes the accuracy of Sentiment Analysis to be low? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q30: What is _BLEU_? 
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=NaïveBayes>Naïve Bayes</a> Interview Questions
#### Q1: What is a *Naïve Bayes Classifier*? ⭐
##### Answer:
* ***Naive Bayes Classifiers*** are a family of simple *probabilistic classifiers* based on applying *Bayes' theorem* with strong independence assumptions between the features.
* *Bayes' theorem* is given by the following equation:
$$
P(A|B)=\frac{P(B|A)P(A)}{P(B)}
$$
* Using Bayes' theorem, the probability of `A` happening given that `B` has occurred can be found.
* An example of the way a Naive Bayes Classifier can be used is, given that it has rained, the probability of temperature being low is `P(Temperature|Rain)`.

![](https://cdn-images-1.medium.com/max/600/1*aFhOj7TdBIZir4keHMgHOw.png)

**Source:** _towardsdatascience.com_

#### Q2: Why Naive Bayes is called _Naive_? ⭐⭐
##### Answer:
We call it **naive** because its assumptions (it assumes that all of the features in the dataset are equally important and independent) are really optimistic and rarely true in most real-world applications:
- we consider that these _predictors_ are _independent_
- we consider that all the predictors have an _equal effect_ on the outcome (like the day being windy does not have more importance in deciding to play golf or not)

**Source:** _towardsdatascience.com_

#### Q3: What _Bayes' Theorem (Bayes Rule)_ is all about? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q4: Find a probability of dangerous Fire when there is Smoke ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q5: Can you choose a _classifier_ based on the _size of the training set_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q6: How would you use _Naive Bayes_ classifier for categorical features? What if some features are numerical? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q7: What's the difference between _Generative Classifiers_ and _Discriminative Classifiers_? Name some examples of each one ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q8: How does the _Naive Bayes_ classifier work? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: What are some advantages of using *Naive Bayes Algorithm*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: What are some _disadvantages_ of using *Naive Bayes Algorithm*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: What is Bayesian Network? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: Are there any problems using _Naive Bayes_ for Classification? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: What are the trade-offs between the different types of _Classification Algorithms_? How would do you choose the best one? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: Compare _Naive Bayes_ vs with _Logistic Regression_ to solve classification problems ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=NeuralNetworks>Neural Networks</a> Interview Questions
#### Q1: What are *Neural Networks*? ⭐
##### Answer:
* A **neural network** is a network or circuit of neurons composed of *artificial neurons* or *nodes*.
* A *neural network* can both be *biological neural networks* or *artificial neural networks*. Artificial neural networks are the ones used to solve *AI* problems.
* The artificial networks may be used for *predictive modeling*, *adaptive control* and applications where they can be trained via a dataset. Self-learning resulting from experience can occur within networks, which can derive conclusions from a complex and seemingly unrelated set of information.

A simple *feed-forward* neural network is shown below:

![ff_nn](https://upload.wikimedia.org/wikipedia/commons/9/99/Neural_network_example.svg)

**Source:** _en.wikipedia.org_

#### Q2: How are *Neural Networks* modelled? ⭐⭐
##### Answer:
* ***Artificial neural networks*** are modelled from biological neurons.
* The connections of the biological neuron are modeled as *weights*. 
  * A positive weight reflects an _excitatory_ connection, while negative values mean _inhibitory_ connections. 
  * All inputs are modified by a weight and summed. This activity is referred to as a _linear combination_. 
* Finally, an activation function controls the amplitude of the output. For example, an acceptable range of output is usually between 0 and 1, or it could be −1 and 1.

![](https://miro.medium.com/max/1400/1*upfpVueoUuKPkyX3PR3KBg.png)

**Source:** _en.wikipedia.org_

#### Q3: How do neural networks get the optimal *weights* and *bias* values? ⭐⭐
##### Answer:
* The neural networks get the optimal *weights* and *bias* values through an **Error Gradient**.
* To decide whether to *increase* or *decrease* the current weights and bias, it needs to be compared to the *optimal* value. This is found by the *gradients of error* with respect to weights and bias:

$$\frac{\partial E}{\partial W}, \frac{\partial E}{\partial b}$$


* The gradient value is calculated from a selected algorithm called **backpropagation**.
* An *optimization algorithm* utilizes the gradient to improve the weight values and bias.

![](https://i.stack.imgur.com/7Ui1C.png)

**Source:** _towardsdatascience.com_

#### Q4: What is a *Perceptron*? ⭐⭐
##### Answer:
* A **Perceptron** is a fundamental unit of a Neural Network that is also a single-layer Neural Network.
* Perceptron is a linear _classifier_. Since it uses already labeled data points, it is a *supervised learning algorithm*.  
* The _activation function_ applies a step rule (convert the numerical output into +1 or -1) to check if the output of the weighting function is greater than zero or not.

A **Perceptron** is shown in the figure below:

![perception](https://www.programmersought.com/images/258/633dca25508a646a6df343339c3d4eaa.png)


**Source:** _towardsdatascience.com_

#### Q5: What are *Loss Functions* in Neural Networks? ⭐⭐
##### Answer:
* Neural network requires a *loss function* to be chosen when designing and configuring the model.
* While optimizing the model, an **objective function** is  either a loss function or its negative. The objective function is sought to be *maximized* or *minimized* (output which has the highest or lowest score respectively). Typically, in a neural network the error should be minimized.
* The *loss function* should reduce all the aspects of a *complex model* down to a *single* scalar value, which allows the candidate solutions to be *ranked and compared*.
* The loss function chosen by the designer should _capture the properties of the problem_ and be motivated by concerns that are important to the project.

![](https://cdn-images-1.medium.com/max/800/1*N1PyOYeog-vyytRbwEwQCQ.png)

**Source:** _machinelearningmastery.com_

#### Q6: What is an *Activation Function*? ⭐⭐
##### Answer:
* An **activation function** applies a step rule (convert the numerical output into +1 or -1) to check if the output of the weighting function is greater than zero or not.
* An **activation function** of a node defines the output of the node given an input or set of inputs to the node.


* **Activation functions** can be divided into three categories: 
  * **ridge functions** 
  * **radial functions**, and
  * **fold functions**.


* A type of **ridge function** called *Rectified Linear Function (ReLU)* is shown below:

![relu](https://www.researchgate.net/profile/Leo-Pauly/publication/319235847/figure/fig3/AS:537056121634820@1505055565670/ReLU-activation-function.png)

* A type of **radial function** called *Gaussian Function* is shown below:

![gaussian](https://www.researchgate.net/profile/Xiaobing-Nie/publication/327821106/figure/fig1/AS:680202015371268@1539184206884/Graph-of-Gaussian-activation-function.png)

* A **fold function** perform aggregation over the inputs, such as taking the *mean, minimum or maximum*.


**Source:** _en.wikipedia.org_

#### Q7: What are the roles of an *Activation Function*? ⭐⭐
##### Answer:
* **Activation Functions** help in keeping the value of the output from the neuron restricted to a certain limit as per the requirement. If the limit is not set then the output will reach very high magnitudes. Most activation functions convert the output to `-1` to `1` or to `0` to `1`.
* The most *important* role of the activation function is the ability to add **non-linearity** to the neural network. Most of the models in real-life is non-linear so the activation functions help to create a non-linear model.
* The *activation function* is responsible for deciding whether a neuron should be activated or not.

**Source:** _towardsdatascience.com_

#### Q8: What is the difference between *Forward Propagation* and *Backward Propagation*? ⭐⭐
##### Answer:
* **Forward propagation** is the input data that is fed in the forward direction through the network. Each *hidden layer* accepts the input data, processes it as per the activation function, and passes it to the successive layer.
* **Back propagation** is the practice of *fine-tuning* the weights of the neural network based on the error rate obtained from the previous epoch. Proper tuning of the weights ensures low error rates, making the model more reliable. 

![](https://miro.medium.com/max/1170/1*0hf4gLbc-2V5RMXBhluJ_A.gif)



**Source:** _towardsdatascience.com_

#### Q9: Name some applications of Neural Networks? ⭐⭐
##### Answer:
Some applications for ANN include:
* System **identification** and **control**: Vehicle control, trajectory prediction.
* **Medical diagnosis**: Identifying cancer, distinguishing highly invasive cancer cell lines from less invasive lines using only cell shape information.
* **Sequence recognition**: Gesture, speech, handwritten and printed text recognition.
* **Geoscience**: Hydrology, ocean modelling, coastal engineering, geomorphology.
* **Cybersecurity**: Discriminating between legitimate activities and malicious ones.

**Source:** _en.wikipedia.org_

#### Q10: What is the difference between *Deep Learning* and *Artificial Neural Networks*? ⭐⭐
##### Answer:
* When researchers started to create ***large*** artificial neural networks, they started to use the word **deep** to refer to them.
* As the term *deep learning* started to be used, it is generally understood that it stands for artificial neural networks which are **deep** as opposed to **shallow** artificial neural networks.
* ***Deep Artificial Neural Networks*** and ***Deep Learning*** are generally the _same thing_ and mostly used interchangeably.

**Source:** _machinelearningmastery.com_

#### Q11: What is *Early Stopping* in Deep Learning? ⭐⭐
##### Answer:
* ***Early stopping*** in deep learning is a type of regularization where the training is **stopped** after a few iterations.
* When training a large network, there will be a point during training when the _model will stop generalizing_ and start learning the statistical noise in the training dataset. This makes the networks unable to predict new data.
* Defining *early stopping* in a neural network will prevent the network from **overfitting**.
* One way of defining early stopping is to start training the model and if the performance of the model starts to _degrade_, then stopping the training process.

![https://miro.medium.com/max/567/1*2BvEinjHM4SXt2ge0MOi4w.png](https://miro.medium.com/max/567/1*2BvEinjHM4SXt2ge0MOi4w.png)



**Source:** _Neural Networks and Deep Learning: A Textbook by Charu C. Aggarwal_

#### Q12: What are *Self-Organizing Maps*? ⭐⭐
##### Answer:
* **Self-Organizing Maps** (**SOMs**) are a class of *self-organizing* clustering techniques.
* It is an _unsupervised form of artificial neural networks_. A self-organizing map consists of a set of neurons that are arranged in a rectangular or hexagonal grid. Each neuronal unit in the grid is associated with a numerical vector of fixed dimensionality. The learning process of a self-organizing map involves the adjustment of these vectors to provide a suitable representation of the input data.
* Self-organizing maps can be used for clustering numerical data in vector format.

![som](https://www.researchgate.net/profile/Mohamed-Zair/publication/329337931/figure/fig1/AS:915377227849728@1595254346086/Structural-model-of-self-organizing-map-neural-network-Figure-2-Experimental-benchmark.png)

**Source:** _medium.com_

#### Q13: What are some advantages of using *Multilayer Perceptron* over a *Single-layer Perceptron*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: What is the *Vanishing Gradient Problem* in artificial Neural Networks? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: What is the *Exploding Gradient Problem* in artificial Neural Networks? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: Why does an artificial Neural Network use *Backpropagation*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: Why should you *Normalize* the input for Neural Networks? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: How would you tune the *Network Structure (Model Design) Hyperparameters* to get the highest accuracy in an artificial Neural Network? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: How would you tune the *Training Algorithm Hyperparameters* to get the highest accuracy in a Neural Network? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: How would you prevent *Overfitting* when designing an artificial Neural Network? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: What type of Neural Networks do *Deep Reinforcement Learning* use? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: How is *One-Shot Learning* still not attainable for artificial Neural Networks? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: What are some criticisms of Neural Networks? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: How has *Translation* of words improved from the _Traditional methods_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: What are the uses of using *RNN* in NLP? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q26: What are the uses of *LSTM* in NLP? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q27: How is *Convolutional Neural Networks (CNN)* used in NLP? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q28: What is _BLEU_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q29: What is _ROUGE_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q30: What are some similarities between *SVMs* and *Neural Networks*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q31: What are some differences between *SVMs* and *Neural Networks*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q32: How can *Neural Networks* be used to create *Autoencoders*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q33: Explain the working of a *Perceptron* ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q34: What happens when you trade the *Breadth* of a neural network for the *Depth*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q35: What does the hidden layer in a Neural Network compute? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q36: What does _1x1 convolution_ mean in a Neural Network? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q37: Give some reasons to choose *Random Forests* over *Neural Networks* ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q38: What are some advantages of *Neural Network* over *Random Forest*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q39: How would you fix the *Exploding Gradient Problem*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q40: What is the difference between *ReLU*, *Leaky ReLU*, *Exponential Linear Unit (ELU)*, and *Parametric ReLU (PReLU)*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q41: When do you use *ReLU*, *Tanh*, and *Sigmoid* activation functions in Neural Networks? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q42: Why does a *Deep Neural Network* work better than a *Shallow Neural Network*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q43: Compare *Feed-forward* and *Recurrent* Neural Network. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q44: Compare the *Convolutional Neural Network* and *Multi-layer Perceptron*. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q45: What is a *Radial Basis Function Network*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q46: What are some uses of *Echo-State Networks*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q47: What is a *GRU*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q48: How are *Attention Metrics* modeled in Neural Networks? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q49: What is intuition behind using *CNN* for NLP? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q50: How would you create a *Neural Captioning Model*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q51: Explain the concept behind the *Neural Machine Translator* ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q52: What is an _Embedding_ in NLP? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q53: What is *Sequential Minimal Optimization*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q54: What are the differences between *Decision Trees* and *Neural Networks*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q55: How does *LSTM* compare to *RNN*? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q56: Explain how a _Recurrent Architecture_ for leveraging visual attention works ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q57: What is a *Deconvolutional Network*? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q58: How is *Competitive Learning* different from traditional Neural Networks? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q59: How would you encode the structure of a _Neural Network_ into a _genome_? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q60: What is _NEAT (Neuroevolution of Augmenting Topologies)_ algorithm? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q61: Explain why the *Initialization* process of weights and bias is important? 
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q62: Explain the intuition behind *RNN* having a Vanishing Gradient Problem? 
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q63: How can *Neural Networks* be _Unsupervised_? 
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=NumPy>NumPy</a> Interview Questions
## [[⬆]](#toc) <a name=Optimization>Optimization</a> Interview Questions
## [[⬆]](#toc) <a name=Pandas>Pandas</a> Interview Questions
#### Q1: How are `iloc()` and `loc()` different? ⭐⭐
##### Answer:
* `DataFrame.iloc` is a method used to retrieve data from a Data frame, **and it is an integer position-based locator (from 0 to length-1 of the axis)**, but may also be used with a boolean array. It takes input as integer, arrays of integers, a slice object, boolean array and functions.

```py
df.iloc[0]
df.iloc[-5:]
df.iloc[:, 2]    # the : in the first position indicates all rows
df.iloc[:3, :3] # The upper-left 3 X 3 entries (assuming df has 3+ rows and columns)
```
* `DataFrame.loc` **gets rows (and/or columns)** with particular labels. 
It takes input as a single label, list of arrays and slice objects with labels. 

```py
df = pd.DataFrame(index=['a', 'b', 'c'], columns=['time', 'date', 'name'])
df.loc['a']     # equivalent to df.iloc[0]
df.loc['b':, 'date']   # equivalent to df.iloc[1:, 1]
```

**Source:** _stackoverflow.com_

#### Q2: What are the operations that _Pandas Groupby_ method is based on ? ⭐⭐
##### Answer:
* _Splitting_ the data into groups based on some criteria. 
* _Applying a function_ to each group independently. 
* _Combining the results_ into a data structure. 

**Source:** _pandas.pydata.org_

#### Q3: Describe how you will get the _names of columns_ of a _DataFrame in Pandas_ ⭐⭐
##### Answer:
* By _Simply iterating_ over columns, and printing the values. 

```py
for col in data.columns:
    print(col)
```

* _Using `.columns()`_ method with the dataframe object, this returns the column labels of the DataFrame.

```py
list(data.columns)
```

* _Using the `column.values()`_ method to return an array of index.

```py
list(data.columns.values)
```

* _Using `sorted()`_ method, which will return the list of columns sorted in alphabetical order.

```py
sorted(data)
```

**Source:** _www.geeksforgeeks.org_

#### Q4: In Pandas, what do you understand as a _bar plot_ and how can you generate a _bar plot visualization_ ⭐⭐
##### Answer:
* A **Bar Plot** is a plot that presents categorical data with rectangular bars with lengths proportional to the values that they represent. 
* A bar plot shows comparisons among discrete categories. 
* One axis of the plot shows the specific categories being compared, and the other axis represents a measured value.

```py

# Code Sample for how to plot
df.plot.bar(x='x_values’', y='y_values')

```

![](https://pandas.pydata.org/docs/_images/pandas-DataFrame-plot-bar-2.png)

**Source:** _pandas.pydata.org_

#### Q5: How would you iterate over rows in a DataFrame in Pandas? ⭐⭐
##### Answer:
[`DataFrame.iterrows`](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.iterrows.html#pandas-dataframe-iterrows) is a generator which yields both the _index_ and _row_ (as a Series):

```python
import pandas as pd

df = pd.DataFrame({'c1': [10, 11, 12], 'c2': [100, 110, 120]})

for index, row in df.iterrows():
    print(row['c1'], row['c2'])
```

```python
10 100
11 110
12 120
```

**Source:** _stackoverflow.com_

#### Q6: How to check whether a Pandas DataFrame is _empty_? ⭐⭐
##### Answer:
You can use the attribute `df.empty` to check whether it's empty or not:

```python
if df.empty:
    print('DataFrame is empty!')
```

**Source:** _stackoverflow.com_

#### Q7: Compare the Pandas methods: `map()`, `applymap()`, `apply()` ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q8: Name the advantage of using `applymap()` vs `apply()` method ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: When cleaning data, mention how you will _identify outliers_ present in a DataFrame object ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: Describe how you can _combine (merge)_ data on Common Columns or Indices? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: What is the difference between `join()` and `merge()` in Pandas? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: What is the difference(s) between `merge()` and `concat()` in Pandas? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: When to use `merge()` over `concat()` and vice-versa in Pandas? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: How will you write DataFrame to PostgreSQL table? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: Group DataFrame Rows into a List ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: Name some type conversion methods in Pandas ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: Select rows from a DataFrame based on columns value in Pandas? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: Select rows whose column value does not equal `some_value` in Pandas ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: Is it a good idea to _iterate_ over DataFrame rows in Pandas? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: How can you subset DataFrame based on a _list of values_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: Count the `NaN` values in a column in pandas DataFrame ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: How can I achieve the equivalents of SQL's `IN` and `NOT IN` in Pandas? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: How would you create Test (20%) and Train (80%) Datasets with Pandas? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: What are some best-practices to work with _Large Files_ in Pandas? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: Explain what is _Multi-indexing_ in Pandas ? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q26: What is _Vectorization_ in a context of using Pandas? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q27: What are some best practises to _optimize_ Pandas code? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=Probability>Probability</a> Interview Questions
#### Q1: How would you _Calibrate Probabilities_ for a classification model? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q2: Why would you use _Probability Calibration_? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=Python>Python</a> Interview Questions
#### Q1: What are the _built-in types_ available In Python? ⭐
##### Answer:
Common _immutable_ type:

1. numbers: `int()`, `float()`, `complex()`
2. immutable sequences: `str()`, `tuple()`, `frozenset()`, `bytes()`

Common _mutable_ type (almost everything else):

1. mutable sequences: `list()`, `bytearray()`
2. set type: `set()`
3. mapping type: `dict()`
4. classes, class instances
5. etc.

You have to understand that Python represents all its data as objects. Some of these objects like lists and dictionaries are mutable, meaning you can change their content without changing their identity. Other objects like integers, floats, strings and tuples are objects that can not be changed. 

**Source:** _techbeamers.com_

#### Q2: Name some _characteristics_ of Python?  ⭐
##### Answer:
Here are a few key points:

*   Python is an **interpreted language**. That means that, unlike languages like C and its variants, Python does not need to be compiled before it is run. Other interpreted languages include _PHP_ and _Ruby_.
*   Python is **dynamically typed**, this means that you don't need to state the types of variables when you declare them or anything like that. You can do things like `x=111` and then `x="I'm a string"` without error
*   Python is well suited to **object orientated programming** in that it allows the definition of classes along with composition and inheritance. Python does not have access specifiers (like C++'s `public`, `private`), the justification for this point is given as "we are all adults here"
*   In Python, **functions are first-class objects**. This means that they can be assigned to variables, returned from other functions and passed into functions. Classes are also first class objects
*   Writing Python code is quick but running it is **often slower than compiled languages**. Fortunately, Python allows the inclusion of C based extensions so bottlenecks can be optimised away and often are. The `numpy` package is a good example of this, it's really quite quick because a lot of the number crunching it does isn't actually done by Python

**Source:** _codementor.io_

#### Q3: How do I _modify_ a string? ⭐
##### Answer:
You can’t because strings are _immutable_. In most situations, you should simply construct a new string from the various parts you want to assemble it from. Work with them as lists; turn them into strings only when needed.

```py
>>> s = list("Hello zorld")
>>> s
['H', 'e', 'l', 'l', 'o', ' ', 'z', 'o', 'r', 'l', 'd']
>>> s[6] = 'W'
>>> s
['H', 'e', 'l', 'l', 'o', ' ', 'W', 'o', 'r', 'l', 'd']
>>> "".join(s)
'Hello World'
```

**Source:** _docs.python.org_

#### Q4: Name some _benefits_ of Python ⭐⭐
##### Answer:
*   Python is a **dynamic-typed** language. It means that you don’t need to mention the data type of variables during their declaration.
*   Python supports **object-orientated programming** as you can define classes along with the composition and inheritance.
*   **Functions** in Python are like **first-class objects**. It suggests you can assign them to variables, return from other methods and pass them as arguments.
*   Developing using Python is quick but running it is often slower than compiled languages.
*   Python has several usages like web-based applications, test automation, data modeling, big data analytics, and much more.

**Source:** _techbeamers.com_

#### Q5: What is _Lambda Functions_ in Python? ⭐⭐
##### Answer:
A **Lambda Function** is a small anonymous function. A lambda function can take _any_ number of arguments, but can _only_ have _one_ expression.

Consider:
```python
x = lambda a : a + 10
print(x(5)) # Output: 15
```


**Source:** _stackoverflow.com_

#### Q6: When to use a `tuple` vs `list` vs `dictionary` in Python? ⭐⭐
##### Answer:
* Use a `tuple` to store a sequence of items that _will not change_.
* Use a `list` to store a sequence of items that _may change_.
* Use a `dictionary` when you want to associate _pairs_ of two items.

**Source:** _stackoverflow.com_

#### Q7: What are the rules for _local_ and _global_ variables in Python? ⭐⭐
##### Answer:
While in many or most other programming languages variables are treated as global if not declared otherwise, Python deals with variables the other way around. They are local, if not otherwise declared. 

* In Python, variables that are only referenced inside a function are implicitly _global_. 
* If a variable is assigned a value anywhere within the function’s body, it’s assumed to be a _local_ unless explicitly declared as global.

Requiring global for assigned variables provides a bar against unintended side-effects.

**Source:** _docs.python.org_

#### Q8: What is _Negative Index_ in Python? ⭐⭐
##### Answer:
Negative numbers mean that you count from the right instead of the left. So, `list[-1]` refers to the last element, `list[-2]` is the second-last, and so on.

**Source:** _stackoverflow.com_

#### Q9: What are _local variables_ and _global variables_ in Python? ⭐⭐
##### Answer:
* **Global Variables**: Variables declared _outside_ a function or in global space are called global variables. These variables can be accessed by any function in the program.
* **Local Variables**: Any variable declared _inside_ a function is known as a local variable. This variable is present in the local space and not in the global space.

**Source:** _edureka.co_

#### Q10: What are descriptors? ⭐⭐
##### Answer:
Descriptors were introduced to Python way back in version 2.2. They provide the developer with the ability to add managed attributes to objects. The methods needed to create a descriptor are `__get__`, `__set__` and `__delete__`. If you define any of these methods, then you have created a descriptor.

Descriptors power a lot of the magic of Python’s internals. They are what make properties, methods and even the super function work. They are also used to implement the new style classes that were also introduced in Python 2.2.

**Source:** _blog.pythonlibrary.org_

#### Q11: Given variables `a` and `b`, switch their values so that `b` has the value of `a`, and a has the value of `b` _without using an intermediary variable_ ⭐⭐
##### Answer:
```py
a, b = b, a
```

**Source:** _adevait.com_

#### Q12: Suppose `lst` is `[2, 33, 222, 14, 25]`. What is `lst[-1]`? ⭐⭐
##### Details:
Suppose `lst` is `[2, 33, 222, 14, 25]`, What is `lst[-1]`?

##### Answer:
It's `25`. Negative numbers mean that you count from the right instead of the left. So, `lst[-1]` refers to the last element, `lst[-2]` is the second-last, and so on.

**Source:** _adevait.com_

#### Q13: How the _string_ does get converted to a _number_? ⭐⭐
##### Answer:
- To convert the string into a number the built-in functions are used like `int()` constructor. It is a data type that is used like `int (‘1’) == 1`.
- `float()` is also used to show the number in the format as `float(‘1’) = 1`.
- The number by default are interpreted as decimal and if it is represented by `int(‘0x1’)` then it gives an error as `ValueError`. In this the `int(string,base)` function takes the parameter to convert string to number in this the process will be like `int(‘0x1’,16) == 16`. If the base parameter is defined as 0 then it is indicated by an octal and 0x indicates it as hexadecimal number.
- There is function `eval()` that can be used to convert string into number but it is a bit slower and present many security risks

**Source:** _careerride.com_

#### Q14:  Does Python have a _switch-case_ statement? ⭐⭐
##### Answer:
In Python befor 3.10, we **do not hav**e a switch-case statement. Here, you may write a switch function to use. Else, you may use a set of if-elif-else statements. To implement a function for this, we may use a dictionary.

```py
def switch_demo(argument):
    switcher = {
        1: "January",
        2: "February",
        3: "March",
        4: "April",
        5: "May",
        6: "June",
        7: "July",
        8: "August",
        9: "September",
        10: "October",
        11: "November",
        12: "December"
    }
    print switcher.get(argument, "Invalid month")
```

Python 3.10 (2021) introduced the [`match`\-`case`](https://www.python.org/dev/peps/pep-0634/) statement which provides a first-class implementation of a "switch" for Python. For example:

For example:

```python
def f(x):
    match x:
        case 'a':
            return 1
        case 'b':
            return 2
```

The `match`\-`case` statement is considerably more powerful than this simple example.

**Source:** _github.com_

#### Q15: How to make a _flat list out of list of lists_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: What's the difference between `lists` and `tuples`? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: Is it possible to have _static methods_ in Python? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: How do I check if _a list is empty_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: Explain how does Python _memory management_ work? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: What's the difference between the list methods `append()` and `extend()`? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: Why would you use the `pass` statement? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: What are _Decorators_ in Python? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: Is there a tool to help find _bugs_ or perform _static analysis_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: What is _Monkey Patching_ and is it ever a good idea? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: Explain the `UnboundLocalError` exception and how to avoid it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q26: What are immutable objects in Python? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q27: What is the difference between `range` and `xrange` functions in Python? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q28: What is a `None` value? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q29: What is _Pickling_ and _Unpickling_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q30: What does this stuff mean: `*args`, `**kwargs`? Why would we use it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q31: What is the most efficient way to _concatenate_ many strings together? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q32: How can I create a _copy of an object_ in Python? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q33: How can you _share global variables_ across modules? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q34: Write a program to check whether the object is of _a class or its subclass_ ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q35: What are the key differences between Python `2` and `3`? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q36: Is this _valid_ in Python and why? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q37: What is a _Callable_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q38: What is the function of `self`? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q39: What are _virtualenvs_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q40: What does an `x = y or z` assignment do in Python? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q41: What are the _Dunder/Magic/Special_ methods in Python? Name a few. ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q42: What are the _Wheels_ and _Eggs_? What is the difference? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q43: What is the difference between `range` and `xrange`? How has this changed over time? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q44: What is _introspection/reflection_ and does Python support it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q45: What is the python `with` statement designed for? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q46: What does the Python `nonlocal` statement do (in Python 3.0 and later)? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q47: After executing the above code, what is the value of `y`? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q48: Explain how to use _Slicing_ in Python? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q49: How to make _a chain of function decorators_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q50: What is the difference between `@staticmethod` and `@classmethod`? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q51: What are _metaclasses_ in Python? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q52: How do I write a function with _output parameters (call by reference)_ ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q53: What's the difference between a Python _module_ and a Python _package_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q54: Why are _default values_ shared between objects? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q55: What is _GIL_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q56: Is it a good idea to use _multi-thread_ to speed your Python code? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q57: Create function that similar to `os.walk` ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q58: What will be _returned_ by this code? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q59: Whenever you _exit_ Python, is all _memory de-allocated_?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q60: Why Python (CPython and others) uses the _GIL_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q61: Show me _three different ways_ of fetching _every third item_ in the list ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q62: How to work with _transitive dependencies_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q63: How is `set()` implemented internally? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q64: What is _MRO_ in Python? How does it work? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q65: Can you explain _Closures_ (as they relate to Python)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q66: What is an alternative to _GIL_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q67: How is _memory managed_ in Python? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q68: What is the purpose of the single _underscore_ `_` variable in Python? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q69: What is _Cython_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q70: Why are Python's _private_ methods not actually private? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q71: Will the code below work? _Why_ or why not? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q72: What is the difference between _old style_ and _new style_ classes in Python? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q73: What will be the _output of the code_ below? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q74: Explain how you _reverse a generator_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q75: What is the difference between _deep_ and _shallow_ copy? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q76: What is _Monkey Patching_? How to use it in Python? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q77: What are the _advantages of NumPy_ over regular Python _lists_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q78: Why aren't Python _nested functions_ called closures? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q79: What is the difference between a function decorated with `@staticmethod` and one decorated with `@classmethod`? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q80: Why would you use _metaclasses_? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q81: Describe Python's _Garbage Collection mechanism_ in brief ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q82: What will this code _return_? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q83: Is there a simple, elegant way to _define singletons_? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q84: Why use `else` in `try/except` construct in Python? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q85: What is a global interpreter lock (_GIL_) and why is it an issue? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q86: How do I _access a module_ written in Python _from C_? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q87: Is there any downside to the `-O` flag apart from missing on the built-in debugging information? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q88: What does Python optimisation (`-O` or `PYTHONOPTIMIZE`) do? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q89: Why isn't all _memory freed_ when Python _exits_? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q90: How should one access _nonlocal variables in closures_ in python 2.x? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q91: How to read a `8GB` file in Python? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=RandomForests>Random Forests</a> Interview Questions
#### Q1: How would you define *Random Forest*? ⭐
##### Answer:
* **Random Forests** is a type of *ensemble* learning method for *classification*, *regression*, and other tasks.
* **Random Forests** works by constructing many **decision trees** at a training time. The way that this works is by averaging several decision trees at *different parts* of the same training set.

**Source:** _en.wikipedia.org_

#### Q2: Explain how the *Random Forests* give output for *Classification*, and *Regression* problems? ⭐⭐
##### Answer:
* **Classification:** The output of the *Random Forest* is the one selected by the *most trees*.
* **Regression:** The output of the *Random Forest* is the *mean* or *average* prediction of the individual trees.

**Source:** _en.wikipedia.org_

#### Q3: What are *Ensemble Methods*? ⭐⭐
##### Answer:
* **Ensemble methods** is a machine learning technique that combines several base models in order to produce one optimal predictive model.
* **Random Forest** is a type of ensemble method.
* The number of component classifier in an ensemble has a great impact on the accuracy of the prediction, although there is a law of diminishing results in ensemble construction.

**Source:** _towardsdatascience.com_

#### Q4: What are some hyperparameters in *Random Forest*? ⭐⭐
##### Answer:
In **Random Forest** the hyperparameters include:
* Number of *decision trees* in the forest.
* Number of *features* considered by each tree when splitting a *node*.
* The *maximum* depth of the individual trees.
* The *minimum* samples to split on at an internal node.
* The *maximum* number of leaf nodes.
* Number of *random* features.
* The size of the *bootstrapped dataset*.

**Source:** _towardsdatascience.com_

#### Q5: How would you find the optimal size of the *Bootstrapped Dataset*? ⭐⭐
##### Answer:
* Due to the observations being sampled with replacements, even if the size of the *bootstrapped dataset* is different, the datasets will be *different*. 
* Due to this, the *full size of the training data* can be used. 

Most of the time the best thing to do is not touch this hyperparameter.

**Source:** _towardsdatascience.com_

#### Q6: Does Random Forest need *Pruning*? Why or why not? ⭐⭐
##### Answer:
* Pruning is a *data compression* technique in machine learning and search algorithms that reduces the size of decision trees by removing sections of the tree that are *non-critical* and redundant to classify instances.
* **Random Forest** usually does not require *pruning* because it will not over-fit like a single decision tree. This happens due to the fact that the trees are *bootstrapped* and that multiple random trees use random features so the individual trees are strong without being *correlated* with each other.

**Source:** _stats.stackexchange.com_

#### Q7: Is it necessary to do *Cross Validation* in Random Forest? ⭐⭐
##### Answer:
* The **OOB** for a random forest is similar to **Cross Validation**. So, it is not necessary to perform cross-validation.
* By default, *random forest* picks up `2/3rd` data for training and rest for testing for regression and almost `70%` data for training and rest for testing during classification. By principle since it randomizes the variable selection during each tree split it's not prone to *overfit* like other models.

**Source:** _datascience.stackexchange.com_

#### Q8: How is a _Random Forest_ related to _Decision Trees_? ⭐⭐
##### Answer:
* ***Random forest*** is an ***ensemble learning*** method that works by constructing a multitude of ***decision trees***. A random forest can be constructed for both classification and regression tasks.
* Random forest **outperforms** decision trees, and it also does not have the habit of *overfitting* the data as decision trees do.
* A decision tree trained on a specific dataset will become very deep and cause overfitting. To create a random forest, decision trees can be trained on different subsets of the training dataset, and then the different decision trees can be averaged with the goal of _decreasing the variance_.

**Source:** _en.wikipedia.org_

#### Q9: Explain the advantages of using *Random Forest* ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: What are some drawbacks of using *Random Forest*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: Why Random Forest models are considered not _interpretable_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: What is *Out-of-Bag Error*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: Explain the concept behind *BAGGing* ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: What does *Random* refer to in *Random Forest*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: What is the difference between *OOB* score and *validation* score? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: What are *proximities* in Random Forests? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: How does the *number of trees* affect the Random Forest model? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: How would you define the criteria to split on at each node of the trees? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: How do you determine the *Depth of the Individual Trees*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: Why is the training efficiency of *Random Forest* better than *Bagging*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: How does *Random Forest* handle missing values? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: What is *Entropy* criteria used to split a node? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: What is *Variable Selection* and what are its *Objectives* in Random Forest? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: How would you improve the performance of Random Forest? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: How is it possible to perform *Unsupervised Learning* with Random Forest? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q26: When would you use *SVMs* over *Random Forest* and vice-versa? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q27: Give some reasons to choose *Random Forests* over *Neural Networks* ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q28: What are some advantages of *Neural Network* over *Random Forest*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q29: What is *Gini Impurity* used to split a node? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q30: How can you tell the importance of features using *Random Forest*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q31: Explain how it is possible to get *feature importance* in *Random Forest* using *Out Of Bag Error* ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q32: Imagine that you know there are _outliers_ in your data, would you use _Logistic Regression_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q33: How would you find the optimal *number of random features* to consider at each split? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q34: Explain a method of *Variable Selection* for *Random Forest* ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=SQL>SQL</a> Interview Questions
#### Q1: What is a `VIEW`? ⭐
##### Answer:
A **view** is simply a virtual table that is made up of elements of multiple physical or “real” tables. Views are most commonly used to join multiple tables together, or control access to any tables existing in background server processes.	

**Source:** _github.com/dhaval1406_

#### Q2: Define a _Temp Table_  ⭐
##### Answer:
In a nutshell, a **temp table** is a _temporary storage structure_. Basically, you can use a temp table to store data _temporarily_ so you can manipulate and change it before it reaches its destination format.

**Source:** _github.com/dhaval1406_

#### Q3: What is `PRIMARY KEY`? ⭐
##### Answer:
* A **PRIMARY KEY** constraint is a _unique identifier_ for a row within a database table. 
* Every table _should have_ a primary key constraint to uniquely identify each row and only one primary key constraint can be created for each table. 
* The primary key constraints are used to enforce _entity integrity_.

**Source:** _github.com/dhaval1406_

#### Q4: What is `DEFAULT`? ⭐⭐
##### Answer:
* **Default** allows to add values to the column _if the value of that column is not set_. 
* Default can be defined on number and datetime fields. 
* They cannot be defined on timestamp and `IDENTITY` columns.

**Source:** _github.com/chetansomani_

#### Q5: What is `FOREIGN KEY`? ⭐⭐
##### Answer:
* **FOREIGN KEY** constraint _prevents_ any actions that would destroy links between tables with the corresponding data values. 
* A foreign key in one table _points_ to a primary key in another table. 
* Foreign keys prevent actions that would leave rows with foreign key values when there are no primary keys with that value. 
* The foreign key constraints are used to **enforce referential integrity**.

**Source:** _github.com/dhaval1406_

#### Q6: What is _Normalisation_? ⭐⭐
##### Answer:
**Normalization** is basically to design a database schema such that **duplicate and redundant data is avoided**. If the same information is repeated in multiple places in the database, there is the risk that it is updated in one place but not the other, leading to data corruption.

There is a number of normalization levels from 1. normal form through 5. normal form. Each normal form describes how to get rid of some specific problem.

By having a database with normalization errors, you open the risk of getting invalid or corrupt data into the database. Since data "lives forever" it is very hard to get rid of corrupt data when first it has entered the database.

**Source:** _stackoverflow.com_

#### Q7: What is the difference between `TRUNCATE` and `DELETE`? ⭐⭐
##### Answer:
* **DELETE** is a Data Manipulation Language(DML) command. It can be used for deleting some specified rows from a table. **DELETE** command can be used with **WHERE** clause.

* **TRUNCATE** is a Data Definition Language(DDL) command. It deletes all the records of a particular table. **TRUNCATE** command is faster in comparison to **DELETE**. While **DELETE** command can be rolled back, **TRUNCATE** can not be rolled back in MySQL.


**Source:** _stackoverflow.com_

#### Q8: What is the difference between _Data Definition Language (DDL)_ and _Data Manipulation Language (DML)_? ⭐⭐
##### Answer:
* **Data definition language (DDL)** commands are the commands which are used to define the database. **CREATE**, **ALTER**, **DROP** and **TRUNCATE** are some common DDL commands.

* **Data manipulation language (DML)** commands are commands which are used for manipulation or modification of data. **INSERT**, **UPDATE** and **DELETE** are some common DML commands.

**Source:** _en.wikibooks.org_

#### Q9: What is the difference between `JOIN` and `UNION`? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: Discuss `INNER JOIN ON` vs `WHERE` clause (with multiple `FROM` tables) ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: Describe the difference between truncate and delete  ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: Find _duplicate_ values in a SQL table ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: What is the difference between `INNER JOIN`, `OUTER JOIN`, `FULL OUTER JOIN`? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: What is the difference between `UNION` and `UNION ALL`?	 ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: Define ACID Properties ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: How a database index can help performance? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: What is Denormalization? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: What is the difference between `WHERE` clause and `HAVING` clause? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: What are the difference between _Clustered_ and a _Non-clustered_ index? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: How does a _Hash_ index work? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: How to select first `5` records from a table? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: What is the difference between `INNER JOIN` and `OUTER JOIN`? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: What is _Collation_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: What's the difference between a _Primary Key_ and a _Unique Key_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: How can _View_ be used to provide _security layer_ for your app? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q26: How would you implement Linear Regression Function in SQL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q27: What is the _cost_ of having a database _index_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q28: How to generate row number in SQL _without_ `ROWNUM` ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q29: Explain the difference between _Exclusive Lock_ and _Update Lock_ ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q30: How does _B-trees Index_ work? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q31: What is the difference among `UNION`, `MINUS` and `INTERSECT`? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q32: How can I do an `UPDATE` statement with `JOIN` in SQL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q33: How can we _transpose_ a table using SQL (changing rows to column or vice-versa)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q34: How does `TRUNCATE` and `DELETE` operations effect _Identity_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q35: Delete _duplicate_ values in a SQL table ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q36: What would happen _without_ an Index? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q37: What is faster, _one big_ query or _many small_ queries? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q38: What are some _other_ types of Indexes (vs B-Trees)? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q39: Name some disadvantages of a _Hash index_ ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q40: What is _Optimistic Locking_ and _Pessimistic Locking_? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q41: Select first row in each `GROUP BY` group (greatest-n-per-group problem)? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q42: How does database _Indexing_ work? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q43: What is the difference between _B-Tree_, _R-Tree_ and _Hash_ indexing? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=SVM>SVM</a> Interview Questions
#### Q1: What is Support Vector Machine? ⭐
##### Answer:
**Support vector machines (SVMs)** are a set of supervised learning methods used for _classification_, _regression_ and _outliers detection_. The objective of the **support vector machine** algorithm is to find a **hyperplane** in an N-dimensional space(N — the number of features) that distinctly classifies the data points.

![](https://miro.medium.com/max/1400/1*ZpkLQf2FNfzfH4HXeMw4MQ.png)

Support vector machines focus only on the points that are the most difficult to tell apart, whereas other classifiers pay attention to all of the points.

The intuition behind the support vector machine approach is that if a classifier is good at the most challenging comparisons (the points in B and A that are closest to each other), then the classifier will be even better at the easy comparisons (comparing points in B and A that are far away from each other).

**Source:** _towardsdatascience.com_

#### Q2: What is _Hyperplane_ in SVM? ⭐⭐
##### Answer:
**Hyperplanes** are **decision boundaries** that help classify the data points. Data points falling on either side of the hyperplane can be attributed to different classes. Also, the dimension of the hyperplane depends upon the number of features. If the number of input features is 2, then the hyperplane is just a line. If the number of input features is 3, then the hyperplane becomes a two-dimensional plane.

To separate the two classes of data points, there are many possible hyperplanes that could be chosen. Our objective is to find a plane that has the maximum margin, i.e the maximum distance between data points of both classes. Maximizing the margin distance provides some reinforcement so that future data points can be classified with more confidence.

![](https://miro.medium.com/max/600/0*0o8xIA4k3gXUDCFU.png)


**Source:** _towardsdatascience.com_

#### Q3: What are *Support Vectors* in SVMs? ⭐⭐
##### Answer:
* **Support vectors** are the data points nearest to the hyperplane, the points of a data set that, if removed, would alter the position of the dividing hyperplane. 
* Using these support vectors, we maximize the margin of the classifier.
* For computing predictions, *only* the support vectors are used.

![](https://miro.medium.com/max/1400/0*ecA4Ls8kBYSM5nza.jpg)

**Source:** _towardsdatascience.com_

#### Q4: What happens when there is no clear Hyperplane in SVM? ⭐⭐
##### Answer:
* Data is rarely as clean that hyperplane is a line that linearly separates and classifies a set of data. In order to classify a dataset, it’s necessary to move away from a 2D view of the data to a 3D view.
* This ‘lifting’ of the data points represents the _mapping of data_ into a _higher dimension_. This is known as kernelling. 

![](https://66.media.tumblr.com/9bffea56372d28d2a30f80557451e824/tumblr_inline_o9aabehtqP1u37g00_540.png)

* In this example, the picture on the left shows our original data points. In 1-dimension, this data is not linearly separable, but after applying the transformation *ϕ*(x) = x² and adding this second dimension to our feature space, the classes become linearly separable.

![](https://miro.medium.com/max/2000/1*NwhqamsvzBkUlYwSAubv5g.png)

**Source:** _www.kdnuggets.com_

#### Q5: What are *Hard-Margin* and *Soft-Margin* SVMs? ⭐⭐
##### Answer:
* **Hard-Margin** SVMs have *linearly separable* training data. No data points are allowed in the margin areas. This type of linear classification is known as Hard margin classification.
* **Soft-Margin** SVMs have training data that are not *linearly separable*. Margin violation means choosing a hyperplane, which can allow some data points to stay either in between the margin area or on the incorrect side of the hyperplane.

![](https://miro.medium.com/max/552/1*CD08yESKvYgyM7pJhCnQeQ.png)

* **Hard-Margin** SVMs are quite sensitive to outliers.
* **Soft-Margin** SVMs try to find the best balance between keeping the margin as large as possible and limiting the margin violations.

**Source:** _towardsdatascience.com_

#### Q6: What are some applications of SVMs? ⭐⭐
##### Answer:
SVMs depends on **supervised learning** algorithms. The aim of using SVM is to correctly _classify_ unseen data.
Some common applications of SVM are:

- **Face detection** – SVMc classify parts of the image as a face and non-face and create a square boundary around the face.
- **Text and hypertext categorization** – SVMs allow Text and hypertext categorization for both inductive and transductive models. They use training data to classify documents into different categories. It categorizes on the basis of the score generated and then compares with the threshold value.
- **Classification of images** – Use of SVMs provides better search accuracy for image classification. It provides better accuracy in comparison to the traditional query-based searching techniques.
- **Bioinformatics** – It includes protein classification and cancer classification. We use SVM for identifying the classification of genes, patients on the basis of genes and other biological problems.
- **Protein fold and remote homology detection** – Apply SVM algorithms for protein remote homology detection.
- **Handwriting recognition** – We use SVMs to recognize handwritten characters used widely.
- **Generalized predictive control(GPC)** – Use SVM based GPC to control chaotic dynamics with useful parameters.

**Source:** _data-flair.training_

#### Q7: Name some _advantages_ of SVM ⭐⭐
##### Answer:
- **Guaranteed Optimality**: Owing to the nature of Convex Optimization, the solution will always be global minimum not a local minimum.
- **Abundance of Implementations**: We can access it conveniently, be it from Python or Matlab.
- SVM can be used for _linearly separable_ as well as _non-linearly separable_ data. Linearly separable data is the hard margin whereas non-linearly separable data poses a soft margin.
- SVMs _provide compliance_ to the semi-supervised learning models. It can be used in areas where the data is labeled as well as unlabeled. It only requires a condition to the minimization problem which is known as the Transductive SVM.
- _Feature Mapping_ used to be quite a load on the computational complexity of the overall training performance of the model. However, with the help of **Kernel Trick**, SVM can carry out the feature mapping using a simple dot product.

**Source:** _data-flair.training_

#### Q8: For `N` dimensional data set what is the _minimum possible number_ of Support Vectors? ⭐⭐
##### Details:
Let's say I am not using any kind of kernel, and it is a hard-margin SVM.

##### Answer:
* For a hard-margin SVM all of the support vectors lie exactly on the margin. 
* _Regardless_ of the number of _dimensions_ or size of the data set, the number of support vectors could be as little as `2`.

![](https://i.stack.imgur.com/qt3CZ.png)

**Source:** _stats.stackexchange.com_

#### Q9: What types of _SVM kernels_ do you know? ⭐⭐
##### Answer:
- **Linear kernel**: Also referred to as the _Non-kernel_, is defined as the inner product of `x` and `y` with an optional constant term `c`. 
  $$
K(x,y) = x^Ty + c
$$
  Is typically used on data sets with large amounts of features.

- **Polynomial Kernel**: is a more generalized form of the _linear kernel_, can distinguish _curved_ or _nonlinear_ input space. 
$$
K(x,) = (\alpha x^T y + c)^d
$$
where the three parameters are `𝛼`, `c`, and `d`. The most common degree `d` used is `2` as larger degrees can lead to overfitting.

- **The Radial Basis Function Kernel**: can map an input space in infinite-dimensional space, is defined as: 
$$
K(x,y) = e^{-\gamma ||x-y||^2}
$$
 where `𝛾` is a parameter that scales the amount of influence two points have on each other, its range lies from `0` to `1`. A higher value of gamma will perfectly fit the training dataset, which causes overfitting. Generally, a `𝛾 = 0.1` is considered to be a good default value.

**Source:** _www.datacamp.com_

#### Q10: Why would you use the _Kernel Trick_? ⭐⭐
##### Answer:
When it comes to **classification** problems, the goal is to establish a decision boundary that maximizes the margin between the classes. However, in the real world, this task can become difficult when we have to treat with **non-linearly separable data**. One approach to solve this problem is to perform a data transformation process, in which we map all the data points to a **higher dimension** find the boundary and make the classification.

That sounds alright, however, when there are more and more dimensions, computations within that space become more and more expensive. In such cases, the **kernel trick allows us to operate in the original feature space without computing the coordinates of the data** in a higher-dimensional space and therefore offers a more efficient and less expensive way to transform data into higher dimensions.

There exist different kernel functions, such as:
- _linear_, 
- _nonlinear_, 
- _polynomial_, 
- _radial basis function (RBF)_, and 
- _sigmoid_. 

Each one of them can be suitable for a particular problem depending on the data.  


**Source:** _medium.com_

#### Q11: How to use _one-class SVM_ for Anomalies Detections? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: What are _Support Vectors_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: Compare *SVM* and *Logistic Regression* in handling outliers ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: What is the *Kernel Trick*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: What is the *Hinge Loss* in SVM? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: What is the role of *C* hyperparameter in SVM? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: What is the difference between *Classification* and *Regression* when using SVM? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: What is _Quadratic Optimisation Problem_ in SVM? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: While designing an *SVM* classifier, what values should the designer select? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: What are the *Convex Hulls*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: What are *Polynomial Kernels*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: When would you use *SVMs* over *Random Forest* and vice-versa? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: What are some similarities between *SVMs* and *Neural Networks*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: What are some differences between *SVMs* and *Neural Networks*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: Compare *K-Nearest Neighbors (KNN)* and *SVM* ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q26: When SVM is _not_ a good approach? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q27: What is _Ranking SVM_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q28: Provide an intuitive explanation of _Linear Support Vector Machines (SVMs)_ ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q29: What are *Slack Variables* in SVM? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q30: Why is the *Lagrangian* important in SVM? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q31: What are _C_ and _Gamma (γ)_ with regards to a Support Vector Machine? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q32: What is the *Dual Problem*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q33: Can you explain _PAC_ learning theory _intuitively_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q34: How does the value of *Gamma* affect the SVM? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q35: How does the value of *C* affect the SVM? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q36: Is there a relation between the _Number of Support Vectors_ and the classifiers performance? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q37: Explain the *dual form* of SVM formulation ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q38: What are *Radial Basis Function Kernels*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q39: What is *Sequential Minimal Optimization*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q40: What is *Structured SVM*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q41: What is the difference between _Deep Learning_ and _SVM_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q42: Name some advantages of using _Support Vector Machines_ vs _Logistic Regression_ for classification ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q43: When would you use _SVM_ vs _Logistic regression_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q44: How would you deal with classification on _Non-linearly Separable_ data? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q45: What is *Mercer's theorem* and how is it related to SVM? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q46: What is the *Probably Approximately Correct* learning? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q47: How do you approximate _RBF kernel to scale_ with large numbers of training samples? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q48: Why is SVM not popular nowadays? Also, when did SVM perform poorly? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q49: Why does SVM work well in practice, even if the reproduced space is very high dimensional? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=Scikit-Learn>Scikit-Learn</a> Interview Questions
#### Q1: How would you create Test (20%) and Train (80%) Datasets with Pandas? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=Searching>Searching</a> Interview Questions
#### Q1: Explain what is Binary Search ⭐⭐
##### Answer:
When the list is **sorted** we can use the **binary search** (also known as half-interval search, logarithmic search, or binary chop) technique to find items on the list. Here's a step\-by\-step description of using binary search:

1.  Let `min = 1` and `max = n`.
2.  Guess the average of `max` and `min`  **rounded down** so that it is an integer.
3.  If you guessed the number, stop. You found it!
4.  If the guess was too low, set _min_ to be one larger than the guess.
5.  If the guess was too high, set _max_ to be one smaller than the guess.
6.  Go back to step two.

In this example we looking for array item with value `4`:
![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/64/Binary_search_into_array_-_example.svg/382px-Binary_search_into_array_-_example.svg.png)

When you do one operation in binary search we reduce the size of the problem **by half** (look at the picture below how do we reduce the size of the problem area) hence the complexity of binary search is <code><i>O</i>(<i>log n</i>)</code>. The binary search algorithm can be written either _recursively_ or _iteratively_.

![](https://dirask.com/static/bucket/1575232592915-67oY6qqQE1--binarry_search_algorithm.png)

**Source:** _www.tutorialspoint.com_

##### Complexity Analysis:
**Time Complexity**: O(log n)
**Space Complexity**: O(log n)
##### Implementation:
##### _JS_

```js
var binarySearch = function(array, value) {
    var guess,
        min = 0,
        max = array.length - 1;	

    while(min <= max){
        guess = Math.floor((min + max) /2);
	if(array[guess] === value)
	    return guess;
	else if(array[guess] < value)
	    min = guess + 1;
	else
	    max = guess - 1;	
     }
	
     return -1;
}
```


##### _Java_

```java
// binary search example in Java
/* here Arr is an of integer type, n is size of array 
   and target is element to be found */

int binarySearch(int Arr[], int n, int target) {

	//set stating and ending index
	int start = 0, ending = n-1;

	while(start <= ending) {
		// take mid of the list
		int mid = (start + end) / 2;

		// we found a match
		if(Arr[mid] == target) {
			return mid; 
		}
		// go on right side
		else if(Arr[mid] < target) {
			start = mid + 1;
		}
		// go on left side
		else {
			end = mid - 1;
		}
	}
	// element is not present in list
	return -1;
}
```


##### _PY_

```py
def BinarySearch(lys, val):
    first = 0
    last = len(lys)-1
    index = -1
    while (first <= last) and (index == -1):
        mid = (first+last)//2
        if lys[mid] == val:
            index = mid
        else:
            if val<lys[mid]:
                last = mid -1
            else:
                first = mid +1
    return index
```


#### Q2: Explain what is Linear (Sequential) Search and when may we use one? ⭐⭐
##### Answer:
**Linear (sequential) search** goes through all possible elements in some array and compare each one with the desired element. It may take up to <code><i>O</i>(<i>n</i>)</code> operations, where N is the size of an array and is widely considered to be horribly slow. In linear search when you perform one operation you reduce the size of the problem _by one_ (when you do one operation in binary search you reduce the size of the problem _by half_). Despite it, it can still be used when:

* You need to perform this search only once,
* You are _forbidden_ to rearrange the elements and you do not have any extra memory,
* The array is tiny, such as ten elements or less, or the performance is not an issue at all,
* Even though in theory other search algorithms may be faster than linear search (for instance binary search), in practice even on medium-sized arrays (around 100 items or less) it might be infeasible to use anything else. On larger arrays, it only makes sense to use other, faster search methods if the data is large enough, because the initial time to prepare (sort) the data is comparable to many linear searches,
* When the list items are arranged in order of _decreasing probability_, and these probabilities are geometrically distributed, the cost of linear search is only <code><i>O</i>(<i>1</i>)</code>
* You have no idea what you are searching.

When you ask MySQL something like `SELECT x FROM y WHERE z = t`, and `z` is a column _without_ an index, linear search is performed with all the consequences of it. This is why adding an index to _searchable_ columns is important.

**Source:** _bytescout.com_

##### Complexity Analysis:
**Time Complexity**: O(n)
**Space Complexity**: O(n)

* A linear search runs in at worst _linear time_ and makes at most `n` comparisons, where `n` is the length of the list. If each element is _equally likely_ to be searched, then linear search has an average case of `(n+1)/2` comparisons, but the average case can be affected if the search probabilities for each element vary.
* When the list items are arranged in order of _decreasing probability_, and these probabilities are geometrically distributed, the cost of linear search is only <code><i>O</i>(<i>1</i>)</code>
##### Implementation:
##### _JS_

```js
function linearSearch(array, toFind){
  for(let i = 0; i < array.length; i++){
    if(array[i] === toFind) return i;
  }
  return -1;
}
```


##### _PY_

```py
# can be simply done using 'in' operator
if x in arr:
   print arr.index(x)
 
# If you want to implement Linear Search in Python
def search(arr, x):
    for i in range(len(arr)):
        if arr[i] == x:
            return i
 
    return -1
```


#### Q3: Explain some Linear Search optimization techniques ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q4: Recursive and Iterative Binary Search: Which one is more efficient and why? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q5: Explain what is Interpolation Search ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q6: Write a program for Recursive Binary Search ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q7: What's wrong with this Recursive Binary Search function? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q8: Compare Binary Search vs Linear Search ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: What is an example of Interpolation Search being slower than Binary Search? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: Which of the following algorithms would be the fastest? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: What is a Jump (or Block) Search? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: Explain why complexity of Binary Search is <code><i>O</i>(<i>log n</i>)</code>? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: Explain how does the Sentinel Search work? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: Explain what is _Fibonacci Search_ technique? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: For Binary Search why do we need round down the average? Could we round up instead? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: How to apply Binary Search <code><i>O</i>(<i>log n</i>)</code> on a sorted Linked List? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: Explain when and how to use Exponential (aka Doubling or Galloping) Search?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: What is the optimal block size for a Jump Search? Explain. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: Explain what is Ternary Search? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: How is it possible to do Binary Search on a Doubly-Linked List in <code><i>O</i>(<i>n</i>)</code> time? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: Why would you ever do Binary Search on a Doubly-Linked list? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: Is Sentinel Linear Search better than normal Linear Search? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: Why use Binary Search if there's ternary search? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: When Jump Search is a better alternative than a Binary Search? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=Sorting>Sorting</a> Interview Questions
#### Q1: Explain how Bubble Sort works ⭐
##### Answer:
**Bubble Sort** is based on the idea of repeatedly _comparing_ pairs of adjacent elements and then swapping their positions if they are in the wrong order. Bubble sort is a _stable_, _in-place_ sort algorithm.

How it works:
* In an unsorted array of `n` elements, start with the first two elements and sort them in ascending order. (Compare the element to check which one is greater).
* Compare the second and third element to check which one is greater, and sort them in ascending order.
* Compare the third and fourth element to check which one is greater, and sort them in ascending order.
* ...
* Repeat steps 1–`n` until no more swaps are required.

**Visualisation:**


![](https://camo.githubusercontent.com/383b23979d4d7f279f8fb285b36bcdd357b10a35/68747470733a2f2f75706c6f61642e77696b696d656469612e6f72672f77696b6970656469612f636f6d6d6f6e732f632f63382f427562626c652d736f72742d6578616d706c652d33303070782e676966)


**Source:** _github.com_

##### Complexity Analysis:
**Time Complexity**: O(n^2)
**Space Complexity**: O(n^2)

Bubble sort has a worst-case and average complexity of <code><i>O</i>(<i>n</i><sup>2</sup>)</code>, where `n` is the number of items being sorted. When the list is already sorted (best-case), the complexity of bubble sort is only `O(n)`. The space complexity for Bubble Sort is `O(1)`, because only single additional memory space is required (for `temp` swap element).
##### Implementation:
##### _JS_

```js
// Normal
const bubbleSort = function(array) {
  let swaps;
  do {
    swaps = false;
    for (let i = 0; i < array.length - 1; i++) {
      if (array[i] > array[i + 1]) {
        let temp = array[i + 1];
        array[i + 1] = array[i];
        array[i] = temp;
        swaps = true;
      }
    }
  } while (swaps);
  
  return array;
};

// Recursively
const bubbleSort = function (array, pointer = array.length - 1) {
  // Base Case
  if (pointer === 0) {
    return array;
  }

  for (let i = 0; i < pointer; i++) {
    if (array[i] > array[i + 1]) {
      let temp = array[i + 1];
      array[i + 1] = array[i];
      array[i] = temp;
    }
  }   
  // Recursive call on smaller portion of the array
  return bubbleSort(array, pointer - 1);  
};
```

##### _PY_

```py
def bubbleSort(arr):
    n = len(arr)
 
    # Traverse through all array elements
    for i in range(n):
 
        # Last i elements are already in place
        for j in range(0, n-i-1):
 
            # traverse the array from 0 to n-i-1
            # Swap if the element found is greater
            # than the next element
            if arr[j] > arr[j+1] :
                arr[j], arr[j+1] = arr[j+1], arr[j]
```

#### Q2: Why Sorting algorithms are important? ⭐
##### Answer:
Efficient sorting is important for **optimizing the efficiency of other algorithms** (such as search and merge algorithms) that require input data to be in sorted lists. Sorting is also often useful for canonicalizing data and for producing human-readable output. Sorting have direct applications in database algorithms, divide and conquer methods, data structure algorithms, and many more.

**Source:** _en.wikipedia.org_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
#### Q3: What is meant by to "Sort in Place"? ⭐⭐
##### Answer:
The idea of an in-place algorithm isn't unique to sorting, but sorting is probably the most important case, or at least the most well-known. The idea is about space efficiency - using the minimum amount of RAM, hard disk or other storage that you can get away with. 

The idea is to **produce an output in the same memory space that contains the input** by successively transforming that data until the output is produced. This avoids the need to use twice the storage - one area for the input and an equal-sized area for the output.

**Quicksort** is one example of In-Place Sorting.

**Source:** _stackoverflow.com_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
#### Q4: Explain what is ideal Sorting algorithm? ⭐⭐
##### Answer:
The **Ideal Sorting Algorithm** would have the following properties:

* **Stable**: Equal keys aren’t reordered.
* **Operates in place:** requiring `O(1)` extra space.
* Worst-case `O(n log n)` key comparisons.
* Worst-case `O(n)` swaps.
* **Adaptive**: Speeds up to `O(n)` when data is nearly sorted or when there are few unique keys.

There is **no** algorithm that has all of these properties, and so the choice of sorting algorithm depends on the application.

**Source:** _www.toptal.com_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
#### Q5: Classify Sorting Algorithms ⭐⭐
##### Answer:
Sorting algorithms can be categorised based on the following parameters:

1.  **Based on Number of Swaps or Inversion**. This is the number of times the algorithm swaps elements to sort the input. `Selection Sort` requires the minimum number of swaps.
2.  **Based on Number of Comparisons**. This is the number of times the algorithm compares elements to sort the input. Using Big-O notation, the sorting algorithm examples listed above require at least <code><i>O</i>(<i>n log n</i>)</code> comparisons in the best case and <code><i>O</i>(<i>n</i><sup>2</sup>)</code> comparisons in the worst case for most of the outputs.
3.  **Based on Recursion or Non-Recursion**. Some sorting algorithms, such as `Quick Sort`, use recursive techniques to sort the input. Other sorting algorithms, such as `Selection Sort` or `Insertion Sort`, use non-recursive techniques. Finally, some sorting algorithm, such as `Merge Sort`, make use of both recursive as well as non-recursive techniques to sort the input.
4.  **Based on Stability**. Sorting algorithms are said to be `stable` if the algorithm maintains the relative order of elements with equal keys. In other words, two equivalent elements remain in the same order in the sorted output as they were in the input.
    *  `Insertion sort`, `Merge Sort`, and `Bubble Sort` are stable
    *  `Heap Sort` and `Quick Sort` are not stable
5.  **Based on Extra Space Requirement.** Sorting algorithms are said to be _in place_ if they require a constant <code><i>O</i>(<i>1</i>)</code> extra space for sorting.
    *  `Insertion sort` and `Quick-sort` are `in place` sort as we move the elements about the pivot and do not actually use a separate array which is NOT the case in merge sort where the size of the input must be allocated beforehand to store the output during the sort.
    *  `Merge Sort` is an example of `out place` sort as it require extra memory space for it’s operations.

**Source:** _www.freecodecamp.org_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
#### Q6: Explain how Insertion Sort works ⭐⭐
##### Answer:
**Insertion Sort** is an _in-place_, _stable_, _comparison-based_ sorting algorithm. The idea is to maintain a sub-list which is always sorted. An element which is to be 'insert'ed in this sorted sub-list, has to find its appropriate place and then it has to be inserted there. Hence the name, **insertion sort**.

Steps on how it works:
* If it is the first element, it is already sorted.
* Pick the next element.
* Compare with all the elements in sorted sub-list.
* Shift all the the elements in sorted sub-list that is greater than the value to be sorted.
* Insert the value.
* Repeat until list is sorted.

**Visualisation:**


![](https://upload.wikimedia.org/wikipedia/commons/0/0f/Insertion-sort-example-300px.gif)

**Source:** _medium.com_

##### Complexity Analysis:
**Time Complexity**: O(n^2)
**Space Complexity**: O(n^2)

* Insertion sort runs in <code><i>O</i>(<i>n</i><sup>2</sup>)</code> in its worst and average cases. It runs in `O(n)` time in its best case.
* Insertion sort performs two operations: it scans through the list, comparing each pair of elements, and it swaps elements if they are out of order. Each operation contributes to the running time of the algorithm. If the input array is already in sorted order, insertion sort compares `O(n)` elements and performs no swaps. Therefore, in the best case, insertion sort runs in `O(n)` time.
* Space complexity is `O(1)` because an extra variable key is used (as a temp variable for insertion).
##### Implementation:
##### _JS_

```js
var insertionSort = function(a) {
    // Iterate through our array
    for (var i = 1, value; i < a.length; i++) {
        // Our array is split into two parts: values preceeding i are sorted, while others are unsorted
        // Store the unsorted value at i
        value = a[i];
        // Interate backwards through the unsorted values until we find the correct location for our `next` value
        for (var j = i; a[j - 1] > value; j--) {
            // Shift the value to the right
            a[j] = a[j - 1];
        }
        // Once we've created an open "slot" in the correct location for our value, insert it
        a[j] = value;
    }
    // Return the sorted array
    return a;
};
```

##### _Java_

```java
import java.util.Arrays;

class InsertionSort {

  void insertionSort(int array[]) {
    int size = array.length;

    for (int step = 1; step < size; step++) {
      int key = array[step];
      int j = step - 1;

      // Compare key with each element on the left of it until an element smaller than
      // it is found.
      // For descending order, change key<array[j] to key>array[j].
      while (j >= 0 && key < array[j]) {
        array[j + 1] = array[j];
        --j;
      }

      // Place key at after the element just smaller than it.
      array[j + 1] = key;
    }
  }

  // Driver code
  public static void main(String args[]) {
    int[] data = { 9, 5, 1, 4, 3 };
    InsertionSort is = new InsertionSort();
    is.insertionSort(data);
    System.out.println("Sorted Array in Ascending Order: ");
    System.out.println(Arrays.toString(data));
  }
}
```

##### _PY_

```py
def insertionSort(array):

    for step in range(1, len(array)):
        key = array[step]
        j = step - 1
        
        # Compare key with each element on the left of it until an element smaller than it is found
        # For descending order, change key<array[j] to key>array[j].        
        while j >= 0 and key < array[j]:
            array[j + 1] = array[j]
            j = j - 1
        
        # Place key at after the element just smaller than it.
        array[j + 1] = key

data = [9, 5, 1, 4, 3]
insertionSort(data)
print('Sorted Array in Ascending Order:')
print(data)
```

#### Q7: What are advantages and disadvantages of Bubble Sort? ⭐⭐
##### Answer:
**Advantages:**

* Simple to understand
* Ability to detect that the list is sorted efficiently is built into the algorithm. When the list is already sorted (best-case), the complexity of bubble sort is only `O(n)`. 


**Disadvantages:**
* It is very slow and runs in <code><i>O</i>(<i>n</i><sup>2</sup>)</code> time in worst as well as average case. Because of that Bubble sort does not deal well with a large set of data. For example Bubble sort is three times slower than **Quicksort** even for n = 100



**Source:** _en.wikipedia.org_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
#### Q8: How would you optimise Bubble Sort? ⭐⭐
##### Answer:
In Bubble sort, you know that after `k` passes, the largest `k` elements are sorted at the `k` last entries of the array, so the conventional Bubble sort uses:
```java
public static void bubblesort(int[] a) {
  for (int i = 1; i < a.length; i++) {
    boolean is_sorted = true;

    for (int j = 0; j < a.length - i; j++) { // skip the already sorted largest elements, compare to a.length - 1
      if (a[j] > a[j+1]) {
         int temp = a[j];
         a[j] = a[j+1];
         a[j+1] = temp;
         is_sorted = false;
      }
    }

    if(is_sorted) return;
  }
}
```
Now, that would still do a lot of unnecessary iterations when the array has a long sorted tail of largest elements. If you remember where you made your _last swap_, you know that after that index, there are the largest elements in order, so:

```java
public static void bubblesort(int[] a) {
  int lastSwap = a.length - 1;
  for (int i = 1; i< a.length; i++) {
    boolean is_sorted = true;
    int currentSwap = -1;

    for (int j = 0; j < lastSwap; j++) { // compare to a.length - i
      if (a[j] > a[j+1]) {
         int temp = a[j];
         a[j] = a[j+1];
         a[j+1] = temp;
         is_sorted = false;
         currentSwap = j;
      }
    }

    if (is_sorted) return;
    lastSwap = currentSwap;
  }
}
```
This allows to skip over many elements, resulting in about a worst case 50% improvement in comparison count (though no improvement in swap counts), and adds very little complexity.

**Source:** _stackoverflow.com_

##### Complexity Analysis:
**Time Complexity**: None
**Space Complexity**: None
#### Q9: Insert an item in a sorted Linked List maintaining order ⭐⭐
##### Answer:
The `add()` method below walks down the list until it finds the appropriate position. Then, it splices in the new node and updates the `start`, `prev`, and `curr` pointers where applicable.

Note that the reverse operation, namely _removing_ elements, doesn't need to change, because you are simply throwing things away which would not change any order in the list.


**Source:** _stackoverflow.com_

##### Implementation:
##### _Java_

```java
public void add(T x) {
    Node newNode = new Node();
    newNode.info = x;

    // case: start is null; just assign start to the new node and return
    if (start == null) {
        start = newNode;
        curr = start;
        // prev is null, hence not formally assigned here
        return;
    }

    // case: new node to be inserted comes before the current start;
    //       in this case, point the new node to start, update pointers, and return
    if (x.compareTo(start.info) < 0) {
        newNode.link = start;
        start = newNode;
        curr = start;
        // again we leave prev undefined, as it is null
        return;
    }

    // otherwise walk down the list until reaching either the end of the list
    // or the first position whose element is greater than the node to be
    // inserted; then insert the node and update the pointers
    prev = start;
    curr = start;
    while (curr != null && x.compareTo(curr.info) >= 0) {
        prev = curr;
        curr = curr.link;
    }

    // splice in the new node and update the curr pointer (prev already correct)
    newNode.link = prev.link;
    prev.link = newNode;
    curr = newNode;
}
```


#### Q10: Explain how _Heap Sort_ works ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: Which of the following algorithms would be the fastest? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: What's the difference between External vs Internal sorting? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: Explain how Merge Sort works ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: Which sort algorithm works best on mostly sorted data? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: Why would you use Merge Sort for a Linked List? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: When is each Sorting algorithm used? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: When is Quicksort better than Mergesort? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: What is "stability" in sorting algorithms and why is it important? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: Sort a Stack using Recursion ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: Sort a Stack using another Stack ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: Explain how _QuickSort_ works ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: Why is Merge sort preferred over Quick sort for sorting Linked Lists? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: Explain how Radix Sort works ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: Explain how to find 100 largest numbers out of an array of 1 billion numbers ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: When Merge Sort is preferred over Quick Sort? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q26: How can I pair socks from a pile efficiently? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=Statistics>Statistics</a> Interview Questions
#### Q1: What is _Normal Distribution_? ⭐⭐
##### Answer:
The **normal distribution** is the most important probability distribution in [statistics](https://statisticsbyjim.com/glossary/statistics/) because it fits many natural phenomena. For example, heights, blood pressure, measurement error, and IQ scores follow the normal distribution. It is also known as the Gaussian distribution and the bell curve.

![](https://cdn.analystprep.com/cfa-level-1-exam/wp-content/uploads/2019/10/05093814/page-123.jpg)

**Normal distributions** have the following features:

- symmetric bell shape
- _mean_ and _median_ and _mode_ are equal; both located at the center of the distribution
- ≈68% of the data falls within 1 standard deviation of the mean
- ≈95% of the data falls within 2 standard deviations of the mean
- ≈99.7% of the data falls within 3 standard deviations of the mean

**Source:** _statisticsbyjim.com_

#### Q2: What's the difference between _Normalisation_ and _Standardisation_? ⭐⭐
##### Answer:
**Normalization** rescales the values into a range of \[0,1\].  This might be useful in some cases where all parameters need to have the same positive scale. However, the _outliers_ from the data set _are lost._

$$
X_{changed} = \frac{X - X_{min}}{X_{max}-X_{min}}
$$ 

**Standardization** rescales data to have a mean ($\mu$) of 0 and standard deviation ($\sigma$) of 1 (unit variance).

$$
X_{changed} = \frac{X - \mu}{\sigma}
$$        

For most applications standardization is recommended.

![](https://i.stack.imgur.com/WqU1U.png)

**Source:** _stats.stackexchange.com_

#### Q3: In _statistics_, what is the difference between _Bias_ and _Error_? ⭐⭐
##### Answer:
* We can talk about the **error** of a single measurement, but **bias** is the _average of errors_ of many repeated measurements,
* **Bias is a statistical property of the error of a measuring technique**,
* Sometimes the term "bias error" is used as opposed to "root-mean-square error".

**Source:** _stats.stackexchange.com_

#### Q4: What is the difference between the _Standard Error of the Mean_ and _Standard Deviation_? ⭐⭐
##### Answer:
- The **standard deviation** (SD) measures the amount of variability, or dispersion, from the _individual data_ values _to the mean_. It's defined as: 
  $$\sigma = \sqrt{  \frac{\sum_{i=1}^n (x_i - \bar{x})^2   }{n-1}   }$$
- The **standard error of the mean** (SEM) measures how far the _sample mean_ (average) of the data is likely to be from the _true population mean_. It's defined as:
  $$\sigma_{\bar{x}} = \frac{\sigma}{\sqrt{n}}$$

Therefore, the relationship between the _standard error of the mean_ and the _standard deviation_ is such that, for given sample size, the standard error of the mean equals the standard deviation divided by the _square root_ of the _sample size_.

**Source:** _www.investopedia.com_

#### Q5: What's the difference between _Confidence Interval_ and _Confidence Level_? ⭐⭐
##### Answer:
- The **confidence level** is the percentage of times we expect to get close to the same estimate if we run our experiment again or resample the population in the same way.

- The **confidence interval** is the actual upper and lower bounds of the estimate we expect to find at a given level of confidence.

For example, if we are estimating a `95%` _confidence interval_ around the mean proportion of female babies born every year based on a random sample of babies, we might find an upper bound of `0.56` and a lower bound of `0.48`. These are the upper and lower bounds of the _confidence interval_ for a _confidence level_ of `95%`.

This means that `95%` of the time, we can expect our estimate to fall between `0.56` and `0.48`.

![https://uploads-cdn.omnicalculator.com/images/confidence_interval/confidence_interval_95.png](https://uploads-cdn.omnicalculator.com/images/confidence_interval/confidence_interval_95.png)

**Source:** _www.scribbr.com_

#### Q6: Why would you use the _Median_ as a measure of central tendency? ⭐⭐
##### Answer:
The **Median** is the most suitable measure of _central tendency_ for **skewed distributions** or distributions with **outliers**. For example, the median is often used as a measure of central tendency for income distributions, which are generally highly skewed.

Because the median only uses one or two values, it’s unaffected by extreme _outliers_ or _non-symmetric distributions_ of scores. In contrast, the **_mean_** and **_mode_** can vary in skewed distributions.

![https://miro.medium.com/max/754/0*wHMvuwRa_YF9SFwY.png](https://miro.medium.com/max/754/0*wHMvuwRa_YF9SFwY.png)

**Source:** _en.wikipedia.org_

#### Q7: What is _Central Tendency_? ⭐⭐
##### Answer:
A measure of **central tendency** is a single value that attempts to _describe_ a set of data by identifying the **central position** within that set of data. In the simplest of terms, it attempts to find a single value that best represents an entire distribution of scores. 

**Mean**, **Median** and **Mode** are average values or **central tendency** of a numerical data set.

**Source:** _statistics.laerd.com_

#### Q8: What is _Statistical Significance_? ⭐⭐
##### Answer:
**Statistical significance** is a term used by researchers to state that it is unlikely their observations could have occurred under the [null hypothesis](https://www.scribbr.com/statistics/hypothesis-testing/) of a [statistical test](https://www.scribbr.com/statistics/statistical-tests/). Significance is usually denoted by a [_p_\-value](https://www.scribbr.com/statistics/p-value/), or probability value.

Statistical significance is arbitrary – it depends on the threshold, or alpha value, chosen by the researcher. The most common threshold is _p_ < 0.05, which means that the data is likely to occur less than 5% of the time under the null hypothesis.

When the _p_\-value falls below the chosen alpha value, then we say the result of the test is statistically significant.

**Source:** _www.scribbr.com_

#### Q9: How many types of _means_ do you know? ⭐⭐
##### Answer:
- **Arithmetic mean**: It’s often simply called the _mean_ or the _average_ and is the sum of all values divided by the total number of values. 
  $$\bar{x} = \frac{1}{n} \sum_{i=1}^n x_i$$
- **Geometric mean**: is often used for a set of numbers whose values are meant to be multiplied together or are exponential, such as values of the human population or interest rates of a financial investment over time.
  $$\bar{x} = \prod_{i=1}^n x_i $$
- **Harmonic mean**: is an average that is often used in averaging things like _rates_ as in the case of speed (i.e., distance per unit of time).
  $$\bar{x} = n \left( \sum_{i=1}^n \frac{1}{x_i}  \right)^{-1}$$

**Source:** _en.wikipedia.org_

#### Q10: Can there be more than one _Mode_? ⭐⭐
##### Answer:
The **mode** is the value that appears most frequently in a data set. A set of data may have one mode, more than one mode, or no mode at all. A data set can often have no mode, one mode, or more than one mode – it all depends on how many different values repeat most frequently.

> For example, in the following list of numbers, 16 is the mode since it appears more times in the set than any other number:
- 3, 3, 6, 9, **16, 16, 16**, 27, 27, 37, 48

Your data can be:

*   without any mode
*   **unimodal**, with one mode,
*   **bimodal**, with two modes,
*   **trimodal**, with three modes, or
*   **multimodal**, with four or more modes.

**Source:** _www.scribbr.com_

#### Q11: What is the _Empirical Rule_? ⭐⭐
##### Answer:
The empirical rule, or the `68-95-99.7` rule, tells you where most of the values lie in a [normal distribution](https://www.scribbr.com/statistics/normal-distribution/):

- Around `68%` of values are within `1` [standard deviation](https://www.scribbr.com/statistics/standard-deviation/) of the mean.
- Around `95%` of values are within `2` standard deviations of the mean.
- Around `99.7%` of values are within `3` standard deviations of the mean.

> The empirical rule is a quick way to get an overview of your data and check for any outliers or extreme values that don’t follow this pattern.

**Source:** _www.scribbr.com_

#### Q12: What is the difference between _Descriptive Statistics_ and _Inferential Statistics_? ⭐⭐
##### Answer:
- **Descriptive statistics**, as its name suggests, focus on _describing_ the characteristics or features of a dataset. Here we look for measures of _distribution_, _central tendency_ and _variability_ in order to draw conclusions based on known data.

- **Inferential statistics** focus on making _generalizations_ about a larger population based on a representative sample of that population, It also allows us to make _predictions_ so its results are usually in the form of a _probability_. Here, we perform _hypothesis testing_, compute _confidence intervals_, make _regression_ and _correlation_ analyses, in order to draw conclusions that go beyond the available data.

**Source:** _careerfoundry.com_

#### Q13: Explain how to use _Standard Deviation_ for Anomalies Detection? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: What is the *F-Score*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: in which use-case we should use _Mean_ and when to use _Median_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: How do you reduce the risk of making a _Type I_ and _Type II_ error? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: What a _p-value_ tells you about _statistical significance_ of observation? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: What is the _Central Limit Theorem (CLT)_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: How many _Levels of Measures_ do you know? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: How many _Sampling Techniques_ do you know? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: What does a _Statistical Test_ do? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: How would you choose the _Statistical Test_ to use? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: State _null_ and _alternate_ hypothesis for  a relationship between gender and height ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: What's the difference between _z-score_ and _t-score_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: How many types of _Descriptive Statistics_ do you know? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q26: How would you assess the _Statistical Significance_ of an insight? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q27: When you sample, what potential _Sampling Biases_ could you be inflicting? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q28: What's the difference between *Homoskedasticity* and *Heteroskedasticity*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q29: How would you calculate a _Confidence Interval_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q30: How many types of measures of _Variability_ do you know? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q31: When would you use the _Interquartile Range (IQR)_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q32: What's the difference between *Kurtosis* and *Skewness*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q33: When would you use a *t-test*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q34: How would you determine the needed _Sample Size_? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q35: How would you calculate a _Confidence Interval_ for _non normally distributed_ data? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q36: Is _mean imputation_ of missing data acceptable practice? Why or why not? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q37: What is the difference between _Central Limit Theorem_ and the _Law of Large Numbers_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q38: How would you increase the _Statistical Power_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q39: What is a _Long Tail_ distribution? How they are produced in real life?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q40: What's the difference between _Covariance_ and _Correlation_? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q41: Which measures of _Variability_ would you use on your data? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q42: How would you calculate and evaluate the _Effect Size_? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q43: How does an ANOVA test work? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=SupervisedLearning>Supervised Learning</a> Interview Questions
#### Q1: What is Support Vector Machine? ⭐
##### Answer:
**Support vector machines (SVMs)** are a set of supervised learning methods used for _classification_, _regression_ and _outliers detection_. The objective of the **support vector machine** algorithm is to find a **hyperplane** in an N-dimensional space(N — the number of features) that distinctly classifies the data points.

![](https://miro.medium.com/max/1400/1*ZpkLQf2FNfzfH4HXeMw4MQ.png)

Support vector machines focus only on the points that are the most difficult to tell apart, whereas other classifiers pay attention to all of the points.

The intuition behind the support vector machine approach is that if a classifier is good at the most challenging comparisons (the points in B and A that are closest to each other), then the classifier will be even better at the easy comparisons (comparing points in B and A that are far away from each other).

**Source:** _towardsdatascience.com_

#### Q2: What is _Linear Regression_? ⭐
##### Answer:
**Linear Regression** is a supervised machine learning algorithm where the predicted output is continuous and has a constant slope. It’s used to predict values within a _continuous range_, (e.g. sales, price) rather than trying to classify them into categories (e.g. cat, dog). 

**Source:** _ml-cheatsheet.readthedocs.io_

#### Q3: What are *Decision Trees*? ⭐
##### Answer:
* ***Decision trees*** is a tool that uses a *tree-like model* of decisions and their possible consequences. If an algorithm only contains *conditional control statements*, decision trees can model that algorithm really well.
* *Decision trees* are a *non-parametric*, _supervised_ learning method.
* *Decision trees* are used for *classification* and *regression* tasks.
* The diagram below shows an example of a decision tree (the dataset used is the Titanic dataset to predict whether a passenger survived or not):

![decision](https://miro.medium.com/max/540/1*XMId5sJqPtm8-RIwVVz2tg.png)

**Source:** _towardsdatascience.com_

#### Q4: What do you understand by the term *Supervised Learning*? ⭐
##### Answer:
* ***Supervised learning*** is a subcategory of *machine learning* and *artificial intelligence*.
* It has a * **labeled** dataset*. Each **input** has a corresponding **output**, and algorithms are trained to **predict the output based on the input**.
* As input data is fed into the model, it adjusts the *weights* until the model is fitted properly.

**Source:** _www.ibm.com_

#### Q5: What are the two types of problems solved by *Supervised Learning*? ⭐
##### Answer:
Supervised learning can be separated into two types of problems when data mining:
* **Classification:** It uses algorithms to assign the test data into specific categories. Common classification algorithms are *linear classifiers*, *support vector machines* (SVM), *decision trees*, *k-nearest neighbor*, and *random forest*.
* **Regression:** It is used to understand the relationship between *dependent* and *independent* variables. *Linear regression*, *logistical regression*, and *polynomial regression* are popular regression algorithms.

**Source:** _www.ibm.com_

#### Q6: What is the difference between _Supervised Learning_ and _Unsupervised Learning_? ⭐⭐
##### Answer:
* **Supervised learning** is when the data you feed your algorithm with is _tagged_ or _labelled_, to help your logic make decisions.
 
 _Example_: a hypothetical non-machine learning algorithm for face detection in images would try to define what a face is (round skin-like-colored disk, with dark area where you expect the eyes etc). A machine learning algorithm would not have such coded definition, but would "learn-by-examples": you'll show several images of faces and not-faces and a good algorithm will eventually learn and be able to predict whether or not an unseen image is a face.

* **Unsupervised learning** are types of algorithms that try to find correlations without any external inputs other than the raw data (your examples are not _labeled_, i.e. you don't say anything).  In such a case the algorithm itself cannot "invent" what a face is, but it can try to **cluster** the data into different groups, e.g. it can distinguish that faces are very different from landscapes, which are very different from horses.

**Source:** _stackoverflow.com_

#### Q7: Give a real life example of _Supervised Learning_ and _Unsupervised Learning_ ⭐⭐
##### Answer:
* **Supervised** learning examples:
  - You get a bunch of photos **with information about what is on them** and then you train a model to recognize new photos.
  - You have a bunch of molecules and **information about which are drugs** and you train a model to answer whether a new molecule is also a drug.
  - Based on past information about spams, filtering out a new incoming email into **Inbox** (normal) or **Junk folder** (Spam)
  - Cortana or any speech automated system in your mobile phone trains your voice and then starts working based on this training.
  - Train your handwriting to OCR system and once trained, it will be able to convert your hand-writing images into text (till some accuracy obviously)

* **Unsupervised** learning examples:

  * You have a bunch of photos of 6 people but **without information about who is on which one** and you want to **divide** this dataset into 6 piles, each with the photos of one individual.
  * You have molecules, part of them are drugs and part are not **but you do not know which are which** and you want the algorithm to discover the drugs.
  - A friend invites you to his party where you meet totally strangers. Now you will classify them using unsupervised learning (no prior knowledge) and this classification can be on the basis of gender, age group, dressing, educational qualification or whatever way you would like. **Why this learning is different from Supervised Learning? Since you didn't use any past/prior knowledge about people and classified them "on-the-go".**
  - NASA discovers new heavenly bodies and finds them different from previously known astronomical objects - stars, planets, asteroids, blackholes etc. (i.e. it has no knowledge about these new bodies) and classifies them the way it would like to (distance from Milky way, intensity, gravitational force, red/blue shift or whatever)
  - Let's suppose you have never seen a Cricket match before and by chance watch a video on internet, now you can classify players on the basis of different criterion: Players wearing same sort of kits are in one class, Players of one style are in one class (batsmen, bowler, fielders), or on the basis of playing hand (RH vs LH) or whatever way you would observe [and classify] it.

**Source:** _stackoverflow.com_

#### Q8: What is _Bias_ in Machine Learning? ⭐⭐
##### Answer:
In supervised machine learning an algorithm learns a model from training data.

The goal of any supervised machine learning algorithm is to best estimate the mapping function (f) for the output variable (Y) given the input data (X). The mapping function is often called the target function because it is the function that a given supervised machine learning algorithm aims to approximate.

**Bias** are **the simplifying assumptions** made by a model to make the target function easier to learn.

Generally, linear algorithms have a high bias making them fast to learn and easier to understand but generally less flexible.

* Examples of **low\-bias** machine learning algorithms include: Decision Trees, k\-Nearest Neighbors and [Support Vector Machines](https://machinelearningmastery.com/support-vector-machines-for-machine-learning/).

* Examples of **high\-bias** machine learning algorithms include: Linear Regression, Linear Discriminant Analysis and Logistic Regression.

**Source:** _machinelearningmastery.com_

#### Q9: Why Naive Bayes is called _Naive_? ⭐⭐
##### Answer:
We call it **naive** because its assumptions (it assumes that all of the features in the dataset are equally important and independent) are really optimistic and rarely true in most real-world applications:
- we consider that these _predictors_ are _independent_
- we consider that all the predictors have an _equal effect_ on the outcome (like the day being windy does not have more importance in deciding to play golf or not)

**Source:** _towardsdatascience.com_

#### Q10: What is a *Perceptron*? ⭐⭐
##### Answer:
* A **Perceptron** is a fundamental unit of a Neural Network that is also a single-layer Neural Network.
* Perceptron is a linear _classifier_. Since it uses already labeled data points, it is a *supervised learning algorithm*.  
* The _activation function_ applies a step rule (convert the numerical output into +1 or -1) to check if the output of the weighting function is greater than zero or not.

A **Perceptron** is shown in the figure below:

![perception](https://www.programmersought.com/images/258/633dca25508a646a6df343339c3d4eaa.png)


**Source:** _towardsdatascience.com_

#### Q11: What is the difference between _KNN_ and _K-means Clustering_? ⭐⭐
##### Answer:
- **_K-nearest neighbors_** or _KNN_ is a _supervised classification algorithm_. This means that we need labeled data to classify an unlabeled data point. It attempts to classify a data point based on its proximity to other `K`-data points in the feature space.

- **_K-means Clustering_** is an _unsupervised classification algorithm_. It requires only a set of unlabeled points and a threshold `K`, so it gathers and groups data into `K` number of clusters.

**Source:** _www.quora.com_

#### Q12: Explain the _structure_ of a Decision Tree ⭐⭐
##### Answer:
A ***decision tree*** is a ***flowchart-like*** structure in which:
* Each *internal node* represents the ***test*** on an attribute (e.g. outcome of a coin flip).
* Each *branch* represents the **_outcome_** of the test.
* Each *leaf node* represents a ***class label***.
* The _paths_ from the root to leaf represent the ***classification rules***.

![https://aiaspirant.com/wp-content/uploads/2020/02/dt_struct.png](https://aiaspirant.com/wp-content/uploads/2020/02/dt_struct.png)

**Source:** _en.wikipedia.org_

#### Q13: How are the different nodes of decision trees _represented_? ⭐⭐
##### Answer:
A **decision tree** consists of three **types** of nodes:
* **Decision nodes:** Represented by **squares.** It is a node where a flow branches into several optional branches.
* **Chance nodes:** Represented by **circles.** It represents the probability of certain results.
* **End nodes:** Represented by **triangles.** It shows the final outcome of the decision path.

![decision_nodes](https://upload.wikimedia.org/wikipedia/commons/a/ad/Decision-Tree-Elements.png)

**Source:** _en.wikipedia.org_

#### Q14: In _statistics_, what is the difference between _Bias_ and _Error_? ⭐⭐
##### Answer:
* We can talk about the **error** of a single measurement, but **bias** is the _average of errors_ of many repeated measurements,
* **Bias is a statistical property of the error of a measuring technique**,
* Sometimes the term "bias error" is used as opposed to "root-mean-square error".

**Source:** _stats.stackexchange.com_

#### Q15: What is the *Bias-Variance* tradeoff? ⭐⭐
##### Answer:
* **High Bias** can cause an algorithm to miss the relevant relations between features and target outputs (*underfitting*).
* **High Variance** may result from an algorithm modeling random noise in the training data (*overfitting*).
![https://community.alteryx.com/t5/image/serverpage/image-id/52874iE986B6E19F3248CF?v=v2](https://community.alteryx.com/t5/image/serverpage/image-id/52874iE986B6E19F3248CF?v=v2)


* The **Bias-Variance tradeoff** is a central problem in _supervised learning_. Ideally, a model should be able to accurately capture the regularities in its training data, but also generalize well to unseen data.
* It is called a *tradeoff* because it is typically impossible to do both simultaneously:  
  * Algorithms with _high variance_ will be prone to _overfitting_ the dataset, but 
  * Algorithms with *high bias* will _underfit_ the dataset.

![bias_variance_tradeoff](https://miro.medium.com/max/883/1*8sV6Sr9uc0Ef39YBivLzrw.jpeg)

**Source:** _en.wikipedia.org_

#### Q16: What is the difference between a *Regression* problem and a *Classification* problem? ⭐⭐
##### Answer:
* **Classification** is the problem of identifying which set of *categories* an *observation* belongs to.
* **Regression** is a set of statistical processes for estimating the relationships between a *dependent variable* and an *independent variable*.
###

* **Classification** is used to predict the values of a _categorical_ variable, so the output is generally in the form of integers, or binary (`0` or `1`).
* **Regression** is used to predict a _continuous_ variable, so the output is also a floating-point number (`0.1`, `0.74`, `0.69`, etc.).

![](https://res.cloudinary.com/practicaldev/image/fetch/s--c4Lfzdwy--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/mjshszqx4fj22hs12vfn.png)

**Source:** _en.wikipedia.org_

#### Q17: What is *Linear Regression*? ⭐⭐
##### Answer:
* ***Linear regression*** is a linear approach for modeling the relationship between a *scalar* response and one or more *explanatory variables*.
* In a *supervised linear regression*, the model tries to find a linear relationship between the input and output data points. This linear relationship is a *straight line* if graphed.
* If there is only one *explanatory* variable it is called *simple linear regression*, and if there are more than one *explanatory* variable it is called *multiple linear regression*.
* A linear function is given by the following equation:
$$
y = X\beta + \epsilon
$$
where all the variables are matrices containing data points.

![linear_regression](https://miro.medium.com/max/1400/1*I-MxKoiWxJXLfExpvbT1eQ.png)

**Source:** _en.wikipedia.org_

#### Q18: What is *k-Nearest Neighbors* algorithm? ⭐⭐
##### Answer:
* ***k-Nearest Neighbors*** is a supervised machine learning algorithm that can be used to solve both *classification* and *regression* problems.
* It assumes that _similar things are closer to each other_ in certain feature spaces, in other words, similar things are in close proximity.

![knn](https://miro.medium.com/max/917/1*wW8O-0xVQUFhBGexx2B6hg.png)

* The image above shows how similar points are closer to each other. KNN hinges on this assumption being true enough for the algorithm to be useful.
* There are many different ways of calculating the distance between the points, however, the straight line distance (Euclidean distance) is a popular and familiar choice.

**Source:** _towardsdatascience.com_

#### Q19: What is *Cross-Validation* and why is it important in supervised learning? ⭐⭐
##### Answer:
* ***Cross-validation*** is a method of assessing _how the results of a statistical analysis will generalize on an independent dataset_,
* It can be used in machine learning tasks to _evaluate the predictive capability of the model_,
*   It also helps us to _avoid overfitting and underfitting_,
* A common way to cross-validate is to divide the dataset into *training*, *validation*, and *testing* where:

  * **Training dataset** is a dataset of known data on which the training is run.
  * **Validation dataset** is the dataset that is *unknown* against which the model is tested. The validation dataset is used after each epoch of learning to gauge the improvement of the model.
  * **Testing dataset** is also an unknown dataset that is used to test the model. The testing dataset is used to measure the performance of the model after it has finished learning.

![cross_validation](https://s3.ap-south-1.amazonaws.com/myinterviewtrainer-domestic/public_assets/assets/000/000/094/original/Cross-Validation.png?1614946006)

**Source:** _en.wikipedia.org_

#### Q20: What is the difference between a _Multiclass problem_ and a _Multilabel problem_? ⭐⭐
##### Answer:
**Multiclass classification** means a classification task with more than two classes; e.g., classify a set of images of fruits which may be oranges, apples, or pears. Multiclass classification makes the assumption that each sample is _assigned to one and only one label_: a fruit can be either an apple or a pear but not both at the same time.

**Multilabel classification** assigns to each sample a set of target labels. This can be thought of as predicting properties of a data-point that are _not mutually exclusive_, such as topics that are relevant for a document. A text might be about any of religion, politics, finance or education at the same time or none of these.

![https://i.stack.imgur.com/XghaO.png](https://i.stack.imgur.com/XghaO.png)

**Source:** _stats.stackexchange.com_

#### Q21: What is the *Bias Error*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: What is the *Variance Error*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: What are some challenges faced when using a *Supervised Regression Model*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: How do you use a supervised *Logistic Regression* for Classification? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: What is a *Confusion Matrix*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q26: How is *Gradient Boosting* used to improve supervised learning? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q27: What are some _disadvantages_ of *Supervised Learning*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q28: What is the difference between *Supervised* and *Unsupervised* learning? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q29: What is the difference between *Gradient Boosting* and *Adaptive Boosting*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q30: What is *Semi-Supervised* learning? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q31: How do you choose between *Supervised* and *Unsupervised* learning? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

## [[⬆]](#toc) <a name=TensorFlow>TensorFlow</a> Interview Questions
## [[⬆]](#toc) <a name=UnsupervisedLearning>Unsupervised Learning</a> Interview Questions
#### Q1: What are some applications of *Unsupervised Learning*? ⭐
##### Answer:
Some common real-world applications of unsupervised learning are:
* **News selections:** Google News uses unsupervised learning to _categorize articles_ on the same story from various online news outlets.
* **Computer vision:** Unsupervised learning algorithms are used for visual perception tasks, such as _object recognition_.
* **Medical imaging:** Unsupervised machine learning provides essential features to medical imaging devices, such as image detection, classification, and segmentation, used in _radiology_ and _pathology_ to _diagnose patients_ quickly and accurately.
* **Anomaly detection:** Unsupervised learning models can comb through large amounts of data and _discover atypical data points_ within a dataset. These anomalies can raise awareness around _faulty equipment_, _human error_, or _breaches in security_.

**Source:** _www.ibm.com_

#### Q2: What are some common Machine Learning problems that *Unsupervised Learning* can help with? ⭐
##### Answer:
Some common challenges that _unsupervised learning_ can help with are:
* **Insufficient labeled data:** For *supervised learning*, there is a requirement for a lot of labeled data for the model to perform well. *Unsupervised learning* can automatically label unlabeled examples. This would work by clustering all the data points and then applying the labels from the labeled ones to the unlabeled ones.
* **Overfitting:** Machine learning algorithms can sometimes overfit the training data by extracting too much from the *noise* in the data. When this happens, the algorithm is memorizing the training data rather than learning how to generalize the knowledge of the training data. Unsupervised learning can be introduced as a *regularizer*. *Regularization* is a process that helps to reduce the complexity of a machine learning algorithm, helping it capture the signal in the data without adjusting too much to the noise.
* **Outliers:** The quality of data is very important. If machine learning algorithms train on outliers (rare cases) then their generalization error will be lower than if they are ignored. *Unsupervised learning* can perform outlier detection using *dimensionality reduction* and create solutions specifically for the outliers, and separately, a solution for the normal data.
* **Feature engineering:** Feature engineering is a vital task for data scientists to perform, but feature engineering is very labor-intensive, and it requires a human to creatively engineer the features. *Representation learning* from unsupervised learning can be used to automatically learn the right type of features to help the task at hand.

**Source:** _www.amazon.com_

#### Q3: What is the difference between _Supervised Learning_ and _Unsupervised Learning_? ⭐⭐
##### Answer:
* **Supervised learning** is when the data you feed your algorithm with is _tagged_ or _labelled_, to help your logic make decisions.
 
 _Example_: a hypothetical non-machine learning algorithm for face detection in images would try to define what a face is (round skin-like-colored disk, with dark area where you expect the eyes etc). A machine learning algorithm would not have such coded definition, but would "learn-by-examples": you'll show several images of faces and not-faces and a good algorithm will eventually learn and be able to predict whether or not an unseen image is a face.

* **Unsupervised learning** are types of algorithms that try to find correlations without any external inputs other than the raw data (your examples are not _labeled_, i.e. you don't say anything).  In such a case the algorithm itself cannot "invent" what a face is, but it can try to **cluster** the data into different groups, e.g. it can distinguish that faces are very different from landscapes, which are very different from horses.

**Source:** _stackoverflow.com_

#### Q4: Give a real life example of _Supervised Learning_ and _Unsupervised Learning_ ⭐⭐
##### Answer:
* **Supervised** learning examples:
  - You get a bunch of photos **with information about what is on them** and then you train a model to recognize new photos.
  - You have a bunch of molecules and **information about which are drugs** and you train a model to answer whether a new molecule is also a drug.
  - Based on past information about spams, filtering out a new incoming email into **Inbox** (normal) or **Junk folder** (Spam)
  - Cortana or any speech automated system in your mobile phone trains your voice and then starts working based on this training.
  - Train your handwriting to OCR system and once trained, it will be able to convert your hand-writing images into text (till some accuracy obviously)

* **Unsupervised** learning examples:

  * You have a bunch of photos of 6 people but **without information about who is on which one** and you want to **divide** this dataset into 6 piles, each with the photos of one individual.
  * You have molecules, part of them are drugs and part are not **but you do not know which are which** and you want the algorithm to discover the drugs.
  - A friend invites you to his party where you meet totally strangers. Now you will classify them using unsupervised learning (no prior knowledge) and this classification can be on the basis of gender, age group, dressing, educational qualification or whatever way you would like. **Why this learning is different from Supervised Learning? Since you didn't use any past/prior knowledge about people and classified them "on-the-go".**
  - NASA discovers new heavenly bodies and finds them different from previously known astronomical objects - stars, planets, asteroids, blackholes etc. (i.e. it has no knowledge about these new bodies) and classifies them the way it would like to (distance from Milky way, intensity, gravitational force, red/blue shift or whatever)
  - Let's suppose you have never seen a Cricket match before and by chance watch a video on internet, now you can classify players on the basis of different criterion: Players wearing same sort of kits are in one class, Players of one style are in one class (batsmen, bowler, fielders), or on the basis of playing hand (RH vs LH) or whatever way you would observe [and classify] it.

**Source:** _stackoverflow.com_

#### Q5: What is Principal Component Analysis (PCA)? ⭐⭐
##### Answer:
**Principal Component Analysis (PCA)** is an unsupervised, non-parametric statistical technique primarily used for **dimensionality reduction** in machine learning.

Principal component analysis is a useful technique when dealing with large datasets. In some fields, (bioinformatics, internet marketing, etc) we end up collecting data which has many thousands or tens of thousands of dimensions. Manipulating the data in this form is not desirable, because of practical considerations like memory and CPU time. However, we can't just arbitrarily ignore dimensions either. We might lose some of the information we are trying to capture!

Principal component analysis is a common method used to manage this tradeoff. The idea is that we can somehow select the 'most important' directions, and keep those, while throwing away the ones that contribute mostly noise. 

For example, this picture shows a 2D dataset being mapped to one dimension: 

 ![](http://i.imgur.com/s4Q1Aru.gif)

Note that the dimension chosen was not one of the original two: in general, it won't be, because that would mean your variables were uncorrelated to begin with.  
We can also see that the direction of the principal component is the one that maximizes the variance of the projected data. This is what we mean by 'keeping as much information as possible.'


**Source:** _math.stackexchange.com_

#### Q6: What is the difference between _KNN_ and _K-means Clustering_? ⭐⭐
##### Answer:
- **_K-nearest neighbors_** or _KNN_ is a _supervised classification algorithm_. This means that we need labeled data to classify an unlabeled data point. It attempts to classify a data point based on its proximity to other `K`-data points in the feature space.

- **_K-means Clustering_** is an _unsupervised classification algorithm_. It requires only a set of unlabeled points and a threshold `K`, so it gathers and groups data into `K` number of clusters.

**Source:** _www.quora.com_

#### Q7: What is the *Curse of Dimensionality* and how can Unsupervised Learning help with it? ⭐⭐
##### Answer:
* As the amount of data required to train a model increases, it becomes harder and harder for machine learning algorithms to handle. **As more features are added to the machine learning process, the more difficult the training becomes.**
* In very *high-dimensional* space, supervised algorithms learn to separate points and build function approximations to make good predictions. 

> When the number of *features* increases, this **search becomes expensive**, both from a time and compute perspective. It might become impossible to find a good solution fast enough. This is the *curse of dimensionality*.

* Using ***dimensionality reduction*** of unsupervised learning, the most _salient_ features can be discovered in the original feature set. Then the dimension of this feature set can be reduced to a more manageable number while losing very little information in the process. This will help supervised learning find the optimum function to approximate the dataset.

**Source:** _www.amazon.com_

#### Q8: How is it possible to perform *Unsupervised Learning* with Random Forest? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q9: What is the difference between *Supervised* and *Unsupervised* learning? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q10: What are some differences between *Unsupervised Learning* and *Reinforcement Learning*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q11: Describe the approach used in *Denoising Autoencoders* ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q12: What is the difference between the two types of *Hierarchical Clustering*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q13: How does *K-Means* perform Clustering? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q14: What are some advantages of using *LLE* over *PCA*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q15: How do you choose between *Supervised* and *Unsupervised* learning? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q16: Why does *K-Means* have a higher *bias* when compared to *Gaussian Mixture Model*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q17: Can you use *Batch Normalisation* in *Sparse Auto-encoders*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q18: What are the main differences between *Sparse Autoencoders* and *Convolution Autoencoders*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q19: What are some differences between the *Undercomplete Autoencoder* and the *Sparse Autoencoder*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q20: Explain how a cluster is formed in the *DBSCAN* Clustering Algorithm ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q21: How is *PCA* used for *Anomaly Detection*? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q22: Explain the *Locally Linear Embedding* algorithm for _Dimensionality Reduction_ ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q23: How to tell if data is _clustered_ enough for clustering algorithms to produce meaningful results? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q24: Are *GAN*s unsupervised? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

#### Q25: How can *Neural Networks* be _Unsupervised_? 
Read answer on 👉 <a href='https://www.mlstack.cafe'>MLStack.Cafe</a>

