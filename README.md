# Modern Data Stack Pipeline

Pipeline com Airbyte, Airflow, dbt, Snowflake e Metabase.

## Tarefas

### Airbyte 

Primeiro, Fork no repo airbytehq/airbyte, depois clonar para o ambiente de desenvolvimento e rodar os comandos:  
<pre><code>cd airbyte  
./run-ab-platform.sh
</code></pre>

Os arquivos .env e docker-compose.yaml são baixados, mas estão sendo ignorados por .gitignore e .dockerignore. Os removi do arquivo e adicionei todos no meu repo airbyte, além de remover usuário e senha do Airbyte.

### Airflow

Step-by-step da [Documentação do Airflow](https://airflow.apache.org/docs/apache-airflow/stable/howto/docker-compose/index.html).

### dbt

Repo [dfedeoli/dbt-model](https://github.com/dfedeoli/dbt-model) com modelos e schema criados no dbt.

### Metabase
