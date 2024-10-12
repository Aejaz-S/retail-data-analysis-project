# retail-data-analysis-project
retail-data-analysis project
To computing various Key Performance Indicators (KPIs) for an e-commerce company, RetailCorp Inc. You have been provided real-time sales data of the company across the globe. The data contains information related to the invoices of orders placed by customers all around the world.
At the industry level, an end-to-end data pipeline is built for this purpose. Tools such as HDFS(Hadoop Distributed File System) are used to store the data that is processed by the real-time processing framework and then shown on a dashboard with tools such as Tableau and PowerBI. The image given below is an example of such a complete data pipeline.
Tasks:
Reading the sales data from the Kafka server
Preprocessing the data to calculate additional derived columns such as total_cost etc
Calculating the time-based KPIs and time and country-based KPIs
Storing the KPIs (both time-based and time- and country-based) for a 10-minute interval into separate JSON files for further analysis
Data Dictionary:
Invoice number: Identifier of the invoice
Country: Country where the order is placed
Timestamp: Time at which the order is placed
Type: Whether this is a new order or a return order
SKU (Stock Keeping Unit): Identifier of the product being ordered
Title: Name of the product is ordered
Unit price: Price of a single unit of the product
Quantity: Quantity of the product being ordered
Command to run the script:
export SPARK_KAFKA_VERSION=0.10
spark-submit --packages org.apache.spark:spark-sql-kafka-0-10_2.11:2.4.5 script.py
