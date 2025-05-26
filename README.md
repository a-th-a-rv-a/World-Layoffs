# World-Layoffs

This project involves cleaning and analyzing the World Layoffs Dataset using SQL. It is structured in two main parts: Data Cleaning and Exploratory Data Analysis (EDA). The dataset tracks layoffs across companies globally, including details such as industry, location, date, stage, and number of employees laid off.

## Data Cleaning

The cleaning process includes:

Staging Table Creation: Duplicates the original dataset into a staging table.

Removing Duplicates: Identifies and removes exact duplicate rows using ROW_NUMBER() and CTEs.

Standardizing Data:

Trims whitespace from company names.

Normalizes industry and country names (e.g., correcting "Crypto Tech" to "Crypto").

Fixes inconsistent date formats and updates the column type to DATE.

Handling Missing Values:

Fills missing industry values using matching company entries.

Removes rows with no layoff data (total_laid_off and percentage_laid_off both NULL).

Schema Finalization: Drops helper columns (like row_num) post-cleaning.


## Exploratory Data Analysis (EDA)

Key analyses include:

Top Companies by total layoffs.

Layoffs Over Time: Trends by date, month, and year.

Industry-Wise & Country-Wise layoff totals.

Startup Stage Analysis: Layoffs categorized by funding stage.

Rolling Monthly Totals: Shows cumulative layoffs over time.

Yearly Top 5 Companies: Uses window functions to rank companies with the highest layoffs per year.

