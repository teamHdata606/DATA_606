## Walmart Stores Sales Forecasting

Link to the dataset: https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/data

This dataset includes historical sales information for 45 establishments spread across several geographies. The aim is to project the sales for each department in each store, each of which has multiple departments.In this dataset we have 3 csv files.Every year, Walmart holds a number of special markdown sales. The Super Bowl, Labor Day, Thanksgiving, and Christmas are the four biggest holidays that these markdowns coincide with. In comparison to non-holiday weeks, the assessment of the weeks that include these holidays is weighted five times more heavily. Modeling the effects of markdowns on these holiday weeks in the absence of complete/ideal historical data is one of the challenges posed by this competition.

Train.csv (5)
Store
Dept
Date
Weekly_sales
IsHoliday

Stores.Csv (3)
Store
Type
Size 

Features.Csv (12)
Store
Date
Temperature 
Fuel_price
Markdown1
Markdown2
Markdown3
Markdown4
Markdown5
CPI
Unemployment 
IsHoliday


### Steps taken before Performing Eexploratory Data Analysis.
* Merging the existing three datasets into one.
* Considering records which are having positive weekly_sales.
* Merging the markdown columns into one unified column.

### Model Classification
* Step 1 : We are splitting the 45 stores into 30 and 15
* Step 2 : And then again we are splitting the 30 stores into 20 and 10 stores.
* Step 3 : Then we train and test  20 and 10 stores individually 

#### We performed four types of Machine learning algorithms which are listed below:
* Linear Regression.
* Decision Tree.
* Random Forest.
* XGBoost.

* Among those ML algorithms Rnadom forest gave some pretty good accuracy levels.
