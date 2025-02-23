# Generating Explain for a Single Query

## Overview
This README provides instructions specific to setting up and using the EXPLAIN tool within the `explain/single-query` subdirectory of the `db2-labs` repository.

For general Python environment setup and VS Code configuration steps, please refer to the [top-level README](../../README.md) in the main `db2-labs` directory.

## Running the EXPLAIN Tool

### 1. Open the Terminal in VS Code
You can open a terminal in two ways:
- **Option A:** Open the terminal window directly after launching VS Code and navigate to the `explain/single-query` folder:
  ```sh
  cd explain/single-query
  ```
- **Option B:** From the **Explorer** panel on the left, right-click on the `explain/single-query` folder and choose **Open in Integrated Terminal**.

### 2. Configure the Database Connection
In the terminal, type:

```sh
vi .env
```

This will open a configuration file for your database settings. Add the following details:

```
database=<your-database-name>
hostname=<your-database-host>
port=<database-port>
protocol=<database-protocol>
uid=<your-username>
pwd=<your-password>
```

Replace the placeholders with your actual database connection information. Save and exit the file:
- Press **Esc**
- Type `:wq` and press **Enter**

### 3. Running Queries in the Notebook
1. Open the `explain-single-query.ipynb` notebook in VS Code.
2. Select **Kernel** → **Change Kernel** and choose the interpreter from the virtual environment configured at the top level (refer to the [top-level README](../README.md) for details).
3. Update the query section with the SQL query you want to analyze.

### 4. Execute the Notebook
Run the cells in the notebook to gather EXPLAIN details for the specified SQL query. The notebook will generate insights based on the query plan.

---

For any additional setup or configuration steps, please refer back to the [top-level README](../README.md).
