# AzureDevDocs
# CosmosDB - recap
CosmosDB is the Microsoft offering of a non-SQL database. These databases are non-relational, meaning that there are no relationships between data points, such as unique primary key identifiers. CosmosDB allows for backups across the world, with a multitude of options for data retention, allowing you to customise how fast the data is replicated, and whether this data is stored in a specific order.
The languages that are supported within CosmosDB are:

 - SQL
 - MongoDB
 - Table
 - Cassandra
 - Gremlin (Graph-based Databases)

# Azure Free Tier offering
As part of the Azure Free Tier, you get the following benefits for free: 

 - 1000 Request units per second
 - 25GB storage
 For testing, this is super handy as you are unlikely to ever hit the maximum request units per second. However, you are unable to retain data in multiple locations using the free tier, reserved exclusively for paid tiers only. Bare this in mind if the data you want to use needs geographic redundancy or not.
# CosmosDB - Data consistency
As part of CosmosDB data redundancy, you can choose how your data is kept. The most consistent offerings are the most expensive, with little to no consistency being much cheaper.
Here is a breakdown of each of the tiers available:
 - Boundless/Stateless - A tolerable delay in data replication in other regions. The data may be inconsistent for a small amount of time. This is the default setting.
 - Consistent - The data will be stored in the exact order, but it takes some time before the data will appear.
 - Eventual - This option will sort the data in time, but the data will be out of order for a long time. 
 - Strong - Most consistent (and most expensive!) - All of the data is written into all of the instances at the same time, meaning that data will automatically be in the correct location immediately.
 # CosmosDB - Containers
 You are able to create containers within your databases. These containers can split the main database data into sections to make it much easier to read. This data could be shown as a graph, a table, or a collection. 
 Alternatively, containers can also contain code to sort the data, triggers based on how much data there is, or inform you about conflicts.
 # CosmosDB - Partitions
 Within CosmosDB, there are partitions, both physical and logical. Physical partitions are autoscaled, which has a limit of 50GB and 10,000 Request Units per Second. Logical units use the same partition key, but still gives a unique item ID.
 # CosmosDB - Methods of payment
 While the Azure Fundamentals exam covers payment and billing in general, the AZ-204 exam will need you to know which payment method is best for certain situations.
 If you have predictable workloads, you can provision a certain amount of Request Units per Second.
 If your workloads are not predictable, such as spiking at certain points, then pay as you go/Serverless is the best option. It is built for low or no traffic loads, as well as inconsistent workloads.
# CosmosDB - Programming
You can write programs within CosmosDB. These programs can be incorporated into the aformentioned containers.
All of these scripts can be executed using the Azure portal, Javascript integrated queries, or CosmosDB SQL Client SDKS.
All transactions within CosmosDB are ATOMIC - meaning they are not final unless the transaction has been fully completed. 
Performance can vary, but mostly runs on bulk data operations. 
# How-to: Azure GUI browser

# How-to: Azure CLI/Cloud Shell 

 

