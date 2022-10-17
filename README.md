# Classificação de emoção de tweets com Python

Esse projeto consistem em ler e identificar sentimentos (positivo, negativo, neutro) associados a tweets criados no ano de 2017 no estado de Minas Gerais. Ele foi baseado no curso Análise de Mineração de texto + classificação de emoção (NLP). Os dados foram obtidos do site https://www.kaggle.com/datasets/leandrodoze/tweets-from-mgbr e são tweets de usuários de Minas Gerais, Brasil, entre dezembro de 2016 e fevereiro de 2017.

## Planejamento da Solução

Para fazer análise de sentimento do conteúdo dos tweets a estratégia foi:

**Exploração e ajuste dos dados:**
- Compreender o significado de cada atributo dos dados
- Identificar e tratar dados nulos
- Padronizar as datas 
- Retirar colunas que contenham apenas campos nulos
- Geolocalizar os usuários 
- Retirar textos duplicados, como retweets

**Feature Engineering:**
- Criar features a serem utilizadas no modelo:
  - Quantidade de palavras em cada tweet
  - Frequência de palavras

**Análise exploratória dos dados:**
- Visualizar gráficos da distribuição das classes (negativo, positivo e neutro)
- Análise da quantidade de palavras segundo a classificação dos sentimentos
- Avaliar quais são as palavras mais comuns em tweets classificados com os diferentes sentimentos usando gráficos de nuvens de palavras (Word Cloud)

**Mineração dos textos:**
- Aplicar transformações nas features, facilitando o aprendizado dos modelos
- Remover hyperlinks, hashtags, menções, emojis e valores numéricos
- Converter o texto em minúsculo, para evitar repetições de palavras
- Remover palavras mais comuns que não são impotância na análise (Stop Words)
- Extração do radical das palavras
- Divisão do texto em unidades menores (tokenização)

**Machine Learning Modeling:**
- Usar o modelo Naive Bayes para classificar os tweets
- Aovaliar o modelo através de uma matriz de confusão e das métricas de desempenho precisão, recall, exatidão e F1-score
- Comparar os resultados do modelo Naive Bayes com outros métodos de classificação: Regressão logística, Random Forest, Support Vector Machines

