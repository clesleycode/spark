Intro to Apache Spark
==================

Brought to you by [Lesley Cordero](http://www.columbia.edu/~lc2958).

## Table of Contents

- [0.0 Setup](#00-setup)
	+ [0.1 R and R Studio](#01-r-and-r-studio)
	+ [0.2 Packages](#02-packages)
- [1.0 Background](#10-background)
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

Spark is a low-level system for distributed computation on clusters, capable of doing in-memory caching between stages, improving the performance. This is in contrast to Hadoop, which instead writes everything to disk. Spark is also a much more flexible system in that it's not only constrained to MapReduce. 

Now, it might seem as though Spark is a replacement for Hadoop; and though it sometimes is used as a replacement, it can also be used to complement Hadoop's functionality. By running Spark on top of a Hadoop cluster, you can still leverage HDFS and YARN and then have Spark replace MapReduce. 


## REPLs

Spark is composed of a built-in Read-Evaluate-Print-Loop in the form of a shell that can be used for interactive analysis. You can begin by entering the following into your terminal:

``` bash
$SPARK_HOME/bin/pyspark
```

Next, you can run the following in Python:

``` python
import pyspark
sc = pyspark.SparkContext("local[*]", "demo")
```

Note that Spark only allows one Spark Context to be active at a time, so you'll need to stop the current spark context before starting a new one.

If this doesn't work, make sure the PYTHONPATH contains the module:

``` bash
export PYTHONPATH=$SPARK_HOME/python:$SPARK_HOME/python/lib/:$PYTHONPATH
```

Now in R, the process is very similar:

``` R
library(SparkR, 
        lib.loc = c(file.path(Sys.getenv("SPARK_HOME"), "R", "lib")))
sparkR.session(master = "local[*]", 
               sparkConfig = list(spark.driver.memory = "2g"))
```

## 5.0 Final Words


### 5.1 Resources

[Apache Spark](http://spark.apache.org/) <br>
[Spark Github](https://github.com/apache/spark)
