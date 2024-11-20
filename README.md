# Overview of the Script:

This script automates the creation of Delta Tables in Databricks. It allows users to define the structure of a Delta table by specifying:

- **Column Names**: The list of columns to be included in the table.
- **Schema List**: The corresponding data types for each column.
- **Nullable List**: Specifies whether each column is nullable (optional).
- **Table Name**: The name of the Delta table to be created.
- **Storage Path**: The location (storage path) where the Delta table will be stored.
- **Partition List**: Specifies the columns to partition the table by (optional).

The script then generates an appropriate SQL or PySpark query to create the Delta table based on the provided inputs.

- **SQL Output**: A `CREATE TABLE` statement with column definitions, partitioning (if applicable), and Delta-specific optimizations.
- **PySpark Output**: A PySpark-based API call to create the Delta table using `DeltaTable.createIfNotExists()` with column definitions, nullable properties, and partitioning.

This automation helps streamline Delta table creation, especially when dealing with large datasets or complex table structures.
