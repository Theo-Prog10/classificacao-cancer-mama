# Classificação de Tumores Mamários com Aprendizado de Máquina

## 1. Sobre o projeto

Este projeto tem como objetivo aplicar técnicas de aprendizado de máquina para classificar tumores mamários como **benignos ou malignos**, utilizando o conjunto de dados *Breast Cancer Wisconsin (Diagnostic)*.

O trabalho foi desenvolvido em Python, utilizando um notebook Jupyter no Google Colab, como atividade acadêmica de estudo de classificação supervisionada.

## 2. Conjunto de dados

O dataset contém 569 amostras e 30 características numéricas extraídas de imagens de células mamárias. A variável `diagnosis` indica a classificação do tumor:

- **B:** benigno.
- **M:** maligno.

Fonte: [Breast Cancer Wisconsin (Diagnostic) — Kaggle](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data).

## 3. Etapas desenvolvidas

- Inspeção e análise exploratória dos dados (EDA).
- Análise da distribuição das classes e das características numéricas.
- Visualização de histogramas e boxplots.
- Limpeza dos dados e remoção de colunas desnecessárias.
- Separação dos dados em conjuntos de treinamento e teste.
- Treinamento de modelos de classificação.
- Avaliação por meio de métricas e matriz de confusão.
- Validação cruzada estratificada com cinco divisões (*Stratified K-Fold*).
- Comparação dos modelos e análise das curvas ROC.

## 4. Modelos utilizados

- **Regressão Logística:** com padronização das características numéricas.
- **Random Forest:** conjunto de árvores de decisão, utilizando ponderação das classes.

## 5. Principais resultados

| Métrica no conjunto de teste | Regressão Logística | Random Forest |
|---|---:|---:|
| Acurácia | 96,49% | 96,49% |
| Precisão da classe maligna | 97,50% | 100,00% |
| Recall da classe maligna | 92,86% | 90,48% |
| F1-score da classe maligna | 95,12% | 95,00% |
| AUC-ROC | 0,9960 | 0,9960 |

Na validação cruzada, a Regressão Logística apresentou acurácia média de 97,36%, enquanto o Random Forest apresentou 96,26%.

Considerando os resultados obtidos, a Regressão Logística apresentou o melhor equilíbrio entre as métricas avaliadas e maior recall para a classe maligna entre os dois modelos.

## 6. Tecnologias utilizadas

- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab / Jupyter Notebook
- GitHub

## 7. Como executar

1. Abra o arquivo `classificacao_cancer_mama.ipynb` neste repositório.
2. Clique em **Open in Colab** ou acesse o [Google Colab](https://colab.research.google.com/).
3. Caso necessário, importe o notebook para o Colab.
4. Execute as células em ordem, do início ao fim.

O notebook carrega o conjunto de dados por meio de uma URL e realiza as etapas de análise, treinamento e avaliação dos modelos.

## 8. Limitações

Os resultados dependem do conjunto de dados e da configuração experimental utilizada. Foram avaliados dois algoritmos, sem validação externa em uma base independente. Portanto, os resultados não garantem o mesmo desempenho em outros conjuntos de dados.

**Aviso:** este projeto tem finalidade exclusivamente acadêmica e educacional. Os modelos apresentados não devem ser utilizados para diagnóstico médico ou tomada de decisões clínicas.
