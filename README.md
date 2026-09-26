🇺🇸 [English version](README-EN.md)

# House Price Prediction

# House Price Prediction

Projeto de Machine Learning desenvolvido para **prever preços de imóveis** e comparar o desempenho de dois modelos de regressão: **Regressão Linear** e **Random Forest Regressor**.

A base utilizada contém **1.460 imóveis e 81 variáveis**, incluindo características como área, qualidade da construção, garagem, porão, número de cômodos e ano de construção. A variável alvo do projeto é `SalePrice`.

## Objetivo

Construir modelos capazes de estimar o preço de venda de imóveis e comparar seus desempenhos utilizando as métricas **MAE, MAPE e R²**.

## Etapas do projeto

- Análise exploratória dos dados;
- Análise dos metadados e tratamento de valores ausentes;
- Engenharia de atributos;
- Separação dos dados em treino (80%) e teste (20%);
- Tratamento de variáveis numéricas com mediana;
- One-Hot Encoding das variáveis categóricas;
- Treinamento da Regressão Linear;
- Treinamento do Random Forest;
- Avaliação e comparação dos modelos.

### Tratamento dos valores ausentes

Um dos principais cuidados durante a preparação dos dados foi analisar os **metadados da base** antes de tratar os valores ausentes.

Em diversas variáveis, `NA` ou `None` não representam um dado desconhecido, mas sim a **ausência de determinada característica no imóvel**, como garagem, piscina, porão ou lareira.

Também foi realizada engenharia de atributos, incluindo a criação de `HasGarage` e `GarageAge`, permitindo representar de forma mais adequada as informações relacionadas à garagem.

## Resultados

| Modelo | MAPE | MAE | R² |
|---|---:|---:|---:|
| Regressão Linear | 12,38% | R$ 19.145 | 0,876 |
| **Random Forest** | **11,01%** | **R$ 17.418** | **0,890** |

O **Random Forest apresentou o melhor desempenho**, obtendo menor erro nas previsões e maior R².

Os resultados também mostram que ambos os modelos conseguiram explicar uma parcela significativa da variação dos preços dos imóveis.

## Conclusão

A comparação mostrou que o Random Forest conseguiu capturar melhor as relações entre as características dos imóveis e seus preços.

Além da modelagem, o projeto reforçou a importância da **compreensão dos dados antes da aplicação de técnicas de tratamento**, principalmente ao lidar com valores ausentes que possuem significado próprio dentro da base.

## Tecnologias

`Python` • `Pandas` • `NumPy` • `Matplotlib` • `Seaborn` • `Scikit-learn`

## Fonte dos dados

Os dados utilizados neste projeto são provenientes da competição
**House Prices - Advanced Regression Techniques**, disponibilizada no Kaggle.

Dataset original: [House Prices - Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data)

Licença: MIT

## Arquivos

```text
house-price-prediction/
│
├── house_price_prediction.ipynb
├── house_prices.csv
├── data_description.txt
└── README.md
```

O notebook contém todo o processo de análise, preparação dos dados, treinamento e avaliação dos modelos.

---

### Autora

**Fernanda Martins Leme**  
Projeto desenvolvido para portfólio em **Ciência de Dados e Machine Learning**.
