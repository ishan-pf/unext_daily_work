# unext_daily_work

Day 1

Data - factual information 
Database - collection of data in the form tables or key or pair
types of data - structured, semi structured and unstructured
Keys - primary key, foreign key, composite key, candidate key, unqiue key
primary key - unique and not null
foreign key - should be a primary key from other table
E-R diagram - graphical representation of entites
Normalization 
1 NF - atomic values
2 NF - 1NF , no partial dependency 
3 NF - 2NF , no transitive dependency, no dependency b/w non key attribute and non key attribute
BCNF - 3NF , no functional dependency
Denormalization
Case Study on E-R diagram
Case Study on normalization
Dimensional and Snowflake modelling
Slowly Changing Dimension 

Day -2 

Creating a virtual Machine
batch processing
stream processing
4 V's - velocity , veracity , variety , volume
Data warehouse - structured data , fixed schema, ACID properties
Data Lake - structured , semi structured and unstructured data
Data lakehouse
Cloud Computing
 - private 
 - public 
 - hybrid
 - community
capital Expenditure
Operational Expenditure
Azure fundamentals


Day - 3 

three types of resources - sql Databases , SQL Managed Instance, SQL virtual machines
SQL Database - single Database, elastic pool ( The databases in an elastic pool are on a single server and share a set number of resources at a set price. Elastic pools in SQL Database enable software as a service (SaaS) developers to optimize the price performance for a group of databases within a prescribed budget while delivering performance elasticity for each database.)
configuring a azure sql server and database
connected to azure sql database
ddl statments - create , show
dml statements - 
dcl statements
a database can have two tables with same name if they have difference schems and you can
access them using their respective scheme identifier 
constraints
truncate table
drop table
delete table
creating library Database
grouping data - group by
having clause
we have to drop the constraint before we could drop the column in case of foreign key

Day 3 

Creating a elastic pool
sql joins - A JOIN clause is used to combine rows from two or more tables, based on a related column between them.
 	   1.Inner Join - The INNER JOIN keyword selects records that have matching values in both tables
           2.Left Join - The LEFT JOIN keyword returns all records from the left table (table1), and the matching 			records from the right table (table2). The result is 0 records from the right side, if 				there is no match.
			Note: In some databases LEFT JOIN is called LEFT OUTER JOIN.
	   3.		
stored procedure - 
	A stored procedure is a prepared SQL code that you can save, so the code can be reused over and over 	again.
	So if you have an SQL query that you write over and over again, save it as a stored procedure, and then 	just call it to execute it.

views -  A view is a virtual table based on the result-set of an SQL statement.

	A view contains rows and columns, just like a real table. The fields in a view are fields from one or more 	real tables in the database.

functions - 1.scalar gives only one unit of output - scalar function takes one or more parameters and returns a single value.
	    2.table valued gives the normal output	
temporary tables -  Temporary Tables are Created in TempDB and are automatically deleted as soon as the last 			     connection is terminated

 - We Should not create physical tables in stored procedure

- Subquery is executed first
 
- join three tables

Union - 1. The UNION operator is used to combine the result-set of two or more SELECT statements.
	2. The UNION operator selects only distinct values by default. To allow duplicate values, use UNION ALL
	3. Every SELECT statement within UNION must have the same number of columns
	4. The columns must also have similar data types
  	5. The columns in every SELECT statement must also be in the same order
Indexing


Day 4

- Resouce Group is a logical container

- With a premium performance selected , the latency will be low. Read and write operations will be frequent
Based on the requirement
1. Block Blobs.
2. File shares
3. page Blobs

- By Default , azure storage accounts make me 3 copies of the data

- Local Redundant means data stored in the same data center

- Zone Redundant has a protection against data center level failure. Data is getting in different
zones

- Geo Redundant intermediate option with failover capabilites in a secondary region

- Geo zone Redundant - local Redundant in primary and secondary region. Both Read and write Operation will be performed on the primary and secondary region

- Read Acces Geo Redundant - Local Redundant in primary and secondary region however the user will access 
the secondary region. Write operation in Primary and Read operation in secondary. The Latency will be significantly low and performance would be higher than the geo zone redundant

- 6 copies in GZRS/GRS - 3 in primary and 3 in secondary

- Region Pair

- SLA ( service level agreement) - it is the availibility and durability 

- GA ( General Availibility )

- upstream is someone who is going to provide u the data
 
- downstream is whom we provide the data

- cross-tenant replication - Allow object replication to copy blobs to a destination account on a different Azure Active Directory (Azure AD) tenant. Not enabling cross-tenant replication will limit object replication within the same Azure AD tenant.

- Acess Tier - Hot - frequently and day to day usage scenarios
	       Cold - INfrequently accessed data and backup scenarios


- Tags are used to visually segrigating the data 

- file shares , blobs

- Ingress - pushing data into azure

- engress - downloading data from azure

data engineer -> data architect

Day 5

-Azure Data factory

- SAS(shared access signature) - time bounded
 access key - lifetime

- A shared access signature (SAS) is a URI that grants restricted access rights to Azure Storage resources.

- if the frontend requires the access, it needs the connection string

- if the azure resouces wants the access , it needs the blob service SAS URI

- Azure Key Vault is a cloud service that provides a secure storage and management system for secrets such as API keys, passwords, certificates, and cryptographic keys

- ADF - data orchestration or data flow activity

- Pipelines - when it has one or more activites

- integration runtime - a gateway or bridge which enables communication

- azure auto resolve - its for the azure resources

- Self hosted integration runtime - when the server is local instead of the cloud

- Sql service integration system (SSIS) - if there is a existing ssis package in the server, then we go for the
SSIS.

- if the source and destination are in cloud however inside a virtual network , then we use Self hosted instegration runtime

- if the source and destination are in cloud however using a ssis package , then we use azure ssis IR

- pipeline space

- pipeline level parameter and dataset level parameter

Day 6

- We can only append values to array type variable

- On activity completion we have four options - On success, On Fail, On Skip and On Completion

- System Variables 

- Triggers cause a function to run. A trigger defines how a function is invoked and a function must have exactly
  one trigger.

- Linked Service , Datasets

- Parameters - pipeline and dataset level

- get MetaData activity and Copy Data activity

- If Activity - control flow

- Dynamic Content

Day 7

- Data transformation using Data flow

- Relationship between different files

- Databricks works on the principle of spark engine for the data tansformation

- 

Day 8 

- we have a db and muliple tables,

- Schema Drift

Day 9

- Azure Synapse is an enterprise analytics service that accelerates time to insight across data warehouses and big      
data systems. Azure Synapse brings together the best of SQL technologies used in enterprise data warehousing, Spark technologies used for big data, Data Explorer for log and time series analytics, Pipelines for data integration and ETL/ELT, and deep integration with other Azure services such as Power BI, CosmosDB, and AzureML.

- Synapse always need a storage acc

- All the data wil be stored on the storage acc and it should be gen2 

- if we make a synapse service, it will automatically ask us to create a gen2 storage accc

- on develop we can make notebooks

 - integrate IR , pipelines

- each and everything needs a different computing unit

- serverless and dedicated sql pool

- serverless fully managed by azure or anyother service provider. Dont have to worry about maintence

- serverless - table not supported

- The main difference between dedicated VM and serverless option is that 
- dedicated VMs provide a fixed amount of resources that are allocated to the VM, 
- while serverless options provide resources on demand and scale automatically based on usage

- data integration unit(DIU) using this Data warehouse calculates the cost

- Openrowset is a function used to read the file

- OPENROWSET is a T-SQL function that allows for reading data from many sources including using the SQL Server's BULK import capability

- we can create the database inside using code or UI.

- UTF - collate is used to enable some special characters
 create db1 collate Latin1_general_100_BIN2_UTF8

- Common table expression

- CTE cant run alone

- When we want to visualize the data we go for serverless, as using dedicated service will be cost ineffective 
and cant be running 24/7.

- how hash helps change data capture - when

- based on the hash value , the data gets distributed on the compute node. thats when its called hash distributed

- clustered columnstore, clustered index , heap

- 

Day 9

- Power Query Editor Tx

- DAX measures

- DAX calculated columns

- Filters ( Visual, Page, All Page)

- Slicer

- RLS ( manage roles)

- Beautification

- Parameter for our sources




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




