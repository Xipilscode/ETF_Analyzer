# ETF Analyzer

The ETF Analyzer is a web application designed to facilitate financial data analysis, focusing on Exchange-Traded Funds (ETFs). Leveraging a robust set of technologies, this tool provides detailed insights into individual asset performance and overall portfolio returns. Users can analyze historical data, perform advanced SQL queries, and visualize results through interactive plots, making it an invaluable resource for financial analysts and data scientists.

### Table of Contents

- [Technologies](#technologies)
- [Installation](#installation)
- [Instructions](#instructions)
- [Contributors](#contributors)
- [License](#license)

### Technologies

This application incorporates a variety of technologies and libraries:

* Python: A versatile high-level programming language that is easy-to-read and powerful, making it great for data analysis.

* SQL: A standard language for managing and manipulating databases. We utilize SQL to interact with our SQLite database.

* SQLite: A database management system based on SQL. SQLite is lightweight and very convenient for small applications like ours.

* Pandas: A library providing high-performance, easy-to-use data structures and data analysis tools for Python.

* hvPlot: A high-level plotting API for the PyData ecosystem built on HoloViews. The interactivity of HvPlot is used to better visualize the daily and cumulative returns of the assets.

* Voilà: A Python library that turns Jupyter notebooks into standalone web applications. We use Voilà to deploy our Jupyter notebook as an interactive web application.

### Installation

To set up this project, ensure you have Python installed (preferably Python 3.8 or later). Additionally, you need SQL and SQLite for database functionalities. The following Python libraries are required: Pandas, hvPlot, and Voilà.

Install these libraries using pip:
```
pip install pandas hvplot voila
```

### Instructions

The ETF Analyzer performs a series of steps to analyze financial data:

1. Analyzing a Single Asset in the ETF: The application reads PYPL data from the database, inspects it, and creates interactive visualizations of daily and cumulative returns.

2. Optimizing Data Access with Advanced SQL Queries: The application performs advanced SQL queries to filter specific data more efficiently, including dates with PYPL's closing prices greater than 200 and the top 10 daily returns for PYPL.

3. Analyzing the ETF Portfolio: The ETF portfolio is built by combining all the data for each asset using SQL joins. Then the performance of this portfolio is evaluated by creating a DataFrame that averages the daily returns for all four assets.

4. Calculating Annualized and Cumulative Returns: The average daily returns in the `etf_portfolio_returns` DataFrame are used to calculate both the annualized and cumulative returns of the portfolio.

5. Deploying the Notebook as a Web Application: The notebook is deployed as a web application using the Voilà library. Screen recording demonstrating the appearance of the web application when deployed locally is included in the repository.

#### Deploying the Notebook: 

![Deploying the Notebook](deploying_notebook.gif)


### Contributors

Alexander Likhachev

### License
MIT