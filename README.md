Data Prep Essencial: Desafio Titanic (Kaggle)

🚢 Visão Geral do Projeto
Este projeto documenta um pipeline completo de Data Preprocessing (Pré-processamento de Dados) para o renomado dataset do desafio Titanic, do Kaggle. O objetivo é transformar o conjunto de dados bruto em uma base limpa, tratada, e pronta para ser consumida por modelos de Machine Learning, seguindo as melhores práticas da ciência de dados.

O notebook detalha o processo, desde a limpeza inicial até a normalização final, criando um alicerce sólido para a fase de modelagem preditiva.

🛠️ Principais Etapas de Pré-processamento (Data Prep)
O processo seguiu as seguintes etapas críticas:

1. Separação de Variáveis e Limpeza Inicial
Identificação da Variável-Resposta: A coluna Survived foi separada imediatamente, garantindo que o processo de tratamento e normalização do dataset de features não fosse influenciado pela variável que se deseja prever.

Remoção de Variáveis Irrelevantes/Sensíveis: Variáveis com baixa utilidade preditiva ou que contêm informações sensíveis, como Name (Nome) e PassengerId (ID do Passageiro), foram removidas logo no início do processo.

2. Tratamento Rigoroso de Valores Nulos (Missing Values)
O tratamento de dados ausentes foi feito com critérios rigorosos:

Eliminação de Colunas Vazias: Colunas com mais de 75% de valores nulos foram descartadas por serem consideradas incompletas demais para contribuir significativamente para o modelo.

Imputação para Dados Numéricos: Para as features numéricas restantes, os valores ausentes foram preenchidos com a média da respectiva coluna.

Imputação para Dados Categóricos: Para variáveis categóricas (como Embarked), os valores nulos foram substituídos pela string "Desconhecido", preservando o registro e criando uma nova categoria informativa.

3. Engenharia e Codificação de Variáveis Categóricas
Extração de Informação: Como forma de obter mais informação, o Title (Título, e.g., Mr., Miss., Mrs.) foi extraído da coluna Name antes de sua remoção. Esta nova feature titulo foi então codificada usando Label Encoding.

One-Hot Encoding: Variáveis nominais como Sex foram transformadas usando One-Hot Encoding (criação de dummy variables), o que é essencial para evitar que o modelo interprete as categorias como tendo uma ordem numérica.

4. Normalização Z-Score (Padronização)
A etapa final do pré-processamento envolveu a padronização das features numéricas através da Normalização Z-Score (Standard Scaling).

Esta técnica transforma os dados para que tenham média igual a 0 e desvio-padrão igual a 1.

A padronização é fundamental para que algoritmos baseados em distância ou gradiente (como K-Nearest Neighbors, Regressão e Redes Neurais) não deem pesos desproporcionais a features com escalas maiores.

📁 Estrutura do Repositório
Untitled10.ipynb: Notebook principal (Google Colab) contendo o código completo do pipeline de Data Prep.

🚀 Tecnologias e Bibliotecas
Python

Pandas: Usada para manipulação, limpeza e análise exploratória inicial dos dados.

Scikit-learn (Sklearn): Utilizada para a implementação do StandardScaler (Z-Score) e técnicas de Encoding (Label e One-Hot).

📊 Fonte do Dataset
Os dados utilizados neste projeto são provenientes do famoso desafio de Machine Learning:

Kaggle: Titanic - Machine Learning from Disaster
