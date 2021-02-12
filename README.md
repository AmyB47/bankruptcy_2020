# Predicting Bankruptcies of Large Public U.S. Companies

**Description**

It’s come to light that companies who filed for bankruptcy in 2020 were having financial struggles before the COVID pandemic, but was it  predictable these companies would file?  This project fit a classification algorithm to predict the 2020 bankruptcy filings of U.S. public companies who had over $100 Million in Assets. 

**Features and Target Variables**

Target: Bankruptcy filing within one year of annual financial report

Features:

| From Financial Reports                | Calculated Features                                       | Industry Divisions                       |
| ------------------------------------------------ | ----------------------------------------------------- | -------------------------------------------------- |
| Assets                     | Debt ratio                                                 | Agriculture, Forestry and Fishing        |
| Assets Current             | Debt equity ratio                                            | Mining                                   |
| Liabilities                | Current ratio                                                | Construction                                                 |
| Liabilities Current        | Leverage                                                     | Manufacturing                                                |
| Net Income/Loss            | Return on equity                                             | Transportation, Communications, Electric,</br> Gas and Sanitary service |
| Stockholders Equity        | Return on assets                                             | Wholesale Trade                                              |
| Operating Income Loss      | Gross profitability ratio                                    | Retail Trade                                                 |
| Earnings Per Share Diluted | For all calculated  ratios, deviation <br>from industry division | Finance, Insurance and Real Estate                           |
|                            |                                                              | Services                                                     |



**Data Sources**

* U.S. Securities and Exchange Commission (SEC) annual financial 10-K and 10-K/A report filings from public companies. To obtain all reports filed for fiscal years ending 2014-2019, had to pull reports submitted to this regulatory agency through 2020 Q3. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2014Q1 - 2019Q3, Google Public Cloud U.S. SEC Public Dataset

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2019Q4 - 2020Q3, [U.S. SEC Financial Statement Data Sets](https://www.sec.gov/dera/data/financial-statement-data-sets.html)

* [U.S. SEC EDGAR](https://www.sec.gov/edgar.shtml) filings search

* SIC Code industry names and industry division ranges available from [Wikipedia](https://en.wikipedia.org/wiki/Standard_Industrial_Classification) 

* [UCLA-LoPucki Bankruptcy Research Database](https://lopucki.law.ucla.edu/spreadsheet.htm)


**Tools**

* Google Cloud Platform

* U.S. Securities and Exchange Commission EDGAR filings search

* PostgresSQL  

* Python

Python packages:

* SQLAlchemy
* Psycopg2
* Pandas 
* Numpy
* Pickle
* Requests
* BeautifulSoup
* Matplotlib
* Seaborn
* SciPy
* Ibmlearn
* SciKit-Learn
