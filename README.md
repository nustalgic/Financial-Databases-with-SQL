# ETF Analyzer

Module 7 Challenge

[![7-4-challenge-image.png](https://i.postimg.cc/Y0L3n2PV/7-4-challenge-image.png)](https://postimg.cc/sGy71zs9)

# Background

In recent years, finance has had an explosion in passive investing. Passive investing means that you invest in a basket of assets that’s called an exchange-traded fund (ETF). This way, you don’t spend time researching individual stocks or companies or take the risk of investing in a single stock. ETFs offer more diversification.

In this Challenge assignment, I’ll build a financial database and web application by using SQL, Python, and the Voilà library to analyze the performance of a hypothetical fintech ETF.

---

## Technologies

The data we're analyzing comes from a jupyter notebook that we've created and imported files to. We'll be using Python to run and read our data. 

* [jupyter] - (https://github.com/jupyter/notebook) - Helps us run our code and get the information we need from the data listed in csv files.


---

## Installation Guide

In order for us to get the data we need we must import pandas, plots and the csv files we want to observe.

```python
# Importing the required libraries and dependencies
import numpy as np
import pandas as pd
import hvplot.pandas
import sqlalchemy
```

---

## Usage

To find the information needed we build a jupyter notebook and run various functions to pull the data from csv files.

```python
# Write a SQL SELECT statement to select the time and daily_returns columns

# Sort the results in descending order and return only the top 10 return values

query = """
SELECT time, close
FROM PYPL
ORDER BY daily_returns DESC
LIMIT 10;
"""

# Using the query, read the data from the database into a Pandas DataFrame

pypl_top_10_returns = pd.read_sql(query, con=engine)

# Review the resulting DataFrame

display(pypl_top_10_returns.head())

```
---
## Notebook deployed as a Web Application

Screen Recording on [Loom](https://www.loom.com/share/f0aae8105a0544d48f1ffd6841658481)

[![Screen-Shot-2022-02-20-at-8-52-48-PM.png](https://i.postimg.cc/7YYP2Cpm/Screen-Shot-2022-02-20-at-8-52-48-PM.png)](https://postimg.cc/7bdyvLP2)


---

## Contributors

Brought to you by Elgin Braggs Jr.

---

## License

MIT