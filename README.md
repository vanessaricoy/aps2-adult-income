# APS2 — Classificação: Adult Income Census

**Disciplina:** Machine Learning  
**Integrantes:** Vanessa Ricoy e Victor Cunha  
**Projeto:** APS2 — Classificação

## Sobre o projeto

Este repositório contém a segunda etapa do projeto de Machine Learning, dando continuidade à análise exploratória de dados (APS1).

O objetivo é desenvolver e avaliar modelos de classificação para prever se a renda anual de um indivíduo pertence à faixa `<=50K` ou `>50K`, utilizando características socioeconômicas do dataset Adult Income Census.

O trabalho contempla pré-processamento, comparação de algoritmos, otimização de hiperparâmetros, avaliação de desempenho, explicabilidade e discussão crítica dos resultados.

## Relatório publicado

O relatório completo, incluindo códigos, gráficos e análises, está disponível no GitHub Pages:

**[Acessar relatório da APS2](https://vanessaricoy.github.io/aps2-adult-income/)**

## Modelos utilizados

Foram implementados e comparados três modelos:

1. Dummy Classifier — modelo de referência (baseline).
2. Logistic Regression — modelo linear com regularização L2.
3. Random Forest — ensemble de árvores de decisão.

A seleção foi realizada por validação cruzada estratificada, utilizando Average Precision (AP) como métrica principal.

Os modelos foram ajustados por busca de hiperparâmetros, com GridSearchCV ou RandomizedSearchCV.

## Pré-processamento

O projeto utiliza Pipeline e ColumnTransformer do Scikit-learn, incluindo:

- Tratamento de valores ausentes;
- Imputação pela mediana para variáveis numéricas;
- RobustScaler para escalonamento;
- OneHotEncoder para variáveis categóricas;
- Avaliação do agrupamento de categorias raras.

## Resultados

O melhor modelo selecionado foi a **Random Forest**, utilizando o pipeline original.

| Métrica | Resultado |
|---|---:|
| Accuracy | 0.812 |
| Precision | 0.582 |
| Recall | 0.775 |
| F1-score | 0.665 |
| ROC-AUC | 0.884 |
| Average Precision | 0.703 |

Os resultados foram obtidos no conjunto de teste reservado, após a seleção do modelo e dos hiperparâmetros.

## Interpretabilidade

O projeto apresenta:

- Análise dos coeficientes da regressão logística;
- Importância das variáveis por permutação na Random Forest;
- Importância global das features com SHAP;
- Explicação de três predições individuais com SHAP.

## Discussão crítica

São discutidas limitações do modelo e do dataset, além de propostas para monitoramento, manutenção e aplicação responsável da solução.

## Ferramentas utilizadas

- Python
- Pandas e NumPy
- Matplotlib e Seaborn
- Scikit-learn
- SHAP
- Jupyter Notebook

## Arquivos

- `APS2_Adult_Income.ipynb` — Notebook original com códigos, análises e resultados.
- `index.html` — Relatório publicado no GitHub Pages.

## Dataset

[Adult Income Census — Kaggle](https://www.kaggle.com/datasets/anaghakp/adult-income-census)

## Etapa anterior

[APS1 — Análise Exploratória de Dados: Adult Income Census](https://vanessaricoy.github.io/aps1-adult-income/)
