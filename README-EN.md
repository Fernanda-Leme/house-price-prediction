[Versão em Português](README.md)

# House Price Prediction

Machine Learning project developed to **predict house prices** and compare the performance of two regression models: **Linear Regression** and **Random Forest Regressor**.

The dataset contains **1,460 properties and 81 variables**, including characteristics such as area, construction quality, garage, basement, number of rooms, and year of construction. The target variable of the project is `SalePrice`.

## Objective

Build models capable of estimating house sale prices and compare their performance using the **MAE, MAPE, and R²** metrics.

## Project Steps

- Exploratory Data Analysis;
- Metadata analysis and missing value treatment;
- Feature engineering;
- Data split into training (80%) and testing (20%) sets;
- Treatment of numerical variables using the median;
- One-Hot Encoding of categorical variables;
- Linear Regression training;
- Random Forest training;
- Model evaluation and comparison.

### Missing Value Treatment

One of the main considerations during data preparation was analyzing the **dataset metadata** before treating missing values.

For several variables, `NA` or `None` does not represent unknown data, but rather the **absence of a specific property feature**, such as a garage, pool, basement, or fireplace.

Feature engineering was also performed, including the creation of `HasGarage` and `GarageAge`, allowing garage-related information to be represented more appropriately.

## Results

| Model | MAPE | MAE | R² |
| --- | ---: | ---: | ---: |
| Linear Regression | 12.38% | $19,145 | 0.876 |
| **Random Forest** | **11.01%** | **$17,418** | **0.890** |

The **Random Forest achieved the best performance**, with lower prediction errors and a higher R².

The results also show that both models were able to explain a significant portion of the variation in house prices.

## Conclusion

The comparison showed that Random Forest was able to better capture the relationships between property characteristics and their prices.

In addition to model development, the project reinforced the importance of **understanding the data before applying data treatment techniques**, especially when dealing with missing values that have a specific meaning within the dataset.

## Technologies

`Python` • `Pandas` • `NumPy` • `Matplotlib` • `Seaborn` • `Scikit-learn`

## Data Source

The data used in this project comes from the **House Prices - Advanced Regression Techniques** competition, available on Kaggle.

Original dataset: [House Prices - Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data)

License: MIT

## Files

```text
house-price-prediction/
│
├── house-price-prediction.ipynb
├── house_prices.csv
├── data_description.txt
├── README.md
└── README-EN.md
```

The notebook contains the complete process of data analysis, data preparation, model training, and model evaluation.

---

### Author

**Fernanda Martins Leme**

Project developed as part of my **Data Science and Machine Learning portfolio**.
