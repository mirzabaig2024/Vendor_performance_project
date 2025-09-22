# Vendor Performance Analysis
This project provides a comprehensive analysis of vendor performance by integrating and cleaning data from multiple sources. It uses statistical methods and data visualization to identify and evaluate key performance indicators, ultimately distinguishing between top-performing and low-performing vendors.

# Project Goal
The primary objective is to analyze vendor performance by:

Consolidating data from various sources (Purchases, Sales, Prices).

Calculating key metrics such as ProfitMargin, stockturnover, and salestopurchaseratio.

Using statistical analysis (t-test) and data visualization to find significant differences in performance between different vendor groups.

# Project Files
This repository contains two main Jupyter Notebooks that guide you through the entire analysis pipeline.

1. Importing_data_to_database&DataCleaning.ipynb:
   
  * This notebook handles the initial data engineering and cleaning. The main steps performed are:
  
  * Connecting to a MySQL database to import raw data.
  
  *  Merging various vendor-related tables (Purchases, Purchase_Prices, Vendor_Invoice, Sales) into a single, comprehensive DataFrame.
  
  * Feature engineering to create new columns like ProfitMargin, stockturnover, and salestopurchaseratio.
  
  * Data cleaning, specifically replacing inf and -inf values with a large number (1e300) to ensure data integrity before importing into the database.
  
  * Exporting the final, cleaned DataFrame to a new table in the MySQL database.

2. analysis.ipynb:
   
  * This notebook focuses on the statistical and visual analysis of the cleaned data. The key components include:
  
  * Importing the final, cleaned data from the MySQL database.
  
  * Calculating summary statistics and overall performance metrics.
  
  * Performing a t-test to determine if there is a statistically significant difference in ProfitMargin between top-performing and low-performing vendor groups.
  
  * Generating various plots to visualize the data, such as box plots showing the impact of order size on unit price and bar plots to visualize vendor contribution margins.

# Key Findings
* Based on the analysis, a significant performance gap was identified:

* The overall average ProfitMargin across all vendors was found to be approximately -15.6%, with a median of 30.4%, indicating a high degree of variability and a net loss for the business.

* The t-test yielded a t-statistic of -17.64 and a p-value of 0.0000.

* The low p-value confirms that there is a statistically significant difference in the mean profit margins between top-performing and low-performing vendor groups.

# Technologies and Libraries
Python: The core programming language.

* **Pandas**: Used for data manipulation, cleaning, and analysis.

* **NumPy**: Used for numerical operations, including handling infinite values.

* **Matplotlib & Seaborn**: Used for creating insightful data visualizations.

* **SciPy**: Used for performing the statistical t-test.

* **SQLAlchemy**: Used to connect to and interact with the MySQL database.

# How to Run the Project
Clone the Repository: Clone this project to your local machine.

Install Dependencies: Make sure you have Python and Jupyter installed. Then, install the required libraries:

```pip install pandas numpy seaborn matplotlib sqlalchemy scipy```

Database Setup: Ensure you have a MySQL database set up with the necessary vendor data. Update the connection details in the Importing_data_to_database&DataCleaning.ipynb notebook.

# Run Notebooks:

* First, run Importing_data_to_database&DataCleaning.ipynb to clean and prepare the data.
  
* Next, run analysis.ipynb to perform the analysis and generate the plots.
