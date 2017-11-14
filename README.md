## DATA622 HW #5
- Assigned on October 25, 2017
- Due on November 15, 2017 11:59 PM EST
- 15 points possible, worth 15% of your final grade

### Instructions:

Read the following:
- [Apache Spark Python 101](https://www.datacamp.com/community/tutorials/apache-spark-python)
- [Apache Spark for Machine Learning](https://www.datacamp.com/community/tutorials/apache-spark-tutorial-machine-learning)

Optional Readings:
- [Paper on RDD](https://www.usenix.org/system/files/conference/nsdi12/nsdi12-final138.pdf)
- [Advanced Analytics with Spark: Patterns for Learning from Data at Scale, 2nd Edition](https://www.amazon.com/_/dp/1491972955), Chapters 1 - 2

Additional Resources:
- [Good intro resource on PySpark](https://annefou.github.io/pyspark/slides/spark/#1)
- [Spark The Definitive Guide](https://github.com/databricks/Spark-The-Definitive-Guide)
- [Google Cloud Dataproc, Spark on GCP](https://codelabs.developers.google.com/codelabs/cloud-dataproc-starter/)


### Critical Thinking (8 points total)

1. (2 points) How is the current Spark's framework different from MapReduce?  What are the tradeoffs of better performance speed in Spark?
Spark was purposely designed to support in-memory processing and allows applications to be written in Java, Python or Scala and to build parallel applications designed to take full and fast advantage of a distributed environment. Unlike MapReduce, Spark is designed for advanced, real-time analytics and has the framework and tools to deliver when shorter time-to-insight is critical. Included in Spark’s integrated framework are the Machine Learning Library (MLlib), the graph engine GraphX, the Spark Streaming analytics engine, and the real-time analytics tool, Shark. One tradeoff of better performance speed in Spark is costs as keeping data in-memory is quite expensive and the memory consumption is very high.

2. (2 points) Explain the difference between Spark RDD and Spark DataFrame/Datasets.
Since inception, RDD was the primary user-facing API in Spark and is an immutable distributed collection of elements of data, partitioned across nodes in a cluster that can be operated in parallel with an API. Like an RDD, a DataFrame is an immutable distributed collection of data but it differs because the data are organized into named columns like a table in a relational database. We can consider DataFrame as an alias for a collection of generic objects Dataset[Row], where a Row is a generic untyped JVM object. Dataset, by contrast, is a collection of strongly-typed JVM objects, dictated by a case class you define in Scala or a class in Java.

3. (1 point) Explain the difference between SparkML and Mahout.
Mahout is built on top of MapReduce therefore constrained by disk accesses, making it slower and not able to handle iterative jobs very well. Machine Learning algorithms use many iterations, this makes Mahout run very slowly. In contrast, something like MlLib is built on top of Spark, making it much faster than Mahout. SparkML provides users with a toolset to create pipelines of different machine learning related transformations on data.

4. (1 point) Explain the difference between Spark.mllib and Spark.ml.
Spark.mllib contains the original API built on top of RDDs and Spark.ml provides higher-level API built on top of DataFrames for constructing ML pipelines. Using Spark.ml is recommended because with DataFrames the API is more versatile and flexible.

4. (2 points) Explain the tradeoffs between using Scala vs PySpark.
Scala is significantly faster than PySpark performance-wise. PySpark is easier to learn because of its syntax and standard libraries. Scala supports powerful concurrency while PySpark does not support true multithreading. Scala is a more verbose language compared to PySpark. PySpark offers several libraries for Machine Learning and Natural Language Processing compared with Scala which lacks good visualization and local data trasnformations.

### Applied (7 points total)

Submit your Jupyter Notebook from following along with the code along in [Apache Spark for Machine Learning](https://www.datacamp.com/community/tutorials/apache-spark-tutorial-machine-learning)
