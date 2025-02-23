# Db2 Labs

## Overview
Welcome to the `db2-labs` repository. This project serves as a collection of scripts and code snippets for using various Db2 tools. As I explore and find useful tools, I will share them here.

Some of the tools require Python, so this README provides the necessary steps to set up the Python environment for running the Db2 scripts.

## Python Environment Setup
This project uses **Python 3.12**. Ensure you have a compatible Python version installed before proceeding.

### 1. Create a Virtual Environment
To create a virtual environment (`.venv`) at the top level of the project:

```sh
python3.12 -m venv .venv
```

### 2. Activate the Virtual Environment
On Linux:
```sh
source .venv/bin/activate
```

### 3. Install Dependencies
Use the `requirements.txt` file to install all necessary dependencies:

```sh
pip install -r requirements.txt
```

### 4. Set the Virtual Environment in VS Code
If you are using VS Code, follow these steps to set `.venv` as the Python interpreter:

1. Open VS Code and load the `db2-labs` folder.
2. Press **Cmd + Shift + P** to open the command palette.
3. Search for **Python: Select Interpreter** and choose `.venv` from the list.
4. If the environment does not appear, click **Enter interpreter path** → **Find** and navigate to `.venv/bin/python3.12`.

### 5. Running Jupyter Notebooks
If you are working with Jupyter notebooks in VS Code:

1. Open the `db2-labs` folder in VS Code.
2. Navigate to the `explain/` directory.
3. Open `explain-single-query.ipynb`.
4. Select **Kernel** → **Change Kernel** and choose the interpreter from `.venv`.

Now, your environment is ready to execute the scripts and notebooks within the `db2-labs` repository.

---

As I add more tools and scripts, I will update this repository with instructions on how to use them effectively.

