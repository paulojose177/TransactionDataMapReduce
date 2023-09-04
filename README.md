# Transaction Data MapReduce with PySpark

## Description

This repository contains a PySpark script designed to perform MapReduce operations on a dataset of transactions. The script reads data from a CSV file, categorizes transactions, performs a count on each category, and then outputs the result.

## Prerequisites

- Python
- PySpark
- Hadoop (WinUtils for Windows)

## How to Run

1. **Set Up Environment Variables**: Ensure you have the following environment variables set. Update the paths to match your local setup.

    ```python
    os.environ["HADOOP_HOME"] = "path_to_WinUtils"
    os.environ["PYSPARK_PYTHON"] = "python.exe"
    os.environ["PATH"] = os.getenv("path") + ";" + os.getenv("HADOOP_HOME") + "\\bin"
    ```

2. **Run Script**: Open the Jupyter notebook and execute the cells.

3. **Data Input**: Place your `.csv` transaction dataset in the appropriate directory and update the path in the script. The script currently expects the dataset path to be in the following section of the code where: `"your_file_path_here.csv"` is:

    ```python
    data = spark.read.option("Header", True).option("InferSchema", True).csv("your_file_path_here")
    ```

4. **Check Output**: After successful execution, the output will be saved in a CSV file named `Output_TransactionMapReduceInfo.csv`.

## Features

- Data ingestion from a CSV file.
- Mapping and reducing to count transaction categories.
- Sorting and outputting the results.
  
## Dependencies

Install the required dependencies using the following command:

```bash
pip install -r requirements.txt
