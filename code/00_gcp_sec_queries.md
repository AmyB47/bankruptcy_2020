

The U.S Securities and Exchange Commission (SEC) has a public dataset in Google Cloud Platform. Company annual financial report data for 2014 through 2019 Q3 were obtained from this source.  Data for 2019 Q4 was obtained with data file downloads from the SEC public website. 

These are a few of the queries run to explore the Google Cloud Platform SEC public dataset.  The last query was run for each year 2014 - 2019 to download the data in CSV files which I then added as tables to a locally saved PostgreSQL database. 

To examine the total number of different companies that submitted a 10-K annual report to the SEC:  

![gcp_by_year](../GCP_queries/gcp_sec_by_year.png)



To examine most commonly provided measures: 

![gcp_by_measure_tag](../GCP_queries/gcp_sec_measure_tags.png)



To see all the measurement tags containing Inventory.  Similar queries done for other measures including, but not limited to, Assets, Liabilities, and Revenue. 

![inventory_search](../GCP_queries/gcp_sec_inventory_search.png)



To query for one specific company and type of measure: 

![company_measure_search](../GCP_queries/gcp_sec_company_measure_search.png)



This query was run for each year 2014-2019:

```sql
SELECT *

FROM
bigquery-public-data.sec_quarterly_financials.quick_summary

WHERE form in ('10-K' , '10-K/A') 
 and SUBSTR(period_end_date,1,4) = '2014'
 and measure_tag in ('Assets' 
,'CurrentAsset'
,'AssetsCurrent'
,'TotalAsset'
,'Liabilities'
,'LiabilitiesCurrent'
,'CashAndCashEquivalentsAtCarryingValue'
,'EarningsPerShareDiluted'
,'EarningsPerShareBasic'
,'RepaymentsOfLongTermDebt'
,'LongTermDebt'
,'LongTermDebtCurrent'
,'LongTermDebtNoncurrent'
,'LongTermDebtMaturitiesRepaymentsOfPrincipalInNextTwelveMonths'
,'DeferredIncomeTaxExpenseBenefit'
,'DeferredIncomeTaxLiabilities'
,'DeferredIncomeTaxesAndTaxCredits'
,'DeferredIncomeTaxLiabilitiesNet'
,'Revenues'
,'SalesRevenueNet'
,'SalesRevenueGoodsNet'
,'OperatingIncomeLoss'
,'OperatingExpenses'
,'CostsAndExpenses'
,'NetIncomeLoss'
,'OperatingIncomeLoss'
,'GrossProfit'
,'ProfitLoss'
,'CashAndCashEquivalentsAtCarryingValue'
,'NetCashProvidedByUsedInOperatingActivities'
,'NetCashProvidedByUsedInFinancingActivities'
,'NetCashProvidedByUsedInInvestingActivities'
,'StockholdersEquity'
,'CashAndCashEquivalentsPeriodIncreaseDecrease'
,'LiabilitiesAndStockholdersEquity'
,'CommonStockValue'
,'Depreciation'
,'InterestExpense'
,'Goodwill'
,'WorkingCapital'
,'IncreaseDecreaseInInventories'
,'InventoryNet'

);

```

