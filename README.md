# Modern Data Stack Pipeline

Curso da [Stack Academy](https://stackacademy.com.br) para construção de pipeline com Airbyte, Airflow, dbt, Snowflake e Metabase.

![alt text](https://github.com/dfedeoli/mds-pipeline/blob/main/modern_data_stack.png?raw=true)

## Tarefas

### Airbyte 

Primeiro, fiz um Fork no repo **airbytehq/airbyte**, depois clonei o repo para o ambiente de desenvolvimento e rodei os comandos:  
<pre><code>cd airbyte  
./run-ab-platform.sh
</code></pre>

Os arquivos _.env_ e _docker-compose.yaml_ são baixados, mas estão sendo ignorados por _.gitignore_ e _.dockerignore_. Os removi dos arquivos _ignore_ e adicionei todos no meu repo, além de remover usuário e senha do Airbyte. Então, é possível dar o comando para levantar o Docker Compose:  
<pre><code>docker-compose up
</code></pre>

### Airflow

Step-by-step da [Documentação do Airflow](https://airflow.apache.org/docs/apache-airflow/stable/howto/docker-compose/index.html) para instanciar container Docker.


### dbt

Repo [dfedeoli/dbt-model](https://github.com/dfedeoli/dbt-model) com modelos e schema criados no dbt.

### Metabase

Criação de arquivo Docker Compose para levantar container Metabase.
