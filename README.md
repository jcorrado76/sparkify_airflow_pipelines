# Introduction
***
This is a project that takes some song data loaded in an S3 bucket, creates Airflow DAGs to load that data into a Redshift data warehouse.

# The DAG
***
The default parameters of the dag will follow these guidelines:
* the DAG does not have dependencies on past runs
* on failure, tasks are retried 3 times
* those retries will occur every 5 minutes
* catchup is turned off
* do not email on retry
