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
