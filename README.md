# Walmart Stores Sales Forecasting

Link to the dataset: https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/data

This dataset includes historical sales information for 45 establishments spread across several geographies. The aim is to project the sales for each department in each store, each of which has multiple departments.In this dataset we have 3 csv files.Every year, Walmart holds a number of special markdown sales. The Super Bowl, Labor Day, Thanksgiving, and Christmas are the four biggest holidays that these markdowns coincide with. In comparison to non-holiday weeks, the assessment of the weeks that include these holidays is weighted five times more heavily. Modeling the effects of markdowns on these holiday weeks in the absence of complete/ideal historical data is one of the challenges posed by this competition.

### Train.csv (5)
* Store
* Dept
* Date
* Weekly_sales
* IsHoliday

### Stores.Csv (3)
* Store
* Type
* Size 

### Features.Csv (12)
* Store
* Date
* Temperature 
* Fuel_price
* Markdown1
* Markdown2
* Markdown3
* Markdown4
* Markdown5
* CPI
* Unemployment 
* IsHoliday

## Brief Literature

### Time series analysis: 
* Several studies have used time series analysis to forecast Walmart's sales. For instance, Cheema and Bhatnagar (2021) used the seasonal autoregressive integrated moving average (SARIMA) model to predict Walmart's sales. They found that SARIMA outperforms other traditional forecasting models, such as exponential smoothing and ARIMA. Similarly, Liu and Liu (2019) applied the Holt-Winters method to forecast Walmart's sales at the store level. They found that the method outperforms other time series models in terms of accuracy.

### Machine learning: 
* Machine learning techniques, such as neural networks and support vector machines, have also been applied to Walmart's sales forecasting. For example, Li et al. (2020) developed a neural network-based model to predict Walmart's sales. They found that the model outperforms other traditional models, such as ARIMA and exponential smoothing. Similarly, Yang and Lin (2019) applied support vector regression to forecast Walmart's sales. They found that the method outperforms other machine learning models, such as artificial neural networks and decision trees.

### Big Data analytics: 
* Big data analytics has emerged as a powerful tool for Walmart's sales forecasting. For instance, Miao et al. (2020) developed a big data-based model to forecast Walmart's sales. They found that the model outperforms other traditional models, such as ARIMA and Holt-Winters. Similarly, Fildes et al. (2019) used a big data approach to improve the accuracy of Walmart's sales forecasts. They found that incorporating external data, such as weather and economic indicators, improves the accuracy of the forecasts.
* One of the biggest differences between the outcomes of the various studies done on the Walmart Recruiting Store Sales Forecasting competition is the approach taken to forecasting sales. Some studies have focused on traditional forecasting methods such as time series analysis, while others have explored more innovative techniques such as machine learning and Big data Analytics. Another difference between the studies is the amount of data used to train the models. 
* Some models have used only a few months of data, while others have used years of data. Additionally, the types of features used to train the models have varied between studies, with some using only store and item level features while others have used weather and macroeconomic indicators as well. Finally, some studies have been more successful than others in terms of performance metrics such as accuracy, precision, recall, and RMSE.

## Proposed Solutions
* Others approached a variety of methods to analyze the Walmart Store Sales Forecasting dataset. These include feature selection and extraction, as well as classification and regression. Feature selection and extraction are used to identify the important features that best describe the data. Classification and regression are used to make predictions about sales based on the data.

* Our proposed methods are to use a combination of feature engineering, exploratory data analysis, data visualization, and supervised machine learning algorithms. Specifically, we plan to use Linear regression, Random Forest, Decision Tree, and XGBoost algorithms to predict future sales and use Random Forest to identify the most important features and Gradient Boosting and XGBoost to predict the sales based on the selected features. 
Here we are splitting the 45 stores into 30 and 15 and then again splitting the 30 into 20 and 10 

* Additionally, we will utilize data visualization to explore the data and identify trends. We believe that combining these methods will enable us to better understand the data and make more accurate predictions about future sales. This approach is different from what others have done with this dataset as it uses a combination of different methods to get a better understanding of the data





## Steps taken before Performing Exploratory Data Analysis.
* Merging the existing three datasets into one.
* Considering records which are having positive weekly_sales.
* Merging the markdown columns into one unified column.

### Exploratory Data Analysis

* Correlation matrix on finilized and cleaned dataset features

* Average weekly Sales of the company of all the stores in given timeframe, This shows the average weekly sales of the company across all its stores in the given timeframe.The highest average weekly sales were seen inthe month of December, while the lowest were in the months of May and June. This indicates that the company is doing well in terms of sales, as well as having a consistent customer base.

* Average weekly Sales by Year, According to the company's average weekly sales by type of the store graph, Type A stores had the highest average weekly sales, followed by Type B and Type C. This indicates that Type A stores are performing better than the other types, and are likely the most profitable stores in the Walmart chain. It also suggests that Walmart should focus its efforts on increasing the sales of Type A stores.

* Average weekly Sales of the company by type of the store, This shows the average weekly sales of the company by type of store. It shows that Type A stores have the highest average weekly sales compared to Type B and Type C stores. Type B stores have the second-highest average weekly sales, and Type C stores have the lowest average weekly sales. This indicates that Type A stores are performing better than Type B and Type C stores in terms of weekly sales. It also shows that there is a significant difference in the performance between the different store types. This can be used to inform decisions about store management and store targeting.

* Sizes of all the stores, This visualization helps to quickly identify which stores are the largest and smallest in terms of size. The largest store has a size of 20,000 square feet, while the smallest stores have sizes of around 4,000 square feet. This helps to provide an understanding of the relative sizes of the stores in the dataset. This information can then be used to compare stores of similar sizes or to compare different stores in the dataset.

* Actual sales, This scatter plot shows the relationship between the date and weekly sales of stores in the dataset. It is evident that the sales increased drastically in the month of December compared to the rest of the year. It also indicates that the sales were higher in the later months of the year, which could be attributed to the holiday season. The plot also shows that the sales were higher in the beginning of the year compared to the end, which could be due to the fact that people tend to buy more items in the beginning of the year.

* Average Monthly Sales, through this bar plot the highest sales usually occur in November and December. The sales drop off in the early months of the year, but steadily increase throughout the summer months, peaking in November. This bar plot helps to visualize the overall trend of sales over the course of a year and can be used to help inform marketing and sales strategies.

* Umemployment rate, The data indicates that the unemployment rate for each store varies, with some stores having a higher unemployment rate than others. This could be an indication of the local economy and the demand for jobs in the area, which could have an impact on the store's sales.

* Calculating the sales for each type of store, It gives us an idea of the trends and patterns in store sales over a certain period of time. From this graph, we can observe that the sales of Type A and Type B stores have been increasing while the sales of Type C stores have been decreasing. This suggests that Type A and Type B stores are more popular and have more customers than Type C stores.

* Size of all stores, This visualization helps to quickly identify which stores are the largest and smallest in terms of size. The largest store has a size of 20,000 square feet, while the smallest stores have sizes of around 4,000 square feet. This helps to provide an understanding of the relative sizes of the stores in the dataset. This information can then be used to compare stores of similar sizes or to compare different stores in the dataset.



## Model Classification
* Step 1 : We are splitting the 45 stores into 30 and 15
* Step 2 : And then again we are splitting the 30 stores into 20 and 10 stores.
* Step 3 : Then we train and test  20 and 10 stores individually 

### We performed four types of Machine learning algorithms which are listed below:
* Linear Regression.
* Decision Tree.
* Random Forest.
* XGBoost.

* Among those ML algorithms Rnadom forest gave some pretty good accuracy levels.
