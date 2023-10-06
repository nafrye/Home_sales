# Home_sales
This respository contains a file that examines home sales data. Data are read into a temporary table. 

Runtime is compared for queries run on the temporary table, a cached version of the temporary table, and a partitioned table (using parquet). Runtime is fastest using the cached table. Partioning may not have reduced runtime because:
1. Analyses required data from each partition to be recombined
2. The data were not that large
