# Product Pricing Prediction Using Hybrid Machine Learning Model 🚀

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![PySpark](https://img.shields.io/badge/PySpark-3.0+-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Big Data](https://img.shields.io/badge/Big%20Data-Enabled-brightgreen.svg)

Welcome to the **Product Pricing Prediction** project! This repository implements a hybrid machine learning model using **PySpark** to predict product prices in a large-scale e-commerce dataset. By combining Random Forest, Gradient Boosted Tree Regressor, and Linear Regression, the model achieves robust price predictions, leveraging big data technologies for scalability and real-time processing. 📊

## 📖 Project Overview

This project tackles the challenge of predicting product selling prices in e-commerce using a big data approach. Key features include:
- **Dataset**: 160,000 rows (80,000 training, 80,000 test) with features like `Product_Brand`, `Item_Category`, `Subcategory_1`, `Subcategory_2`, `Item_Rating`, and `Date`.
- **Technology**: PySpark for distributed computing, handling large datasets efficiently.
- **Hybrid Model**: Combines Random Forest, GBTRegressor, and Linear Regression for improved accuracy.
- **Streaming**: Processes data in batches to simulate real-time price prediction.

The project demonstrates scalable big data analytics, achieving RMSE values as low as 3,605.78, with applications in dynamic pricing and market analysis. 🛍️

## 📂 Repository Structure

```
product-pricing-prediction/
├── dataset/
│   ├── train.csv        # Training dataset (80,000 rows)
│   └── test.csv         # Test dataset (80,000 rows)
├── pricing_prediction.py  # PySpark script for the hybrid model
├── README.md            # Project documentation
├── .gitignore           # Ignores Python temp files
└── .gitattributes       # Git LFS configuration for datasets
```

## 🛠️ Setup Instructions

### Prerequisites
- **Python**: 3.8 or higher
- **PySpark**: 3.0 or higher
- **Git LFS**: For handling large dataset files
- Other dependencies: `pandas`, `matplotlib`, `seaborn`

### Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/product-pricing-prediction.git
   cd product-pricing-prediction
   ```

2. **Install Dependencies**:
   ```bash
   pip install pyspark pandas matplotlib seaborn
   ```

3. **Set Up Git LFS**:
   ```bash
   git lfs install
   git lfs pull
   ```

4. **Verify Dataset**:
   - Ensure `dataset/train.csv` and `dataset/test.csv` are downloaded via Git LFS.
   - If files are missing, run `git lfs pull` again.

## 🚀 Running the Code

Execute the PySpark script to train the model and predict prices:
```bash
spark-submit src/pricing_prediction.py
```

The script:
- Loads and preprocesses the dataset.
- Trains a hybrid model using Random Forest, GBTRegressor, and Linear Regression.
- Processes streaming batches and evaluates performance with RMSE.

## 🔄 Methodology

The project follows a streamlined pipeline, visualized below:

1. **Data Loading** 📥
2. **Exploratory Analysis** 🔍
3. **Data Preprocessing** 🧹
4. **Model Pipeline** 🛠️
5. **Model Training** 🧠
6. **Streaming Processing** 🌊
7. **Model Evaluation** 📈

**Flow Diagram**:
```
Data Loading → Exploratory Analysis → Data Preprocessing → Model Pipeline → Model Training → Streaming Processing → Model Evaluation
```

## 📊 Results

- **Dataset Insights**:
  - Training: 80,000 rows, 8 columns; 9,481 missing `Date` values.
  - Test: 80,000 rows, 7 columns (no `Selling_Price`).
  - `Selling_Price` range: 199 to 30,918 (mean: 3,878.89, std: 8,441.54).
- **Model Performance**:
  - RMSE across 18 streaming batches: 3,605.78 (best) to 4,844.09 (worst).
  - Accurate predictions for many products (e.g., `P-9951`: predicted 416.0, actual 416.0).
  - Challenges with outliers (e.g., `P-4042`: predicted 3,963.14, actual 21,770.0).
- **Top Categories**: Jewellery and home decor dominate sales (up to 2,380,686 and 1,715,850).

## 🔮 Future Work

- 🛡️ **Outlier Handling**: Apply log transformation or robust scaling.
- 🧩 **Feature Engineering**: Add temporal trends or customer reviews.
- 🚀 **Model Enhancement**: Explore deep learning or advanced ensembles.
- 🕒 **Missing Data**: Impute missing `Date` values using temporal patterns.
- 🌐 **Deployment**: Test in a real-time production environment.

## 📜 License

This project is licensed under the [MIT License](LICENSE).

## 🙌 Contributing

Contributions are welcome! Feel free to:
- Open issues for bugs or suggestions.
- Submit pull requests with improvements to code or documentation.

## 📬 Contact

For questions, reach out via GitHub Issues or email at jadoonaqsakhan@gmail.com.

---

⭐ **Star this repository** if you find it useful! Happy coding! 🎉
