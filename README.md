# bagging-randonforest

# Bagging
O objetivo principal do Bagging é evitar o overfitting, que ocorre quando um modelo de machine learning se ajusta excessivamente aos dados de treinamento e apresenta desempenho inferior em novos dados. Para isso, o Bagging emprega a criação de múltiplos modelos de machine learning usando diferentes conjuntos de dados dtreinamento, e a combinação dos resultados desses modelos através da média, visando reduzir a variância geral e melhorar a capacidade de generalização. O Bagging pode ser aplicado com diferentes algoritmos de machine learning, sendo flexível em sua escolha.

# Passo a Passo
## Bootstrap
Sendo uma base de treino 
 com tamanho 
, realizar o bootstrap (amostragem com reposição) é gerarmos 
 novas bases de treino 
, cada uma com tamanho 
. 
 é gerado a partir de amostragens da base 
, uniformemente, aleatóriamente e com reposição.

## Modelagem
Depois de criadas as bases de treino 
 aplicamos o método de modelagem que desejamos a cada uma das 
 bases de treino 
.

## Aggregating
Depois de ajustarmos 
 modelos utilizando as 
 amostras do bootstrap, combinamos os resultados por sua média (para modelos de regressão) ou por votação (para modelos de classificação).


# Random Forest
O Random Forest é uma técnica de aprendizado em conjunto, assim como o Bagging, que é utilizada para tarefas de classificação, regressão e outras. Seu funcionamento é baseado na criação de diversas árvores de decisão, lidando com o problema de overfit ao se criar uma única árvore de decisão com grande profundidade.

Dessa forma, o Random Forest é uma técnica útil para lidar com problemas de overfitting e para melhorar a performance de modelos de aprendizado de máquina em geral. Além disso, ele apresenta a vantagem de ser relativamente fácil de implementar e de ser capaz de lidar com uma grande variedade de tipos de dados.

# Passo a Passo
## Bootstrap + feature selection
Dada uma base de dados, realizaremos uma amostragem com reposição (bootstrap) e geraremos novas bases uniformes, aleatórias e com reposição. Sendo a quantidade e tamanho das bases a ser definidas de antemão, do mesmo modo que no bagging.

O algoritmo de treinamento para a Random Forest aplica a técnica geral do Bootstrap com uma pequena modificação dividindo também as colunas com as variáveis explicativas do modelo (feature selection). Respeitando a regra: m novas bases de dados com raiz quadrada de p colunas de variáveis explicativas para um problema de classificação ou p colunas dividido por 3 de variáveis explicativas para um problema de regressão

Então os passos de modelagem (utilizando árvores de decisão) e aggregating se repetem como no Bagging
