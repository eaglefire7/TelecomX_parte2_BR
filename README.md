# Projeto de Machine Learning: Análise e Previsão de Churn de Clientes

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Libraries](https://img.shields.io/badge/Libraries-Scikit--learn%2C%20Pandas%2C%20XGBoost-orange.svg)

## 📖 Sumário Executivo

Este projeto de ponta a ponta aborda o problema crítico de evasão de clientes (churn) numa empresa do setor de telecomunicações. Utilizando um conjunto de dados real, foi realizada uma análise exploratória aprofundada, um pipeline de pré-processamento robusto e o treino de múltiplos modelos de Machine Learning. O modelo **Random Forest** foi selecionado como o de melhor performance, destacando-se pela sua alta capacidade de identificar corretamente os clientes propensos a cancelar. Finalmente, os insights extraídos do modelo foram traduzidos num **plano de ação com estratégias de retenção de clientes** direcionadas e baseadas em evidências.

## 🎯 Objetivo do Projeto

O principal objetivo de negócio foi reduzir a taxa de churn através da criação de um sistema de previsão inteligente. Os objetivos específicos foram:
* **Analisar** o comportamento da base de clientes para entender os principais motivos que levam ao cancelamento.
* **Construir** um modelo de Machine Learning preciso para identificar clientes com alta probabilidade de churn.
* **Propor** ações de retenção proativas e personalizadas com base nos insights gerados pelo modelo.

## 📂 O Conjunto de Dados

O projeto utilizou o ficheiro `dados_tratados.csv`, contendo informações anonimizadas sobre os clientes, incluindo:
* **Dados Demográficos:** Género, idade (Sénior), parceiros e dependentes.
* **Serviços Contratados:** Telefonia, múltiplas linhas, tipo de serviço de internet, segurança online, etc.
* **Informações de Contrato e Fatura:** Tipo de contrato, tempo de contrato (tenure), método de pagamento e valores.

## 🛠️ Metodologia

O projeto seguiu um pipeline de Data Science estruturado em 5 etapas principais:

1.  **Análise Exploratória de Dados (EDA):** Investigação visual e estatística para identificar padrões, correlações e os primeiros insights sobre os fatores de churn. Foram criados gráficos de distribuição, boxplots e heatmaps de correlação.

2.  **Pré-processamento e Engenharia de Features:**
    * Limpeza e tratamento de dados.
    * Transformação de variáveis categóricas em numéricas (One-Hot Encoding).
    * Balanceamento do conjunto de dados com a técnica **SMOTE** para corrigir o forte desequilíbrio entre as classes.
    * Padronização de features (`StandardScaler`) para preparar os dados para modelos sensíveis à escala.

3.  **Modelagem e Treino:**
    * Divisão dos dados em conjuntos de treino e teste (70/30) de forma estratificada.
    * Treino de um vasto leque de algoritmos de classificação:
        * Modelos Lineares: Regressão Logística, SVM.
        * Modelos Baseados em Instância: KNN.
        * Modelos de Ensemble: Random Forest, XGBoost.
        * Redes Neuronais: MLPClassifier.

4.  **Avaliação e Comparação de Modelos:**
    * Utilização de métricas como Acurácia, Precisão, Recall e F1-Score para avaliar a performance.
    * Análise detalhada com Matrizes de Confusão.
    * Diagnóstico de overfitting/underfitting comparando a performance nos dados de treino e teste.

5.  **Interpretação e Análise de Variáveis:**
    * Análise de importância de variáveis (Feature Importance, Coeficientes, Permutation Importance) para entender o que cada modelo "aprendeu".

## 💡 Principais Insights e Fatores de Risco

A análise, confirmada consistentemente por todos os modelos de alta performance, apontou os seguintes fatores como os principais impulsionadores do churn:
* 📉 **Tipo de Contrato:** Contratos **mensais** são o maior indicador de risco.
* ⏳ **Tempo de Contrato (Tenure):** Clientes **novos** (com baixo *tenure*) têm uma probabilidade de evasão drasticamente maior.
* 💻 **Serviço de Internet e Custo:** Clientes com serviço de **Fibra Óptica** e **faturas mensais mais altas** tendem a cancelar mais.

## 🚀 Resultados e Estratégias Propostas

O modelo **Random Forest** foi o grande destaque, alcançando uma **Acurácia de Teste de 88%** e, mais importante, um **Recall de 84%** para a classe "churn", provando a sua eficácia em detetar clientes em risco. Com base nos insights, as principais recomendações estratégicas são:

1.  **Criar campanhas de incentivo** para a migração de clientes de contratos mensais para anuais.
2.  **Implementar um programa de onboarding** proativo para clientes nos primeiros 90 dias.
3.  **Revisar a estrutura de preços e valor agregado** para os planos de Fibra Óptica.

## ⚙️ Como Executar o Projeto

1.  Clone este repositório: `git clone (https://github.com/eaglefire7/TelecomX_parte2_BR.git)`
2.  Instale as bibliotecas necessárias: `pip install pandas scikit-learn imbalanced-learn xgboost matplotlib seaborn`
3.  Execute o notebook Jupyter `[TelecomX_parte2_BR.ipynb`. Certifique-se de que o ficheiro `dados_tratados.csv` está no mesmo diretório.
