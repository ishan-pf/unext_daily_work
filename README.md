# unext_daily_work



* creating elastic pool in Azure SQL
* Subqueries
* Self join, Cross Join
* stored procedures
* Views
* Functions
	- Scalar Functions
	- Table valued Functions
* temp tables
* Union, intersection, Union All
* indexing

pySpark

- why Spark - distributed computing and parallel processing
- pySpark is like an api between python and spark engine
-Driver and worker
- in order to allow every executor to perform work in parallel, spark breaks up the day into chunks
  called partitions

Lazy evaluation
	- Unless we are performing an action , data transformation won't start executing
	- For example - maindf = pd.read_csv('')
	-  testdf = maindf('revenue' * 100) //data manipulation 
	-  testdf.show() //after we run this action, then only data transformation will take place
	- Testdf.write('driver
	- For every action , the driver creates a job for worker
	
Types of Transformation
	- Narrow and wide
	- Based on shuffling ,No. of jobs are created
	-  Spark uses a master-slave architecture
	- It has one central coordinator ( Driver ) that communicates
	With many distributed workers( Executors)
	- The Driver is the process where the main method runs
	- First it converts the user program into tasks and after that it schedules the tasks on the executors
	Executors
	- They are worker nodes processes in charge of running individual tasks in a given Spark Jon.
	- They are launched at the beginning of a spark application and typically run for the entire lifetime of an application. Once they have run the task they send the results to the driver. They also provide in-memory storage for RDDs that are cached by users programs through block manager.

	1. A standalone application starts and instantiates a SparkContext instance (and it is only then when you can call the application a driver).
	2. The driver program ask for resources to the cluster manager to launch executors.
	3. The cluster manager launches executors.
	4. The driver process runs through the user application. Depending on the actions and transformations over RDDs task are sent to executors.
	5. Executors run the tasks and save the results.
	6. If any worker crashes, its tasks will be sent to different executors to be processed again. In the book "Learning Spark: Lightning-Fast Big Data Analysis" they talk about Spark and Fault Tolerance:
	7. With SparkContext.stop() from the driver or if the main method exits/crashes all the executors will be terminated and the cluster resources will be released by the cluster manager.
- 
	-  A stage is a physical unit of execution
	- It is a set of parallel tasks — one task per partition. In other words, each job gets divided into smaller sets of tasks, is what you call stages.
	- Resilient Distributed Datasets (RDD) is a fundamental data structure of Spark. It is an immutable distributed collection of objects. Each dataset in RDD is divided into logical partitions, which may be computed on different nodes of the cluster.
	

	When a Action is called against a Data, The spark engine will perform the below steps,

Deployment Types 
	- Client Mode
	- Cluster Mode

27 sep 

Features of delta table
-    Time traveling in delta table

Vacuum my files 

Default - delta and parquet

Delta supports deletion
Parquet does not support deletion
	
Single source of truth - data should be at one place ( container/one storage acc)

Medallion / multi hop architecture

Rollback on delta

%sql
Select * from e_zip_tbl version as of 0

Raw/bronze - sql , oracle, storage, azure single source of truth

![image](https://github.com/ishan-pf/unext_daily_work/assets/55364798/1824bdf4-5b52-4c32-9408-17c2ec16c168)

12 SEP 2023

Azure Synapse analytics
SQL Pools
Serverless
Dedicated Pools
Collate in SQL
Common Table Expression
Global Temporary table
Data distribution
Replicated
Round-Robin
Hash Distributed
Indexing
Notebooks
![image](https://github.com/ishan-pf/unext_daily_work/assets/55364798/aa8da7f3-07ee-46f8-a47b-3b5c02d8b66e)

13 sep 2023

PowerBI Desktop
Power Query
Loading in data
Reports
Dashboards
Parameters in PowerBI
Filtration
Visual level
Report level
Page level
Calculated columns and measures
DAX – Data analytics expression
RBAC
![image](https://github.com/ishan-pf/unext_daily_work/assets/55364798/74aa6186-c055-41cc-8f30-98bae69e9446)

14 sep 2023

Loading csv files in PowerBI
Relationship between entities
Univariant, Bivariant, multivariant
Hands on activities
Parameter
Power query editor
DAX
Filters
Slicer
Tables
Beautification
Connecting to SQL Management server
![image](https://github.com/ishan-pf/unext_daily_work/assets/55364798/f03bf30e-9336-4026-afe2-cb74e34e6d71)

15 sep 2023

Case study – PowerBI
Introduction to python
Integer
Float
String
Boolean
List
Tuple
Dictionary
Operators
![image](https://github.com/ishan-pf/unext_daily_work/assets/55364798/51b86b4c-2782-444e-8d08-4cb192231c7c)




