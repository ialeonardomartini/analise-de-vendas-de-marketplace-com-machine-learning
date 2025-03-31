# 🛒 Prevendo Vendas no Marketplace Wish com Machine Learning

![Python](https://img.shields.io/badge/Python-Ecommerce%20Analysis-yellow?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Manipulation-blue?style=for-the-badge&logo=pandas)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML%20Modeling-orange?style=for-the-badge&logo=scikit-learn)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-green?style=for-the-badge&logo=seaborn)

## 📌 Sobre o Projeto

Este projeto tem como objetivo identificar os fatores que mais influenciam o **sucesso de vendas de produtos** no marketplace **Wish**, utilizando **Python, análise de dados e Machine Learning**.

A análise foi feita sobre um dataset real, disponível no [Kaggle](https://www.kaggle.com/datasets/jmmvutu/summer-products-and-sales-in-ecommerce-wish), e passou por um pipeline completo de tratamento, exploração, extração de insights e modelagem preditiva com **Random Forest**.

---

## 🎯 Objetivo

> Desenvolver um modelo de **classificação binária** capaz de prever se um produto terá **alto volume de vendas (acima da mediana de faturamento)** com base em atributos como preço, rating, badges, uso de ad boost, entre outros.

---

## 📚 Etapas do Projeto

### 🧼 1. Qualidade e Preparação dos Dados

- Tratamento de dados ausentes (`product_color`, `origin_country`, `urgency_banner`)
- Conversão de variáveis categóricas e numéricas
- Criação de variáveis como:
  - `income` (faturamento total do produto)
  - `discount` (diferença entre retail price e price)
  - `tags_count` (quantidade de tags)
  - `success` (produto com income > 7.000)

---

### 📊 2. Análise Exploratória (EDA)

- **Distribuições**: vendas, preço, desconto, rating
- **Tags e Wordcloud**: principais palavras associadas a produtos de sucesso vs fracasso
- **Ad Boosts**: impacto na conversão
- **Avaliações e badges**: correlação com vendas
- **Shipping & país de origem**: influência logística
- **Correlação entre variáveis** e análise de produtos campeões

---

### 🧠 3. Machine Learning

- **Modelo utilizado**: `RandomForestClassifier`
- **Features utilizadas**:
  - Preço, desconto, rating, número de tags, badges, shipping express, inventário, etc.
- **Divisão treino/teste**: 70% / 30%
- **Técnicas**:
  - GridSearchCV para otimização de hiperparâmetros
  - Matriz de confusão e classification report
  - Análise de **feature importance**
  - Explicabilidade com **SHAP values**

📈 **Acurácia do modelo**: ~79%  
📊 **F1-score macro**: 0.79

---

## 🏆 Principais Insights

- Produtos com **maior desconto** tendem a vender mais
- **Avaliações altas** e uso de **ad boost** estão associados ao sucesso
- **Badges de qualidade** têm correlação positiva com maiores vendas
- A quantidade de **tags relevantes** também impacta positivamente
- **Produtos de alto sucesso** costumam ser enviados globalmente

---

## 🔗 Fonte dos Dados

📦 [Wish Dataset - Kaggle](https://www.kaggle.com/datasets/jmmvutu/summer-products-and-sales-in-ecommerce-wish)

---

🚀 **Vamos descobrir o que realmente faz um produto vender?**
