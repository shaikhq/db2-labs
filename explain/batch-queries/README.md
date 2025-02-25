# Batch Query Execution and Explain Plan Collection for Db2

This repository provides a batch version of the Explain Notebook, enabling the execution of multiple SQL queries against a Db2 database and the collection of their corresponding EXPLAIN plans. Each query is processed to remove schema references, executed against the default schema, and the resulting explain data is stored in organized output directories.

📋 Features
Execute multiple SQL queries in batch mode.
Automatically remove schema references to run queries against the default schema.
Export explain tables and actual execution statistics.
Save outputs in timestamped subfolders for each query.
Support non-interactive batch execution using Papermill.

**This notebook needs to run on a Db2 server.**


🚀 Getting Started (Linux)
1. Clone the Repository

```shell
git clone https://github.com/shaikhq/db2-labs.git
cd db2-labs/explain/batch-queries
```

2. Prepare Your Environment
Ensure you have Python installed. Create and activate a virtual environment named .venv:
```shell
python3 -m venv .venv
source .venv/bin/activate
```
For general Python environment setup and VS Code configuration steps, please refer to the [top-level README](../../README.md) in the main `db2-labs` directory.

Install the required dependencies. Since the requirements.txt file is located in the top-level project directory, provide the relative path to it:

```shell
pip install -r ../../requirements.txt
```

3. Prepare Your Queries
Create a queries.sql file in the batch-queries directory. List each SQL query on a separate line:

```sql
-- queries.sql
SELECT * FROM table1;
SELECT column1, column2 FROM table2 WHERE condition;
-- Add more queries as needed
```

4. Execute the Batch Notebook
Run the batch notebook using Papermill:

```shell
papermill explain_batch_notebook.ipynb output_notebook.ipynb
```

This command executes the explain_batch_notebook.ipynb with the provided queries and outputs the results to output_notebook.ipynb.

5. Review the Outputs
After execution, the explain plans and related outputs are saved in the output directory. Each query's results are stored in a subfolder named with the query's execution timestamp.

⚙️ Customization
To run queries against schemas other than the default, modify the notebook's code to retain or specify the desired schema references.

🛠️ Non-Interactive Execution
For non-interactive mode, activate the virtual environment and execute the notebook using Papermill:

```shell
source .venv/bin/activate
papermill explain_batch_notebook.ipynb output_notebook.ipynb
```

This allows the notebook to run in the background, processing all queries in the queries.sql file.
