# Modern Data Stack Pipeline

Curso da [Stack Academy](https://stackacademy.com.br) para construção de pipeline com Airbyte, Airflow, dbt, Snowflake e Metabase.

![alt text](https://github.com/dfedeoli/mds-pipeline/blob/main/modern_data_stack.png?raw=true)

## Obtenção das ferramentas

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

### Snowflake
Criação de Warehouse e todas entidades a partir de arquivo DDL.

### dbt

Repo [dfedeoli/dbt-model](https://github.com/dfedeoli/dbt-model) com modelos e schema criados no dbt.

### Metabase

Criação de arquivo Docker Compose para levantar container Metabase.


## Breakdown das tarefas

### Infraestrutura

* Setup do ambiente de desenvolvimento no Gitpod.io
* Setar as Permissoes do Gitpod ao Repositorio no GitHub
* Subir o Airbyte via Docker
* Subir o Airflow via Docker
* Subir o Metabase via Docker
* Criar o script de execução
* Testar a execução

### Snowflake Data Warehouse

* Criar a Conta no snowflake
* Verificar a existência das tabelas
* Obter os links de conexão e nome da conta

### Extração:

#### No Airbyte

* Conectar com as origens baseadas nos arquivos .csv
* Criar as entidades no snowflake através do script base da documentação
* Conectar o destino no snowflake
* Criar as conexões do Airbyte associando as origens ao destino 
* Testar as conexões

### Preparação:

#### No Airbyte (Destination Loading Method)

Local Staging (Ambiente de Desenvolvimento)
Cloud Staging (Ambiente de Produção)

### Transformação:

#### No dbt

* Criação da Conta
* Conexão com o GitHub X
* Criação do Dbt Project
* Criação do Profile de conexão com o snowflake
* Criação do Schema
* Criação dos Modelos Base
* Criação do Modelo Relacionado
* Visualização gráfica do modelo
* Teste de execução
* Commits, Branches, Pull Requests, Merges no Github
* Obtenção do link de conexão com o Airbyte


### Visualização:

#### No Metabase

* Conectar Metabase com o Snowflake
* Criar uma Question
* Criar um Dashboard
* Adicionar uma Question
* Visualizar o Resultado

### Orquestração:

#### No Airflow

* Criar a dag
* Criar a Docker network
* Incluir nos Docker Composes a network criada
* Setup no serviço
* Testar a conexão entre os containers do Airflow e do Airbyte
* Criar as conexões com o Airbyte através do script
* Testar a execução do pipeline
