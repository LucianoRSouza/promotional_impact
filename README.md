# ML Promotional Impact on Sales

This project explores the impact of promotions on sales using a Gradient Boosting Regressor model. The dataset contains information about sales, promotions, and product details.

## Dataset

The (invented for reference only)dataset `promotional_sales_data.csv` contains the following columns:

- `date`: The date of the sale
- `total_sales`: The total sales value for each transaction
- `location`: The location where the sale occurred
- `product_type`: The type of product sold
- `sales_price`: The price of the product
- `quantity_sold`: The quantity of the product sold in the transaction
- `promotion`: Binary value (0 or 1) indicating if the sale was promotional (1) or not (0).

## Preprocessing

- The `date` column is converted to datetime format, and the year, month, and day are extracted to facilitate analysis.
- Categorical features `location` and `product_type` are encoded using Label Encoder.
- The original categorical columns are dropped, and a new `promotion_label` column is created to represent whether the sale is promotional or not (Non-Promotional or Promotional).

## Model Training and Evaluation

- The dataset is split into training and testing sets using a test size of 20% and a random state of 42.
- A Gradient Boosting Regressor model is trained on the training data and evaluated on the test data using Mean Squared Error (MSE), Mean Absolute Error (MAE), and R-squared (R2) metrics.

## Hyperparameter Tuning

- GridSearchCV is used to perform hyperparameter tuning for the Gradient Boosting Regressor model. The hyperparameters `n_estimators` and `learning_rate` are explored with various values.
- The best model obtained from GridSearchCV is then evaluated using cross-validation to compute the mean cross-validation MSE.

## Data Visualization

- Several data visualizations are created to gain insights into the data:
  - Bar plots showing the total sales for non-promotional and promotional sales by product type.
  - Bar plot comparing the quantity sold for each product type in promotional and non-promotional sales.
  - Line plot showing the time series analysis of total sales with promotion label.
  - Seasonal decomposition plot of total sales.
  - Correlation matrix heatmap between features and total sales.
  - Pairplot for selected features.

## How to Use

1. Clone the repository.
2. Install the required libraries by running `pip install -r requirements.txt`.
3. Place the `promotional_sales_data.csv` file in the appropriate directory.
4. Run the `main.py` script, and the results and visualizations will be displayed in the console and matplotlib figures.

Feel free to modify and experiment with the code to explore more insights from the data.

Happy coding!

