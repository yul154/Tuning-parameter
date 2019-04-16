#  **Spark essentials**
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
  * lazy evaluation: the execution will not start until an action is triggered
  * Transfotmations code runs at driver, action codes runs at workers
<img width="481" alt="Screen Shot 2019-04-16 at 5 17 48 PM" src="https://user-images.githubusercontent.com/27160394/56244730-a525dd00-606b-11e9-8236-ad0f7e1c87e9.png">

* Actions
> Cause Spark to execute recipe to transform source
<img width="494" alt="Screen Shot 2019-04-16 at 5 22 00 PM" src="https://user-images.githubusercontent.com/27160394/56245014-5462b400-606c-11e9-8799-9b9142c2f802.png">
<img width="403" alt="Screen Shot 2019-04-16 at 5 30 07 PM" src="https://user-images.githubusercontent.com/27160394/56245407-5b3df680-606d-11e9-9c24-6fbbc60c9551.png">

* Programming model
  1. read data
  2. summ within partitions
  3. combine sums in driver
* Caching RDD: avoid reload data
  * `rdd.cache()`
* pySpark Closures
  * automatically for functions that run on RDDs at workers, and for any global variables that are used by those workers.
  * one closure sent for per work with every task
  * no communication between workers
  * any changes that you make to the global variables that are at the workers are not sent to the driver or to other workers.
* pySpark share variable
> what if we want to count events that occur during job execution?
  1. boradcast variables: cache a value in memory on all nodes，We can send it to the worker only once instead
of having to send it with each task
  2. accumulator(write only): only driver can read
  >  variables that could only be added to by an associative operation.

## Process of a Spark program
1. use the master parameter to specify the number of workers.
2. When you create an RDD, you can specify, the number of partitions for that RDD, and Spark will automatically create that RDD spread across the workers.
3. When you perform transformations and actions that use functions, Spark will automatically push a closure containing. that function to the workers so that it can run at the workers.






