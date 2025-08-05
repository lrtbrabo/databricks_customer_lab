<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/main/images/header_genie.png">

# Hands-On LAB 01 - Importando os dados

Treinamento Hands-on na plataforma Databricks com foco nas funcionalidades de Análise Exploratória e Painéis.


## Objetivos do Exercício

O objetivo desse laboratório é importar os DADOS que serão utilizados nos exercícios.
</br></br>

## Exercício 01.01 - Criação do database

``` sql
USE CATALOG dbx_workshop;

CREATE DATABASE IF NOT EXISTS <seu_nome>_schema;

```
</br>

## Exercício 01.02 - Importação dos Arquivos

1.No Repossitório GITHUB, na pasta de DADOS, clique em cada nome do arquivo de dados (*.CSV), e clique no botão para fazer um download local do arquivo, conforme figura abaixo:
</br></br>
<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab1_01.png">

</br>
2.No MENU do Databricks, clique na Opção "+NEW" e na opção  "Add or Upload Data":
</br></br>
<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab1_02.png" width="400px">

</br></br>
3.Escolha a opção "Create or Modify Table":
</br></br>
<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab1_03.png" width="700px">

</br></br>
4.Selecione o nome do Catálogo "dbx_workshop", o nome do SCHEMA "<seu_nome>_schema" e coloque o nome da tabela como "salarios":
</br></br>
<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab1_04.png">
</br></br>

5.Clique em "Create table"
</br></br>

## Exercício 01.03 - Aplicação de funções de governança

1.Clique em "SQL Editor"

2.Execute o seguinte comando SQL:
``` sql
SELECT * FROM dbx_workshop.<seu_nome>_schema.salarios;
```

3.Ainda no SQL Editor, execute o seguinte comando SQL:
``` sql
ALTER TABLE dbx_workshop.<seu_nome>_schema.salarios ALTER COLUMN cpf SET MASK dbx_workshop.gov_rh.cls_salario;
ALTER TABLE dbx_workshop.<seu_nome>_schema.salarios ALTER COLUMN salario_base SET MASK dbx_workshop.gov_rh.cls_salario;
ALTER TABLE dbx_workshop.<seu_nome>_schema.salarios ALTER COLUMN salario_pago SET MASK dbx_workshop.gov_rh.cls_salario;
```

4.Execute o seguinte comando SQL (você vai reparar que o resultado é exatamente o mesmo e nada mudou, está correto):
``` sql
SELECT * FROM dbx_workshop.<seu_nome>_schema.salarios;
```