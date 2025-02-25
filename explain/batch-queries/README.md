Here's the updated `README.md` for your repository, tailored specifically for Linux users:

---

# Batch Query Execution and Explain Plan Collection for Db2

This repository provides a batch version of the **Explain Notebook**, enabling the execution of multiple SQL queries against a Db2 database and the collection of their corresponding **EXPLAIN** plans. Each query is processed to remove schema references, executed against the default schema, and the resulting explain data is stored in organized output directories.

## 📋 Features

-Execute multiple SQL queries in batch mode
-Automatically remove schema references to run queries against the default schema
-Export explain tables and actual execution statistics
-Save outputs in timestamped subfolders for each query
-Support non-interactive batch execution using **Papermill**

## 🚀 Getting Started (Linux)

### 1. Clone the Repository

```bas
git clone https://github.com/shaikhq/db2-labs.git
cd db2-labs/explain/batch-queris
``


### 2. Prepare Your Environment

Ensure you have Python installed. Create and activate a virtual environment named `.venv`:

```bas
python3 -m venv .venv
source .venv/bin/activae
``

Install the required dependencies. Since the `requirements.txt` file is located in the top-level project directory, provide the relative path to i

```bas
pip install -r ../../requirements.tt
``


### 3. Prepare Your Queries
Create a `queries.sql` file in the `batch-queries` directory. List each SQL query on a separate lin

```sq
-- queries.sql
SELECT * FROM table1;
SELECT column1, column2 FROM table2 WHERE condition;
-- Add more queries as needd
``


### 4. Execute the Batch Notebook
Run the batch notebook using **Papermill*

```bas
papermill explain_batch_notebook.ipynb output_notebook.ipyb
``

This command executes the `explain_batch_notebook.ipynb` with the provided queries and outputs the results to `output_notebook.ipynb

### 5. Review the Outputs
After execution, the explain plans and related outputs are saved in the `output` directory. Each query's results are stored in a subfolder named with the query's execution timestam

## ⚙️ Customization
To run queries against schemas other than the default, modify the notebook's code to retain or specify the desired schema reference

## 🛠️ Non-Interactive Executio

For non-interactive mode, activate the virtual environment and execute the notebook using Papermi:

```bah
source .venv/bin/activate
papermill explain_batch_notebook.ipynb output_notebook.ipnb
``


This allows the notebook to run in the background, processing all queries in the `queries.sql` fi.

--

By following these steps, you can efficiently execute a batch of SQL queries against a Db2 database and collect their explain plans for analys. 