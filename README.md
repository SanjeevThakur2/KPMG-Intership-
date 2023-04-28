# KPMG-Intership

The Sprocket Central Pty Ltd dataset is a dataset provided for an internship project with KPMG. The dataset contains data from Sprocket Central Pty Ltd, a fictional company that sells bikes and cycling accessories to customers around the world.

This code reads data from a file named KPMG.xlsx. It creates three separate variables from three different sheets named transaction, CustomerDemographic, and CustomerAddress.

Next, the code checks the transaction data frame for missing values, drops the rows where brand is null, and fills the missing values in the online_order column with its mode.

In the CustomerDemographic data frame, the code replaces the gender column's F, Femal with Female, M with Male, and U with Unspecified. It drops the default column, removes the rows with the deceased_indicator as Y, replaces the spelling mistake in job_industry_category, and fills the null values in the job_industry_category column. It first finds the percentage of missing values in the column, then fills the missing values with the following approach: fill Manufacturing and Financial Services with the most frequent values and Health and Retail with half of the remaining null values. Finally, it fills the missing values in the tenure column with the median.

The CustomerAddress data frame is only read and not modified.

The code uses numpy, statistics, pandas, matplotlib, and seaborn libraries for data analysis and visualization. It also imports ExcelWriter and ExcelFile from pandas to read the excel file. The warnings library is used to ignore the warnings generated during execution.

The code can be executed in any python environment after installing the libraries mentioned above.
