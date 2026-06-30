# California Housing Prices Dataset

Predicting housing prices in California using machine learning.

This project focuses on exploratory data analysis (EDA), data preprocessing, and the training of multiple regression models to predict the median house values in California based on various demographic and geographical features.

## Features

* **Exploratory Data Analysis (EDA):** Visualizing data distributions and feature correlations.
* **Data Preprocessing:** Handling missing values, scaling numerical features, and encoding categorical variables.
* **Machine Learning Pipeline:** Splitting data and creating transformation pipelines using Scikit-Learn.
* **Model Training & Evaluation:** Implementing and comparing various regression algorithms including Linear Regression, Decision Trees, Random Forests, Gradient Boosting, XGBoost, and K-Nearest Neighbors.
* **Jupyter Notebooks:** Code is cleanly separated into individual notebooks for different algorithms and consolidated workflows.

## Tech Stack

| Category | Technology |
| --- | --- |
| **Data Manipulation** | Pandas, NumPy |
| **Data Visualization** | Matplotlib, Seaborn |
| **Machine Learning** | Scikit-Learn, XGBoost |
| **Development Environment** | Jupyter Notebook |

## Architecture / Project Structure

The repository is structured around a central CSV dataset and several Jupyter notebooks representing different stages of the machine learning lifecycle.

```text
.
├── .ipynb_checkpoints/                            # Jupyter auto-saves
├── AllModels.ipynb                                # Consolidated notebook training and evaluating all models
├── California Housing Prices.ipynb                # Main notebook for data exploration and preprocessing
├── California_Housing_Prices_DecisionTree.ipynb   # Decision Tree Regression model training
├── California_Housing_Prices_LinearRegression.ipynb # Linear Regression model training
├── California_Housing_Prices_RandomForest.ipynb   # Random Forest Regression model training
└── housing.csv                                    # The California Housing Prices dataset

```

* **`housing.csv`**: The primary dataset used for the project.
* **`California Housing Prices.ipynb`**: Responsible for the initial EDA, understanding the dataset structure, and building data transformation pipelines.
* **Individual Model Notebooks**: Isolate the training and evaluation logic for specific algorithms.
* **`AllModels.ipynb`**: A unified workflow that imports all necessary libraries and trains multiple models side-by-side for comparison.

## How It Works

1. **Data Loading:** The `housing.csv` file is loaded into a Pandas DataFrame.
2. **EDA:** The data is visualized using Seaborn and Matplotlib to identify trends (e.g., median income vs. house value) and outliers.
3. **Preprocessing:** - Missing values in columns like `total_bedrooms` are imputed using Scikit-Learn's `SimpleImputer`.
* The categorical feature `ocean_proximity` is converted into numerical values using `OneHotEncoder`.
* Numerical features are scaled using `StandardScaler`.


4. **Data Splitting:** The data is divided into training and testing sets using `train_test_split`.
5. **Modeling:** The preprocessed training data is passed to various regressor models (Linear, Decision Tree, Random Forest, Gradient Boosting, XGBoost).
6. **Evaluation:** The models are cross-validated and evaluated to determine their predictive accuracy.

## Installation

To run this project locally, clone the repository and install the required Python libraries.

```bash
# Clone the repository
git clone https://github.com/arnavmaheshwari/california-housing-prices-dataset.git

# Navigate to the project directory
cd california-housing-prices-dataset

# Install dependencies
pip install pandas numpy scikit-learn matplotlib seaborn xgboost jupyter

# Launch Jupyter Notebook
jupyter notebook

```

## Environment Variables

*No environment variables are required to run this project.*

## Usage

1. Start the Jupyter Notebook server using the installation instructions above.
2. Open `California Housing Prices.ipynb` to explore the dataset and view the preprocessing pipeline.
3. Open `AllModels.ipynb` or any of the algorithm-specific notebooks to execute the machine learning models.
4. Run the cells sequentially to observe model training and performance metrics.

## API Documentation

*No APIs are exposed in this project.*

## Database

* **Technology:** Flat File (CSV)
* **Schema Overview:** Contains 20,640 records with 10 columns: `longitude`, `latitude`, `housing_median_age`, `total_rooms`, `total_bedrooms`, `population`, `households`, `median_income`, `median_house_value`, and `ocean_proximity`.

## Screenshots

## Deployment

*This project is currently for local execution and research purposes. No automated deployment pipelines (like Docker or GitHub Actions) are configured.*

## Testing

There are no dedicated unit test files. Model validation is integrated directly within the Jupyter notebooks using Scikit-Learn's `cross_val_score` and `train_test_split`.

## Performance / Optimization

* Built automated preprocessing pipelines (`Pipeline` and `ColumnTransformer`) to prevent data leakage and ensure consistent scaling.
* Utilized ensemble methods (Random Forest, Gradient Boosting, XGBoost) to significantly optimize predictive performance over standard linear models.

## Security

*Not applicable for this static data science repository.*

## Future Improvements

* Implement hyperparameter tuning using `GridSearchCV` or `RandomizedSearchCV` to optimize model parameters.
* Build a web interface using Streamlit or Gradio to allow users to input custom housing metrics and get a price prediction.
* Package the best-performing model into a deployable REST API.

## Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the project.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a pull request.

## License

This project is licensed under the MIT License.

## Author

**Arnav Maheshwari** [GitHub Profile](https://www.google.com/search?q=https://github.com/arnavmaheshwari)

## Acknowledgements

* [Scikit-Learn Documentation](https://scikit-learn.org/)
* [XGBoost](https://xgboost.readthedocs.io/)
* The California Housing Prices Dataset (originally derived from the 1990 California census)
