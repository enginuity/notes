Shared variables: 
-> broadcast -> cache the value in all nodes
-> accumulators -> these can be used for logging for job progress

RDDs: Resilient distributed datasets
-> data is partitioned here

Transformations: Create a new data set
Actions: Return a value

lazy eval -> evaluate only when variables are needed
persist() will save a value 

Variables might not persist changes properly across machines -- use accumulators

printing RDD elements: 
* `collect`: brings data to main driver, then stick into `println`
* `take(x)`: Takes `x` values. 