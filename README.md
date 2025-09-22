# Vendor_performance_project
# File 1: Importing_data_to_database&DataCleaning.ipynb

This file focuses on the data preparation steps. The main performance points are:

Data Consolidation: The notebook imports vendor information from various tables, including Purchases, Purchase_Prices, Vendor_Invoice, and Sales, into a single final summary table.

Data Cleaning and Transformation:

It calculates ProfitMargin, stockturnover, and salestopurchaseratio.

It also handles data cleaning by replacing inf and -inf values with a large number (1e300) to enable successful database import.

# File 2: analysis.ipynb

This file uses the cleaned data to perform a deeper performance analysis. The key findings are:

Overall Performance Metrics: The analysis of 10,692 records reveals an average ProfitMargin of approximately -15.6%, which indicates a significant net loss. The median ProfitMargin is 30.4%.

Vendor Performance Analysis:

A statistical t-test was conducted to compare the mean profit margins of top-performing and low-performing vendors.

The test result shows a t-statistic of -17.64 and a p-value of 0.0000.

Conclusion: Based on the low p-value (less than 0.05), the null hypothesis—that there is no significant difference in the mean profit margins between the two groups—is rejected. This confirms a statistically significant difference in performance between the top and low-performing vendor groups.







