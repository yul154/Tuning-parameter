# The Big Data Problem
> a single machine can no longer process or even store all the data
* distribute data over large clusters

##  Hardware for Big Data
* problem with cheap haradware
1. failures
2. network speeds
3. uneven performance

## distributing work
* how do we split work across machines: use a hash table
* deal with failure or slow tasks: launch another task, kill the original task
* Map reduce:iterative jobs involve a lot o disk i/o for each repetition
  1. mapper: read data from hard drive, process it and then write it out to disk
  2. reducer: read data from disk, process it, write the results out to disk
  *  I/O operation on disk are very slow

## Spark
### Basick conception
> new distributed execution engine
* keep more data in-memory(use memory instead of disk)
* one more step: read data from disk to memory
* Resilient distributed datasets(RDDs): 
  * write program in terms of opertaions on distributed datasets
  * RDDs built and manipulate throught a diverse set o parallel transformations an actions
  * RDDS automatically rebuild on machine failure
  * RDDS includes partitions collections of objects 
* MapReduce in Spark
  * storage: in-memory or on disk
  * support opertaions more than map and reduce(hadoop)
  * execution model: batch, interactive, streaming
  * Programming:Scala, Java(Hadoop),R and Python
  
### Spark with Big data
* pySpark: Python programming interface
* Spark program:
  1. consists of two programs: a driver program(driver machine) and workers programs(clusters nodes)
  2. Spark context: tell Spark how and where to access a cluster
  3. pySpark shell and Databricks Cloud automatically create sc variable
  4. use SparkContext to create RDDs
* master parameter for a Spark context
  1. determine type(local, remote) an size of cluster to use
  2. `local`: run Spark locally with one worker thread
  3. `local[k]`:  run Spark locally with k worker thread
  4. `spark://HOST:PORT`: connect to a Spark standalone cluster
* RRDs
  * immutable once constructed
  * track lineage information to efficiently recompute lost data
  * operations on collection of elements in parallel
  * need to specifies number of partitions for an RDD
  * Types of operations: transformations(executed when action run on it) and actions
* Transformations: create new datasets from an existing one
  * lazy evaluation: creating a recipt for creating result
  * Transfotmations code runs at driver, action codes runs at workers
  



