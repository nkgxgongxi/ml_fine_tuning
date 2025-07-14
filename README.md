# ML Fine Tuning Demo

This repository provides a hands-on demonstration of machine learning model fine-tuning using the classic Titanic dataset from Kaggle. The project includes examples for both local model training and a more advanced workflow using Snowflake Notebooks.

## repository Contents

*   `simple_lr_model.ipynb`: A Jupyter notebook demonstrating how to train and fine-tune a **Logistic Regression** model locally.
*   `simple_rf_model.ipynb`: A Jupyter notebook demonstrating how to train and fine-tune a **Random Forest** model locally.
*   `Titanic Model Tuning Demo.ipynb`: A notebook designed to be run within the **Snowflake Notebooks** environment for in-database model tuning.
*   `snowflake_access_control.sql`: A SQL script to guide users in setting up the necessary roles, users, database, and schema in Snowflake to run the demo.
*   `requirements.txt`: A list of Python packages required for the local execution demos.
*   `train.csv` & `test.csv`: The training and testing datasets sourced from the Kaggle Titanic competition.
*   `.gitignore`: Standard file to exclude certain files from Git tracking.

---

## Getting Started

You can run this project in two ways: locally on your own machine or directly within the Snowflake Data Cloud.

### Option 1: Local Model Training Demo

This option allows you to run the simple logistic regression and random forest models on your local machine.

#### Prerequisites
*   Python 3.x
*   Jupyter Notebook or JupyterLab

#### Steps
1.  **Clone the repository:**
    ```bash
    git clone https://github.com/nkgxgongxi/ml_fine_tuning.git
    cd ml_fine_tuning
    ```

2.  **Create a virtual environment (recommended) and install dependencies:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    pip install -r requirements.txt
    ```

3.  **Launch Jupyter and run the notebooks:**
    ```bash
    jupyter notebook
    ```
    From the Jupyter interface, open and run `simple_lr_model.ipynb` or `simple_rf_model.ipynb`.

---

### Option 2: Model Tuning in Snowflake

This option demonstrates how to perform model tuning directly within the Snowflake Data Cloud using Snowflake Notebooks.

#### Prerequisites
*   A Snowflake account with permissions to create users, roles, databases, and warehouses.

#### Steps
1.  **Set up Snowflake Environment:**
    *   Log in to your Snowflake account.
    *   Open a new worksheet and use the `snowflake_access_control.sql` script as a guide to create the necessary user, role, database, schema, and warehouse for this demo.

2.  **Load Data into Snowflake:**
    *   Upload `train.csv` and `test.csv` to a Snowflake internal stage. You can do this via the Snowsight UI or using the `PUT` command in SnowSQL.

3.  **Run the Snowflake Notebook:**
    *   Navigate to the **Notebooks** section in Snowsight.
    *   Create a new notebook and import or copy the code from `Titanic Model Tuning Demo.ipynb`.
    *   Ensure the notebook is configured to use the database, schema, and warehouse you created in Step 1.
    *   Run the cells in the notebook to perform data loading, preprocessing, model training, and tuning—all within Snowflake.

---

## Data

The dataset used in this project is from the **Kaggle: "Titanic - Machine Learning from Disaster"** competition. You can find more information about it [here](https://www.kaggle.com/c/titanic).
*   `train.csv`: The training set.
*   `test.csv`: The test set.
