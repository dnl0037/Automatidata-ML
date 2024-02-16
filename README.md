# Project: New York City Taxi Fare Prediction

The New York City Taxi and Limousine Commission seeks a way to utilize the data collected from the New York City area to predict the fare amount for taxi cab rides. The project comprises five notebooks, each focusing on a different aspect of the data analysis process.

- Notebook 1 - Inspect and Analyze Data: Investigates and understands the provided taxi cab dataset, including creating a pandas dataframe, performing a cursory inspection, and compiling summary information about the data.

- Notebook 2 - Exploratory Data Analysis: Conducts exploratory data analysis on the dataset, including data cleaning, building visualizations, and evaluating and sharing results.

- Notebook 3 - Hypothesis Testing: Demonstrates knowledge of hypothesis testing by analyzing whether there is a relationship between payment type and fare amount, using descriptive statistics and hypothesis testing in Python.

- Notebook 4 - Multiple Linear Regression Model: Builds a multiple linear regression model to predict fare amount, evaluating model performance and interpreting results.

- Notebook 5 - Random Forest and XGBoost Models: Implements Random Forest and XGBoost models to predict whether a customer is a generous tipper, considering ethical implications and recommending adjustments to the model objective if necessary.

Each notebook plays a crucial role in understanding the data, conducting analysis, building models, and providing insights regarding fare prediction and customer tipping behavior in New York City taxi cab rides.

# Notebook 1: Data Inspection and Analysis

### Data Overview
![Data Overview](images/1.png)

- The `fare_amount` values exhibit a wide range, including negative values, indicating potential data errors.
- Similarly, the `tip` column contains extremely high values, which may also be erroneous.
- Trip distances vary, with most rides falling within the 1-3 mile range, but some outliers extend beyond 33 miles.

### Data Quality Issues
![Data Quality Issues](images/2.png)

- Errors are evident in the data, as indicated by negative `total_amount` values, suggesting potential data entry mistakes.

### Insights

- Key variables for building a predictive model for taxi fare include `total_amount` and `trip_distance`, which provide insights into the nature of taxi rides.
