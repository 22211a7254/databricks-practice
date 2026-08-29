# databricks-practice
# Databricks PySpark Practice

A beginner-friendly project to practice **Databricks, Apache Spark, and PySpark DataFrame operations**.

##  Project Overview

This project demonstrates basic data processing using PySpark in a Databricks notebook. A small sample dataset containing names, ages, and cities is created and converted into a Spark DataFrame.

The project performs basic operations such as:

* Creating a Spark DataFrame
* Displaying DataFrame data
* Filtering rows based on a condition
* Creating a new column using an existing column
* Practicing Git and Databricks integration

##  Technologies Used

* **Databricks**
* **Apache Spark**
* **PySpark**
* **Python**
* **Git & GitHub**
* **Jupyter Notebook (`.ipynb`)**

## 📂 Project Structure

```text
databricks-practice/
│
└── demo_notebook.ipynb
```

##  Sample Dataset

The project uses the following sample data:

| Name  | Age | City      |
| ----- | --: | --------- |
| Laxmi |  21 | Hyderabad |
| Ravi  |  25 | Bangalore |
| Anu   |  23 | Chennai   |
| Kiran |  28 | Mumbai    |

##  Operations Performed

### 1. Create DataFrame

The sample data is converted into a PySpark DataFrame using:

```python
df = spark.createDataFrame(data, columns)
```

### 2. Display Data

The DataFrame is displayed using:

```python
df.show()
```

### 3. Filter Data

People older than 23 are selected using:

```python
filtered_df = df.filter(df.Age > 23)
```

Output:

| Name  | Age | City      |
| ----- | --: | --------- |
| Ravi  |  25 | Bangalore |
| Kiran |  28 | Mumbai    |

### 4. Add a New Column

A new column showing the age after five years is created using:

```python
df2 = df.withColumn("Age_in_5_years", col("Age") + 5)
```

Example:

| Name  | Age | Age in 5 Years |
| ----- | --: | -------------: |
| Laxmi |  21 |             26 |
| Ravi  |  25 |             30 |
| Anu   |  23 |             28 |
| Kiran |  28 |             33 |

##  Learning Objectives

Through this project, I practiced:

* Working with Databricks notebooks
* Understanding Spark DataFrames
* Creating DataFrames using PySpark
* Filtering data using conditions
* Performing column transformations
* Using PySpark functions such as `col()`
* Managing notebooks using Git and GitHub

##  How to Run

1. Open the notebook in a Databricks workspace.
2. Attach the notebook to an available Databricks cluster.
3. Run the cells sequentially.
4. View the DataFrame outputs and transformations.

Alternatively, the notebook can be opened in a compatible Jupyter/PySpark environment with the required Spark configuration.

##  Future Improvements

This practice project can be extended by adding:

* CSV/JSON dataset ingestion
* Data cleaning and missing-value handling
* Duplicate removal
* GroupBy and aggregation operations
* Data joins
* Spark SQL queries
* Parquet/Delta Lake storage
* Basic ETL pipeline

## 👩‍💻 Author

**Laxmi Prasanna**

This repository is created for practicing **Databricks and PySpark data processing concepts**.
