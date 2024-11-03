# worldclim-pandas-spark

## Benchmarking Climate Data Loading and Querying with Pandas and Spark
This project aims to benchmark the loading and querying of climate data from WorldClim using Pandas and Apache Spark for data processing at different spatial resolutions.

## Context
WorldClim provides global climate data at various spatial resolutions. In this project, precipitation data at resolutions of 10m, 5m, and 2.5m were utilized. The analysis compares the performance and scalability between Pandas DataFrame (non-distributed processing) and Spark DataFrame (distributed processing) in loading the dataset and executing queries.

## Features
* **Data Download and Conversion**: WorldClim data was downloaded in raster format and converted to CSV files using the raster2xyz tool.
* **Loading Benchmark**: The loading time of the data was evaluated using both Pandas and Spark DataFrames.
* **Query Benchmark**: The execution time of simple queries on the loaded data was assessed using both Pandas and Spark DataFrames.
* **Export to Parquet**: The data was exported to Parquet format to test a columnar storage format.

## Results
The benchmark results clearly indicate the superiority of distributed processing over non-distributed processing in terms of performance and scalability for querying large datasets, whether climatic or otherwise. The choice of the Parquet storage format, with its columnar storage, also significantly contributed to the efficiency of the queries. These conclusions highlight the importance of distributed processing and appropriate storage in large-scale data analysis.