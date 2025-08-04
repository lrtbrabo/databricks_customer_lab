<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/main/images/header_genie.png">

# Hands-On LAB 01 - Importando os dados

Treinamento Hands-on na plataforma Databricks com foco nas funcionalidades de Análise Exploratória e Painéis.


## Objetivos do Exercício

O objetivo desse laboratório é importar os DADOS que serão utilizados nos exercícios.
</br></br></br>

## Exercício 01.01 - Criação do database

``` sql
USE CATALOG dbx_workshop;

CREATE DATABASE IF NOT EXISTS <seu_nome>_schema;

```
</br></br>

## Exercício 01.02 - Importação dos Arquivos

No Repossitório GITHUB, na pasta de DADOS, clique em cada nome do arquivo de dados (*.CSV), e clique no botão para fazer um download local do arquivo, conforme figura abaixo:
</br></br>
<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/main/images/lab1_01.png">

</br></br></br>
No MENU do Databricks, clique na Opção "+NEW" e na opção  "Add or Upload Data":
</br></br>
<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/main/images/lab1_02.png" width="400px">

</br></br></br>
Escolha a opção "Create or Modify Table":
</br></br>
<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/main/images/lab1_03.png" width="700px">

</br></br></br>
Selecione o nome do Catálogo  (ACADEMY), o nome do SCHEMA (GENIE_AIBI) e um nome pra nova tabela:

<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/main/images/lab1_04.png">
</br></br>
</br></br></br>




