<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/main/images/header_genie.png">

# Hands-On LAB 02 - Criando o AI/BI Genie


Treinamento Hands-on na plataforma Databricks com foco nas funcionalidades de perguntas e respostas usando linguagem natural.

## Objetivos do Exercício

O objetivo desse laboratório é usar o AI/BI Genie para permitir a análise de dados de vendas utilizando somente **Português**.


## Exercício 02.00 - Preparação

1.Para criar o ambiente Genie, comece clicando em "Genie" na aba lateral esquerda do Databricks

<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab2_01.png">
</br></br>

2.Clique no botão "New" no canto direito superior

3.Utilize a interface que abriu para procurar pela sua tabela e após selecionar clique em "Create"
<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab2_02.png">

4.A seguinte interface vai aparecer para você. Altere o nome no canto esquerdo superior colocando "<seu_nome>_genie". Após isso, você pode começar a interagir com os dados de salários utilizando o chat:
<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab2_03.png">

5.Fique livre para testar as mais diversas perguntas, não queremos intervir na sua criatividade aqui. Gaste alguns minutos perguntando curiosidades sobre o salário dos funcionários para ele, além disso, você pode utilizar instruções para deixar as coisas mais interessantes. Por exemplo, tente perguntar para ele "O salário pago para os funcionários está dentro dentro da faixa de comissão?", você vai reparar que ele não consegue responder a esta pergunta pois ele não tem o contexto de pagamento da empresa.

Podemos adicionar conhecimento coorporativo ao Genie através das instruções. Clique em "configure" no canto direito superior do Genie e depois em "Instructions". Adicione o seguinte texto nas instruções: "O salário pago de um funcionário deve ser de 5% a 10% maior que o salário base por conta da comissão". Inicie um novo chat e realize a mesma pergunta para ele "O salário pago para os funcionários está dentro dentro da faixa de comissão?".

No meu caso, podemos ver que ele retorna uma análise no desvio do salário dos funcionários com base na nova regra inserida.
<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab2_04.png">

<br>

6.Além disso, podemos adicionar funções ao Genie para que ele gere "Trusted Assets", que são queries onde a AI não aluciou pois ela foi gerada/curada por um ser humano. Pense nisso como um "selo de verificado" da sua rede social favorita! Para adicionarmos um Trusted Asset. Pergunte para o Genie "Quais as estatísticas dos salários de analistas?", ele vai retornar algo parecido com esse resultado:
<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab2_05.png">

7.Note que ao clicar em "Show code" ele te mostra a query que foi gerada. Volte no seu "SQL Editor" e adicione o código abaixo (Após o RETURN tem a query que o Genie gerou para mim, substitua pela sua query):
```sql
CREATE OR REPLACE FUNCTION dbx_workshop.<seu_nome>_schema.get_analyst_statistics()
  RETURNS TABLE
  COMMENT 'Use esta função para pegar as estatísticas sobre os salários dos analistas'
  RETURN 
    SELECT
      MIN(`salario_base`) AS min_salario_base,
      MAX(`salario_base`) AS max_salario_base,
      AVG(`salario_base`) AS avg_salario_base,
      STDDEV(`salario_base`) AS stddev_salario_base,
      MIN(`salario_pago`) AS min_salario_pago,
      MAX(`salario_pago`) AS max_salario_pago,
      AVG(`salario_pago`) AS avg_salario_pago,
      STDDEV(`salario_pago`) AS stddev_salario_pago
    FROM
      `dbx_workshop`.`<seu_nome>_schema`.`salarios`
    WHERE
      `cargo` = 'Analista'
```

<br>

8.Após executar essa query, voltei no seu Genie Space e siga "Configure" -> "SQL Queries". Clique na seta para baixo e selecione "SQL Function". Após isso, selecione o seu catálogo, schema e função.
<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab2_06.png">

9.Clique em "New chat" e refaça a pergunta "Quais as estatísticas dos salários de analistas?". Note que desta vez, além de executar mais rápido, ele também vai trazer um "selo de verificado".
<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab2_07.png">