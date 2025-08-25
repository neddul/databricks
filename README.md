# Databricks Mini Lakehouse

A tiny end-to-end demo using Databricks:
- Ingest NYC taxi sample data into **Delta Lake**
- Explore with **Spark SQL**
- Train a small **ML** model with **MLflow** tracking
- Schedule the workflow with a **Databricks Job**
- Version control via **Databricks Repos** + **GitHub**

## Notebooks
- `ingest_to_delta` – Loads data into a Delta table (`dbx_demo.nyc_taxi`)
- `transform` – SQL analytics + creates a view (`dbx_demo.vw_zip_stats`)
- `mlflow` – Trains a tiny linear model, logs to MLflow

## How to run (Databricks Free Edition)
1. Clone this repo into **Databricks Repos**
2. Open `ingest_to_delta.ipynb` and **Run All**
3. Open `transform.ipynb` and **Run All**
4. Open `mlflow.ipynb`, set your MLflow experiment path, and **Run All**
5. Check **Experiments** to see metrics and artifacts

## Optional: Schedule as a Job
- **Workflows → Jobs → Create Job**
- Add tasks in order: 01 → 02 → 03
- Use a small serverless SQL warehouse or all-purpose compute (Free Edition quotas apply)
- Set a schedule (e.g., daily)

## Tech
- Apache Spark, Delta Lake, SQL, MLflow
- Databricks Workspaces, Jobs, Repos (GitHub integration)
