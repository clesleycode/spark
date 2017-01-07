Intro to Apache Spark
==================

Brought to you by [Lesley Cordero](http://www.columbia.edu/~lc2958).

## Table of Contents

- [0.0 Setup](#00-setup)
	+ [0.1 R and R Studio](#01-r-and-r-studio)
	+ [0.2 Packages](#02-packages)
- [1.0 Background](#10-background)
	+ [1.1 Machine Learning](#11-Machine Learning)
	+ [1.2 Data](#12-data)
	+ [1.3 Overfitting vs Underfitting](#13-overfitting-vs-underfitting)
	+ [1.4 Glossary](#14-glossary)
		* [1.4.1 Factors](#141-factors)
		* [1.4.2 Corpus](#142-corpus)
		* [1.4.3 Bias](#143-bias)
		* [1.4.4 Variance](#144-variance)
- [2.0 Data Preparation](#30-data-preparation)
	+ [2.1 dplyr](#31-dplyr)
	+ [2.2 Geopandas](#32-geopandas)
- [3.0 Exploratory Analysis](#30-exploratory-analysis)
- [4.0 Data Visualization](#50-data-visualization)
- [5.0 Machine Learning & Prediction](#50-machine-learning--prediction)
	+ [5.1 Random Forests](#51-random-forests)
	+ [5.2 Natural Language Processing](#52-natural-language-processing)
		* [5.2.1 ANLP](#521-anlp)
	+ [5.3 K Means Clustering](#53-k-means-clustering)
- [6.0 Final Exercise]($60-final-exercise)
- [7.0 Final Words](#60-final-words)
	+ [7.1 Resources](#61-resources)
	+ [7.2 More!](#72-more)


## 0.0 Setup

This guide was written in Python 3.5.


### 0.1 Python and Pip

Download [Python](https://www.python.org/downloads/) and [Pip](https://pip.pypa.io/en/stable/installing/).

### 0.2 Modules


```
```

### 0.3 Other 

Follow [these](https://www.dataquest.io/blog/pyspark-installation-guide/) instructions for PySpark setup! 

## 1.0 Background




### DeepSpark

DeepSpark uses cutting-edge neural networks to automate the manual processes of software development, including writing test cases, fixing bugs, implementing features according to specs, and reviewing pull requests (PRs) for their correctness, simplicity, and style. As a multifaceted program trained to examine diffs against Spark code base, DeepSpark automatically writes its own patches for Spark. By reviewing PRs, this AI can both enforce a high and consistent standard for code quality as well as make constructive suggestions. Additionally, DeepSpark, during its code scanning, is capable of generating code for new components of Spark. 

DeepSpark consists of three 15-layer convolutional neural networks on a 12,000-node Spark cluster using 1.2 PB of memory. The first network, the analytical network, is trained using a data set constructed from historical PRs against Spark, with a goal of training the network to identify the problem solved by a PR. 

Then, the second network, the generative network, is trained using selected code examples from StackOverflow tagged with the apache-spark label, designed to produce constructive comments and code segments which were helpful in solving the poster’s problem. Because this network generates human-readable responses, this network has a number of input features regarding discriminatory language to prevent it from making unsavory comments (as other AIs have been plagued by this issue). 

The final network, the evaluative network, is trained to identify whether a change is helpful and effective or not, also using past Spark pull requests as a training set, with a goal of predicting the probability of a particular change of being merged into Spark.

By using these three networks in synchronicity, DeepSpark is able to effectively review PRs by determining what problem they are solving, evaluating whether or not the PR solves this problem, and offering suggestions if there are sections of the PR which are not correct or don’t meet Spark standards for quality. If DeepSpark cannot identify any errors or issues with a PR with 95% certainty, it will LGTM, and if it finds that this rate dips below 60%, the PR is immediately closed. This way, DeepSpark has decreased the average time to response for a PR from 5 days to 40 seconds, while also reducing the time committers spend in this area considerably.



### PySpark

Apache spark and pyspark in particular are fantastically powerful frameworks for large scale data processing and analytics. In the past I’ve written about flink’s python api a couple of times, but my day-to-day work is in pyspark, not flink. With any data processing pipeline, thorough testing is critical to ensuring veracity of the end-result, so along the way I’ve learned a few rules of thumb and build some tooling for testing pyspark projects.



## 5.0 Final Words


### 5.1 Resources

[]() <br>
[]()
