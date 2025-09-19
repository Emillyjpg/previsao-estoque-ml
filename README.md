# 📦 Previsão de Estoque com Machine Learning

Este projeto é uma **adaptação do passo a passo do SageMaker Canvas**, mas utilizando **Python e Scikit-Learn** em ambiente gratuito (Google Colab ou Jupyter Notebook).  
O objetivo é prever a **quantidade de estoque disponível** com base em dados de produto, data e promoções.

---

## 🚀 Tecnologias
- Python 3
- Pandas / Numpy
- Scikit-Learn
- Matplotlib

---

## 📊 Dataset
- **Tamanho**: 500 registros  
- **Colunas**:
  - `ID_PRODUTO`: identificador único
  - `DIA`: data do registro
  - `FLAG_PROMOCAO`: indicador de promoção (0 = não, 1 = sim)
  - `QUANTIDADE_ESTOQUE`: variável alvo (o que queremos prever)

---

## 🔄 Passos do Projeto
1. **Pré-processamento**
   - Conversão da coluna de data.
   - Criação de variáveis derivadas (`ANO`, `MES`, `DIA_SEMANA`).

2. **Treinamento**
   - Divisão treino/teste.
   - Modelo: **Random Forest Regressor**.

3. **Avaliação**
   - RMSE: ~29.9
   - R²: ~-0.09 (modelo inicial, precisa de ajustes).

4. **Previsões**
   - Arquivo `previsoes_estoque.csv` com resultados.

---

## 📈 Resultados (exemplo)
| ID_PRODUTO | Estoque Real | Estoque Previsto |
|------------|--------------|------------------|
| 12         | 7            | 39.5             |
| 24         | 44           | 16.6             |
| 25         | 0            | 24.2             |

---

## 📌 Próximos Passos
- Criar novas features (ex: médias móveis, sazonalidade).
- Testar algoritmos mais avançados (XGBoost, LSTM).
- Ampliar dataset.

---
