# StepbyStep-Modelando_um_DataWarehouse
Mostrarei o caminho para a modelagem de um DW, desde a sua criação e modelagem até a exibição de relatórios!

**Passos para a criação de DW:**

**1 - Entrevistas**
 - É o passo onde conversamos com os interessados no DW e analisamos O QUE e COMO vão querer analisar os dados; 
 - Identificamos também as bases de dados de origem, de onde podemos retiras os dados.
 
**2 - Matriz Dimensão x Indicador** 
 - Nesse passo colocamos as informações adiquiridas nas entrevistas em uma Matriz, essa matriz vai possuir indicadores e dimensões: Na vertical da matriz teremos "O que quero analisar? - Indicador", já na Horizontal "Como quero analisar? - Dimensão";
 - Os indicadores que possuem os mesmos cruzamentos são chamados de tabelas de fato.
 
**3 - Modelagem do Data Warehouse**
- Aqui criamos e construímos as tabelas do DW com base na Matriz Dimensão x Indicador, arrumamos os relacionamentos, campos e constraints.

**4 - Carga do DW**
- Nesse passo já precisamos ter noção das fontes de dados para realizar o E.T.L;
- E.T.L (Extract-Tranform-Load): Aqui realizamos a importação do dados de origem para o destino. Como o próprio nome já diz, extraímos de uma origem, transformamos antes de jogar no destino e carregamos no destino.
- Algumas técnicas de transformações são: Limpeza de Dados, Lookup, Union, Funções de transformação, ODS (Tabelas Auxiliares), etc..

**5 - Criação e Carga dos OLAPs**
- Escolher o tipo de OLAP e modelar, temos alguns tipos como: Molap, Holap, Rolap;
- O tipo de OLAP utilizado nessa modelagem é o Rolap: Onde além de guardar as informações em cache, também nos permite consultar as informações em nossa base relacional;
- Fonte OLAP: As tabelas de fato do Data Warehouse que possuem **indicadores**;
- **Por que criar um OLAP?** No OLAP todas as combinações entre os valores já se encontram calculadas e armazenadas, ele é um cubo;
- Lembrete: A linguagem que utilizamos no OLAP não é a T-SQL, usada em bases relacionais, como o OLAP é Multidimensional utilizamos a MDX (MultiDimensional Expression), é uma linguagem de consulta para bases multidimensionais.

**6 - Criação dos relatórios de Analises**
- Aqui realizamos a criação de nossos relatórios análiticos, onde existem 3 tipos:
  * Análise Ad-Hoc: Fornece o OLAP de forma livre para o usuário;
  * Análise Padronizada: Para usuários que não querem se perder no OLAP, mas desejam flexibilidade;
  * Análise Customizada: Para usuários com interesses apenas nas informações do relatório, sem interesse no OLAP.
