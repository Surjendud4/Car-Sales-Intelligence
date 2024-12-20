# Summery
As a Data Analyst, I believe that every step of a project involves encountering challenges, and without addressing these problems, accurate data analysis cannot be achieved.

In this project I encountered a complex issue related to building accurate relationships between multiple tables and ensuring proper calculations for metrics like Current Year Sales, Previous Year Sales, and Sales Growth. The challenge was to handle many-to-many relationships and ambiguous filter directions while maintaining data accuracy and performance.

# The Problem
I was working with four key tables:
i) Orders: Contained transactional data, including sales details.
ii) Budget: Contained planned sales by date.
iii) Returns: Listed orders that were returned.
iv) People: Included regional managers and their regions.

# The difficulties were:
i) Establishing a proper relationship between the Orders and Budget tables due to a many-to-many relationship on the date field.
ii) Calculating metrics like Previous Year Sales across multiple years (2019-2022) without a dedicated date table.
iii) Resolving ambiguous relationships between Orders and Returns.

# My Process
Analyzed the Relationships:
I examined the tables and identified the root cause of the issues
i) Orders and Budget had a many-to-many relationship.
ii) Orders and Returns were ambiguous in cross-filtering direction.

# Implemented a Date Table:
i) I created a robust Date Table with fields like Date, Year, Month, Quarter, and Week Number. Then, I established one-to-many relationships between the Date Table and both Orders and Budget tables, making the Date Table the central point for time-based calculations.

# Adjusted Filter Directions:
i) Set Budget filters Orders to ensure budget data flows into transactional analysis.
ii) Configured Returns filters Orders to focus only on returned orders for specific analyses.

# Created DAX Measures:
I built measures to calculate key metrics
i)Current Year Sales: Leveraging DATESYTD for time intelligence.
ii) Previous Year Sales: Using SAMEPERIODLASTYEAR to compare performance.
iii) Sales Growth: Calculated as (Current Year Sales - Previous Year Sales) / Previous Year Sales.

# Validated Results:
I rigorously tested the calculations by filtering individual years and validating totals across the dataset. I also ensured scalability by addressing potential edge cases, such as blank or missing data.

# Outcome
Through methodical analysis and execution, I resolved all relationship ambiguities, ensured accurate calculations, and significantly improved the model's performance. This process enhanced my confidence in solving complex data challenges and demonstrated my ability to work independently and deliver reliable solutions.

![7 1](https://github.com/user-attachments/assets/090684c9-e4ab-464a-af63-436409f27a50)

![7 2](https://github.com/user-attachments/assets/ff3c3db7-bb6d-444f-9c77-657911c98cfa)

![7 3](https://github.com/user-attachments/assets/3783492e-7a4c-455e-b5a2-746b27a78776)

![7 4](https://github.com/user-attachments/assets/3a720113-1cce-4e77-925b-6fe828fcd2d9)






