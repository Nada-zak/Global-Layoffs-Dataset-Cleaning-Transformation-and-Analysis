# Global-Layoffs-Dataset-Cleaning-Transformation-and-Analysis

#Project Overview: 
This project focuses on cleaning, standardizing, and analyzing a dataset related to company layoffs. The dataset contains information about companies, industries, dates, and the number of employees laid off. After cleaning and preparing the data, various analytical queries were performed to uncover trends in layoffs over time, across industries, countries, and specific companies.

#Key Steps:

##1. Data Cleaning:
•	###Removing Duplicates:###
Identified and removed duplicate records using a ROW_NUMBER() function to ensure that only unique rows remain, based on key attributes like company, location, industry, and date.
•	###Standardizing Data:###
o	Whitespace Removal: Cleaned company and country fields by trimming any leading or trailing whitespace.
o	Correcting Industry Names: Standardized industry names (e.g., ensuring all variations of 'Crypto' are labeled consistently).
o	Date Formatting: Converted date values from text to proper DATE format using the str_to_date() function.
•	###Handling Null Values:###
Filled missing values in the industry column by cross-referencing other records of the same company. This helped populate incomplete data without introducing inaccuracies.
•	###Removing Unnecessary Data:###
Removed rows where both percentage_laid_off and total_laid_off were null, as these records added no value to the analysis. Also, the row_num column, used for duplicate removal, was dropped after cleaning.

##2. Data Analysis:
After cleaning, the dataset was analyzed to extract meaningful insights regarding layoffs across companies, industries, countries, and specific periods.
Key Analyses
•	###Company-level Analysis:### The project highlights which companies had the highest number of layoffs. We focused on aggregating total layoffs by company and examined individual companies like Google to understand their specific layoff trends.
•	###Time-based Analysis:### We analyzed the data to determine the time span of layoffs, identifying the earliest and latest events recorded. Yearly and monthly trends were explored to reveal which periods saw the most significant layoffs.
•	###Industry and Geographic Insights:### The project also breaks down layoffs by industry and country, helping to identify the sectors and regions that experienced the most layoffs. This provides a clear picture of how different areas of the economy were impacted.
•	###Stage of Layoffs:### We categorized layoffs based on their stages (e.g., announced, confirmed), helping to show how far along companies were in their workforce reduction processes.
•	###Cumulative and Rolling Totals:### To track how layoffs accumulated over time, we calculated rolling totals, showing the cumulative effect of layoffs month by month. This provides an understanding of how layoffs developed over time.
•###	Top 5 Companies by Year:### A ranking system was implemented to find the top companies with the highest number of layoffs for each year. This analysis highlights which companies were most affected during specific periods, providing a deeper look at layoffs on an annual basis.

