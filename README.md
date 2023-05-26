# mds-pipeline

## Tarefas

### Airbyte 

Primeiro, Fork no repo airbytehq/airbyte, depois clonar para o ambiente de desenvolvimento e rodar os comandos:
cd airbyte
./run-ab-platform.sh

Os arquivos .env e docker-compose.yaml são baixados, mas estão sendo ignorados por .gitignore e .dockerignore. Os removi do arquivo e adicionei todos no meu repo airbyte, além de remover usuário e senha do Airbyte.

### Airflow

https://airflow.apache.org/docs/apache-airflow/stable/howto/docker-compose/index.html

### Metabase