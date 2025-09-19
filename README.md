# 📦 Previsão de Estoque com Machine Learning

Este projeto é uma **adaptação do passo a passo do SageMaker Canvas**, utilizando **Python e Scikit-Learn** em ambiente gratuito (Google Colab ou Jupyter Notebook).  
O objetivo é prever a **quantidade de estoque disponível** com base em dados de produto, data e promoções.

---

## 🚀 Tecnologias Utilizadas
- Python 3
- Pandas / Numpy
- Scikit-Learn
- Matplotlib

---

## 📊 Dataset
- **Registros:** 500 linhas  
- **Colunas:**
  - `ID_PRODUTO`: identificador único do produto
  - `DIA`: data do registro
  - `FLAG_PROMOCAO`: indicador de promoção (0 = não, 1 = sim)
  - `QUANTIDADE_ESTOQUE`: variável alvo (estoque real)

Dataset disponível em:  
`dataset/dataset-500-curso-sagemaker-canvas-dio.csv`

---

## 🔄 Passo a Passo do Projeto

### **1. Selecionar Dataset**
- Utilizado o arquivo `dataset-500-curso-sagemaker-canvas-dio.csv`.
- O dataset foi carregado com **Pandas**.
- A coluna `DIA` foi convertida para formato de data.

### **2. Construir e Treinar**
- Criadas variáveis derivadas:
  - `ANO`, `MES`, `DIA_SEMANA`
- Definidas variáveis de entrada (**X**) e saída (**y**).
- Divisão treino/teste (80% / 20%).
- Algoritmo utilizado: **Random Forest Regressor**.

### **3. Analisar**
- Métricas avaliadas:
  - **RMSE (Root Mean Squared Error):** ~29.9
  - **R²:** ~-0.09 (modelo inicial ainda precisa de ajustes).
- Importância das variáveis:
  - `ID_PRODUTO` teve maior peso na previsão.
- O modelo inicial apresenta baixa performance → melhorias futuras.

### **4. Prever**
- Foram geradas previsões para o conjunto de teste.
- As previsões foram salvas no arquivo:
  `resultados/previsoes_estoque.csv`

---

## 📈 Resultados
- O modelo inicial não performou bem (R² negativo).  
- Isso indica que o modelo ainda não explica adequadamente a variabilidade do estoque.  
- Possíveis melhorias:
- Criar novas features (ex: médias móveis, sazonalidade).
- Testar outros algoritmos (XGBoost, LSTM para séries temporais).
- Ampliar o dataset.

---
