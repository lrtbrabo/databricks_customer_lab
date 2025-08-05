<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/main/images/header_genie.png">

# Hands-On LAB 03 - Criando o Dashboard AI/BI

Treinamento Hands-on na plataforma Databricks com foco nas funcionalidades de Análise Exploratória e Painéis.
</br></br>

## Objetivos do Exercício

O objetivo desse laboratório é montar um Painel, utilizando os dados de salário.
</br></br></br>


## Exercício 03.00 - Passo a Passo na criação do Painel

1.Para criar um painel no AI/BI, comece clicando em "Dashboards" na aba lateral esquerda do Databricks e em seguida clique em "Create Dashboard"

<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab3_01.png">
</br></br>

2.Uma vez na interface do AI/BI Dashboards, você vai clicar em "Data" no canto esquerdo. Após isso, clique em "Add data source" e coloque o path da sua tabela de salários

<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab3_02.png">
</br></br>

3.Agora clique em "Untitled page" logo ao lado do botão "Data". A interface "canvas" vai abrir para que você possa criar o seu painel. Para adicionar uma visualização, clique no botão conforme ilustra a imagem

<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab3_03.png">
</br></br>

4.Você vai ver que a seguinte interface vai aparecer para você. Note que é uma interface de chat, então você pode interagir com ela utilizando português sem maiores problemas. Vamos testar isso nos próximos passos

<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab3_04.png">
</br></br>

5.Nessa interface de chat, digite "Faça um counter da soma do salário base". O seu resultado deve ser algo similar ao da imagem abaixo. Aceite a sugestão da AI e posicione onde achar melhor. (Caso o resultado seja diferente da imagem abaixo, chame o instrutor) 

<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab3_14.png">
</br></br>

5.Agora vamos adicionar mais algumas outras visualizações conforme abaixo repetindo os passos 4 e 5. Caso você tenha alguma dificuldade, chame o instrutor. 

- Faça um counter da média do salário base
- Faça um counter da média do salário pago
- Faça um gráfico de distribuição da média das comissões pagas por cargo
- Faça a evolução da folha salarial ao longo do tempo

</br></br>

6.Além disso, é possível criar visualizações de "forma tradicional" utilizando a interface. No momento que você clica no botão para adicionar uma nova visualização, invés de utilizar o chat, utilize a interface a direita para criar a seguinte visualização:

<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab3_05.png">
</br></br>

7.Também podemos adicionar tabelas inteiras na interface, adicione uma nova visualização e coloque o texto "7. Faça uma tabela com todas as informações".

<br>

8.Se tudo deu certo até aqui, você deve ter algo parecido com a imagem abaixo.

<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab3_06.png">
</br></br>

8.Agora vamos adicionar alguns filtros. Para isso, clique no botão de adição de filtros conforme a imagem abaixo:

<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab3_07.png">
</br></br>

9.Faça a configuração do seu primeiro filtro conforme a imagem abaixo. Este filtro vai nos permitir fazer um filtro por um range da datas:

<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab3_08.png">
</br></br>

10.Vamos adicionar mais dois filtros, um para cargo e outro para faixa salarial, adicione mais 2 filtros e os coloque com as seguintes configurações:

<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab3_09.png">
<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab3_10.png">
</br></br>

11.Se você seguiu as intruções até aqui corretamente, o seu painel atual deve se parecer com a imagem abaixo (note que o local das visualizações podem estar diferentes, isso não tem impacto para nosso cenário de testes):

<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab3_11.png">
</br></br>

12.Agora vamos começar o passo de publicação do painel, mas antes disso, vamos renomear a nossa página e nosso painel. Clique no nome do painel (ele vai estar nomeado como "New Dasboard <timestamp_de_criação>") e troque o nome para "<seu_nome>_lab_dashboard". Além disso, clique nos 3 pontinhos verticais ao lado de "Untitled page" logo abaixo do nome do dashboard e selecione "rename". Pode escolher o nome que julgar melhor. 

<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab3_12.png">
</br></br>

13.Clique em "Publish" no canto direito superior da interface do AI/BI. A tela abaixo será exibida para você. Para configurar, clique em "Don't embed credentials", selecione a flag de "Enable Genie" e selecione a opção "Link existing Genie space", nesse campo, adicione a url do ambiente Genie que você criou no laboratório anterior. Clique em "Publish" e agora seu painel está oficialmente publicado!

<img src="https://raw.githubusercontent.com/lrtbrabo/databricks_customer_lab/refs/heads/main/images/lab3_13.png">
</br></br>

---
Parabéns! Você completou o laboratório AI/BI Genie e Dashboards!