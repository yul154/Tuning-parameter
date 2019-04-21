#  Data Structure
1. Structured: relational database, formatted messages
2. Semi-Structured: Documents, XML, JSON
3. Unstructured: Plain Text, Media
## semi-structured
* file:sequece of bytes
* tabular:a table which a collection of rows an columns
  1. format no well-defined
  2. types may be incorrectly inferred
* In pySpark
  * DataFrames
<img width="513" alt="Screen Shot 2019-04-21 at 12 22 47 PM" src="https://user-images.githubusercontent.com/27160394/56472729-4b892e00-6430-11e9-94d6-89cffb15243b.png">
## log file
* Binary file I/O performance is typically much better (faster) than text file I/O performance
* The time to read a compressed file is more litte than the time to write a compressed file

## Structured Data
* SQL supported by pySpark DataFrames
* JOIN IN spark
  1. SparkSQL and Spark DataFrame `join()`
  2. Pair RDDs: `x.join(y):`