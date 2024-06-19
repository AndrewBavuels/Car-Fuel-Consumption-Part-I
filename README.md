# **Car Fuel Consumption Part I - Analysis and Predictions 🚗📈🔮**

The goal for this project was to be more prepared for the next technical assessment as part of a selection process. Once more, I want to show a case in which I will apply **advanced analytics** involving **data visualization** and **predictions with machine learning** regarding Car Fuel Consumption.

![Let's Get the Party Started](https://media.giphy.com/media/lNGyr4FWfRO8S8LARn/giphy.gif)


## 1. Project description 👇
 
### _Part I: Exploratory Data Analysis (EDA) Visualization with Python._

For this project, I used a "Car Fuel Consumption" dataset from [Kaggle](https://www.kaggle.com/datasets/anderas/car-consume/). 
First, I am going to get insights into the current status about how much is the consumption per gas fuel type. After the data cleaning process...

- Question #1: Which gas type consumes the most? E10 or SP98?
- Question #2: How much is the consumption?
- Question #3: It consumes 0.4 liters more with E10 gas, isn't it?
- Question #4: Which of the two fuels is cheaper, E10 or SP 98?


![Driving Fast And Furious GIF by The Fast Saga](https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExcmtkcHMzbTJsODltamZtaDFhN3cxM2d6OTRncWVtYng3OWtkOGIzdSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/2EWa4uTH39d2NTJRGy/giphy.gif)

### I. Exploratory Data Analysis (EDA)

Here is a little extract from Jupyter Notebook, using Python and their libraries (described down in the Technology Stack section).

![EDA_with_Python](https://github.com/AndrewBavuels/Sales-and-Business-Report-with-Microsoft-Power-BI/blob/main/images/EDA%20with%20Python.png)

Remember when I first detected the **outliers** in the Power BI visualization? Well, this is the part and I am performing their handling per each **customer segment**



The EDA execution will depend on the specific needs of your data analysis. Mostly, those key moments happen when:

- Feature Engineering.
- Relational model to answer questions.
- Developing new analyses or reports.
- Modifying the data structure.
- Performing data maintenance or cleaning.

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


## **3. Report Demo 📊📈📉**

To show what it looks like in action, [click here](https://github.com/AndrewBavuels/Sales-and-Business-Report-with-Microsoft-Power-BI/blob/main/report/Dunder%20Mifflin%20Sales%20Report.pbix).
> **_Note:_** The demo is also contained in the **report** folder.

## **4. Folder structure 📁**
```
└── project
    ├── architecture
    │   └── Dunder Mifflin data pipeline.png
    ├── data
    │   ├── raw
    │   │   ├── DIM sku.xlsx
    │   │   ├── DIM state_branches.xlsx
    │   │   └── FACT sales.xlsx
    │   ├── processed
    │   │   └── FACT sales.xlsx
    │   └── ready
    │       └── sales.xlsx
    ├── notebooks
    │   └── main.ipynb
    ├── report
    │   └── Dunder Mifflin Sales Report.pbix
    └── README.md    
```
## **6. Next steps 💡**

- Develop an action plan to address problem areas identified in the 80-20
- Establish a multidisciplinary team with clearly defined roles to address the problem areas identified in the 80-20
***
- Automate the connection with new data in the reporting system
- Integrate other data formats such as MySQL, PostgreSQL, JSON, XML

###  **Contact info📧**
For further information, reach me at andres.buelvas.diago.01@gmail.com
