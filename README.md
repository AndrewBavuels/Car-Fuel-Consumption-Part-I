# **Car Fuel Consumption Part I - Analysis and Predictions 🚗📈🔮**

This is the first part of a project series to show a case in which I will apply **advanced analytics,** involving data visualization and **predictions with Machine Learning,** regarding Car Fuel Consumption.

![Let's Get the Party Started](https://media.giphy.com/media/lNGyr4FWfRO8S8LARn/giphy.gif)


## 1. Project description 👇
 
### _Part I: Exploratory Data Analysis (EDA) Visualization with Python._

For this project, I used a "Car Fuel Consumption per gas fuel type" dataset from [Kaggle](https://www.kaggle.com/datasets/anderas/car-consume/). From the Kaggle Dataset context, there are 4 questions formulated:

- **Question #1:** Which gas type consumes the most? E10 or SP98?
- **Question #2:** How much is the consume?
- **Question #3:** It consumes 0.4 liters more with E10 gas, isn't it?
- **Question #4:** Which of the two fuels is cheaper, E10 or SP 98?

"_All these questions are answered in the notebook of this repository._"

![Driving Fast And Furious GIF by The Fast Saga](https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExcmtkcHMzbTJsODltamZtaDFhN3cxM2d6OTRncWVtYng3OWtkOGIzdSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/2EWa4uTH39d2NTJRGy/giphy.gif)

### Exploratory Data Analysis => Summary:

- **Performing data maintenance or cleaning:** Duplicates, null-values, outliers
- **String operations:** Normalize to lowercase, replacing numbers to categorical and vice-versa
- **Feature Engineering:** Merging features, such as 'consumption rate' based on distance and consumed gas
- **Relational model transformation:** For future project steps
- **Answering questions from our Exploratory Data Analysis:** The main goal of this repository

### Highlights:

### Question #1: Which gas type consumes the most? E10 or SP98?

![question_1](https://github.com/AndrewBavuels/Car-Fuel-Consumption-Part-I/blob/main/images/question_1.png)

We can observe the **consume rate (liter per kms),** regarding the car speed records, is **higher** for the gas type **SP98**

### Question #2: How much is the consumption?

#### Code Snippet:

![question_2](https://github.com/AndrewBavuels/Car-Fuel-Consumption-Part-I/blob/main/images/question_2.png)

#### Stats Overview

| gas_type | count | mean     | std      | min  | 25%    | 50%    | 75%    | max  |
|----------|-------|----------|----------|------|--------|--------|--------|------|
| E10      | 138.0 | 0.304058 | 0.125085 | 0.04 | 0.22   | 0.295  | 0.3975 | 0.68 |
| SP98     | 197.0 | 0.321421 | 0.126652 | 0.09 | 0.24   | 0.310  | 0.4000 | 0.73 |

#### Mean Analysis

| gas_type | consume_rate |   speed   |
|----------|--------------|-----------|
| E10      |   0.304058   | 43.289855 |
| SP98     |   0.321421   | 41.497462 |

#### Median Analysis

| gas_type | consume_rate |   speed   |
|----------|--------------|-----------|
| E10      |      0.295   |    42.0   |
| SP98     |      0.310   |    41.0   |


- **E10** has a **mean consumption rate** of 0.304 and a **median** of 0.295.
- **SP98** has a **mean consumption rate** of 0.321 and a **median** of 0.310.
  

Both gas types show similar patterns in terms of distribution and spread **(std)**, with **SP98 having a slightly higher average consumption rate** compared to E10.

### Question #3: It consumes 0.4 liters more with E10 gas, isn't it?

Here is the reason why I created a **relational-ish table df**:

#### Code Snippet:

![question_3.1](https://github.com/AndrewBavuels/Car-Fuel-Consumption-Part-I/blob/main/images/question_3.1.png)

I am showing in the previous image, the merge of the gas consumption records to the treated dataset, in order to figure out if E10 is consumed 0.4 liters more than SP98. **Now, with a groupby, I am getting the mean and the median for such consumptions:**

#### Mean Analysis

| gas_type | consume |
|----------|---------|
| E10      | 4.781159|
| SP98     | 4.668020|

#### Code Snippet:

![question_3.2](https://github.com/AndrewBavuels/Car-Fuel-Consumption-Part-I/blob/main/images/question_3.2.png)

#### Median Analysis

| gas_type | consume |
|----------|---------|
| E10      | 4.7     |
| SP98     | 4.6     |

#### Code Snippet:

![question_3.3](https://github.com/AndrewBavuels/Car-Fuel-Consumption-Part-I/blob/main/images/question_3.3.png)


It consumes 0.4 liters more with E10 gas, isn't it? **The answer is Not necessarily.**

It depended on the number of experiments per gas type. That is why I did the Feature Engineering in the first place,
to mean creating the column **'consume_rate'** to be accurate in telling **which gas type consumes the most.**

### Question #4: Which of the two fuels is cheaper, E10 or SP 98?

From the Kaggle Dataset context:

- **E10** is sold for **€ 1.38**
- **SP98** is sold for **€ 1.46**

#### Code Snippet:

![question_4](https://github.com/AndrewBavuels/Car-Fuel-Consumption-Part-I/blob/main/images/question_4.png)

#### Comparative Price Analysis between E10 and SP98

In this analysis, we compare the mean and median prices paid for two types of gasoline: E10 and SP98.

#### Mean Price

The mean price is the average of all prices paid for each type of gasoline. Here are the results:

- **Mean price of E10**: 6.598
- **Mean price of SP98**: 6.815

This means that, on average, the price paid for E10 is lower than the price paid for SP98.

**Is E10 cheaper than SP98?** Yes, on average, E10 is cheaper than SP98.

#### Median Price

The median price is the middle value in a set of data when it is ordered from lowest to highest. Here are the results:

- **Median price of E10**: 6.486
- **Median price of SP98**: 6.716

This means that if we order all the prices paid for each type of gasoline, the central value for E10 is lower than the central value for SP98.

**Is E10 cheaper than SP98?** Yes, according to the median prices, E10 is cheaper than SP98.

### Conclusion

Both the mean and median price analyses indicate that **E10 is generally cheaper than SP98.** This information can be useful for consumers looking for more economical options when choosing the type of gasoline for their vehicles.

After this Exploratory Data analysis, **the next experiment will be Machine Learning training models for Gas Consumption predictions.** We export the 'pre-processed' dataset as follows:


## **2. Technology stack 💻**

### Programming language:
- [Python](https://docs.python.org/3/)

### Python Libraries:
- [pandas](https://pandas.pydata.org/docs/reference/frame.html): For data manipulation and analysis.
- [numpy](https://numpy.org/doc/stable/): For mathematical operations and array manipulation.
- [matplotlib.pyplot](https://matplotlib.org/stable/contents.html): For data visualization.
- [seaborn](https://seaborn.pydata.org/): For statistical data visualization.
- [re](https://docs.python.org/3/library/re.html): For regular expression operations.
- [scipy](https://docs.scipy.org/doc/scipy-1.12.0/reference/generated/scipy.stats.skewnorm.html): For scientific and technical computing.




#### Distribution platform
- [Anaconda](https://www.anaconda.com/)

#### Computing environment
- [Jupyter Notebooks](https://jupyter.org/)

## **3. Folder structure 📁**
```
└── project
    ├── data
    │   ├── raw
    │   │   └── measurements.csv
    │   └── pre_processed
    │   │   └── pre_processed_gas_df.csv
    ├── notebooks
    │   └── main.ipynb
    └── README.md    
```
## **4. Next steps 💡**

#### Predictions

- Do you have any hypothesis?
- Can you make any kind of prediction: regression and/or classification?


#### Enriching the dataset

- Obtain related data by web scraping or with APIs.

#### Database

- Load the processed information into a database

###  **Contact info📧**
For further information, reach me at andres.buelvas.diago.01@gmail.com
