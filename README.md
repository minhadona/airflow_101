# airflow_101

## level 1: 
> only airflow container

airflow container has the following mandatory services:
-  postgres (optional?)
-  redis : broker that forwards messages from scheduler to worker
-  webserver : webserver available at http://localhost:8080
-  scheduler : monitors all tasks and DAGs, then triggers the task instances once their dependencies are complete
-  worker : worker that executes the tasks given by the scheduler
-  flower : for monitoring the environment
-  airflow-init : initialization service

*descriptions provided by [official doc](https://airflow.apache.org/docs/apache-airflow/2.0.1/start/docker.html)*

in x-airflow-common, the volumes are mapped from inside to outside. on the local machine (a folder named /dags on current directory is created to bridge the inside of docker at /opt/airflow/dags) 

## level 2:
