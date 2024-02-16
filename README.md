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


# Notebook 2: Exploratory Data Analysis (EDA)

### Trip Characteristics Analysis
![Trip Characteristics Analysis](images/3.png)

- **Insights**: The majority of trips were short journeys of less than two miles, with a steep decline in the number of trips as distance traveled increases. This suggests that most taxi rides in the dataset were relatively short in duration.

<table>
  <tr>
    <td><img src="images/4.png" alt="Insights1"></td>
    <td><img src="images/5.png" alt="Insights2"></td>
  </tr>
</table>


- **Distribution Analysis**: Both the total cost and tip amount distributions are right-skewed, with most costs falling in the $5-15 range and nearly all tips in the $0-3 range. There are no significant differences in tip distributions between vendors, even at higher tip amounts.

### Passenger Count and Ride Frequency

<table>
  <tr>
    <td><img src="images/6.png" alt="Passenger Count1"></td>
    <td><img src="images/7.png" alt="Passenger Count2"></td>
  </tr>
</table>


- **Findings**: Most rides were single occupancy, with nearly 3% of rides having as many as six passengers. However, there were also 33 rides with a passenger count of zero, which is unusual and may need further investigation.

![Trip Characteristics Analysis](images/8.png)
- **Tip Amount Variation**: Mean tip amount varies minimally by passenger count, although there is a slight drop for four-passenger rides. This drop is expected given the lower frequency of rides with four passengers.

### Temporal Analysis

![Daily and Monthly Ride Patterns](images/9.png)

- **Daily and Monthly Ride Patterns**: Wednesday through Saturday saw the highest number of daily rides, while Sunday and Monday had the fewest. Thursday had the highest gross revenue, despite having only slightly more rides than Saturday.

![Seasonal Trends](images/10.png)

- **Seasonal Trends**: Monthly rides and revenue follow consistent patterns, with notable dips in the summer months (July, August, September) and one in February.

### Geographic Analysis

<table>
  <tr>
    <td><img src="images/11.png" alt="Location Density1"></td>
    <td><img src="images/12.png" alt="Location Density2"></td>
  </tr>
</table>


- **Location Density**: Drop-off locations exhibit a characteristic curve related to the cumulative density function of a normal distribution, indicating relatively even distribution across terrain. However, a disproportionate number of locations receive the majority of traffic, likely near popular tourist attractions, airports, and transportation terminals.

### Limitations and Further Investigation

- **Data Limitations**: The dataset lacks geographic coordinates for drop-off locations, limiting the ability to analyze location-specific patterns.
- **Opportunities for Further Analysis**: Investigating the reason behind rides with zero passengers and exploring the specific locations corresponding to high-traffic drop-off points could provide valuable insights into taxi ride patterns in the New York City area.

This exploratory analysis provides a comprehensive understanding of the characteristics and patterns within the taxi ride dataset, laying the groundwork for further analysis and modeling in subsequent notebooks.
