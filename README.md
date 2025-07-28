# Wine Quality Prediction

This project explores the use of machine learning, specifically **linear regression**, to predict wine quality based on various **physicochemical attributes**. By understanding which chemical components most influence quality, this tool aims to assist winemakers and sommeliers in evaluating and improving their wine production processes.

## Project Objectives

- Predict wine quality using physicochemical properties of red and white wines.
- Identify the most influential features affecting wine quality.
- Provide data-driven insights to support the wine production and grading process.

## Dataset

The dataset used is sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/186/wine+quality), consisting of:
- **Red wine samples**: 1,599 entries
- **White wine samples**: 4,898 entries
- **Total samples**: 6,497 rows with 11 numerical features and a quality score (target)

### Features:
- Fixed Acidity
- Volatile Acidity
- Citric Acid
- Residual Sugar
- Chlorides
- Free Sulfur Dioxide
- Total Sulfur Dioxide
- Density
- pH
- Sulphates
- Alcohol

##  Data Preprocessing

- Merged red and white wine datasets
- Removed duplicate indexes and checked for null values
- Applied MinMaxScaler for normalisation
- Conducted exploratory data analysis (EDA): skewness, kurtosis, heatmaps, histograms

## Model Development

- **Model used**: Linear Regression (`scikit-learn`)
- **Train/Test Split**: 80/20
- **Cross-Validation**: 5-fold CV
- **Feature Engineering**: Polynomial Features (Degree 2)
- **Key Metrics**:
  - MAE: ~0.58
  - RMSE: ~0.76
  - R²: ~0.21
  - MAPE: ~10.39%

## Key Insights

- **Most influential features**: Alcohol, Citric Acid, Volatile Acidity, Density, Chlorides
- Alcohol has a strong positive correlation with quality
- Volatile Acidity and Chlorides have a strong negative correlation
- Dataset imbalance affects predictive performance (most wines rated 5–7)

## Limitations

- Combined red and white wine data might obscure feature-specific trends
- Imbalanced quality scores (few samples with extreme ratings)
- Linear regression may not capture complex interactions, could explore tree-based models in future

## Potential Applications

- Use model as a preliminary tool for wine quality sorting
- Adapt methodology for related domains like beer or coffee quality prediction
- Automate wine quality control pipelines in wineries

## Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- Seaborn, Matplotlib
