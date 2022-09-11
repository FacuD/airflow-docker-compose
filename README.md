# Running Airflow 2.0 with Docker (Easy)

### The idea of this repository is to have in one place all the necessary to run Airflow with docker

1. `mkdir airflow-docker && cd airflow-docker`
2. `curl -LfO https://airflow.apache.org/docs/apache-airflow/stable/docker-compose.yaml`
3. `mkdir ./dags ./plugins ./logs`
4. `echo -e "AIRFLOW_UID=$(id -u)\nAIRFLOW_GID=0" > .env`
5. `docker-compose up airflow-init`
6. `docker-compose up`
7. Then you can visit `http://localhost:8080/` and log in with username and password "airflow"
8. Use `docker-compose down` to stop containers and remove containers, networks, volumes, and images created by `docker-compose up`

### All credits to [Data with Marc](https://www.youtube.com/watch?v=aTaytcxy2Ck)
