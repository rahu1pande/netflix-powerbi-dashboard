🎬 Netflix Content Performance Dashboard – Power BI

📌 Project Overview
This project analyzes Netflix content data to uncover insights related to genre distribution, content growth trends, country-wise production, and ratings classification.
The dashboard enables interactive filtering and business analysis.

📊 Dataset Details
Dataset: Netflix Titles Dataset
Total Records: 8,000+ titles
Features: Title, Type, Genre, Country, Release Year, Rating, Duration

🛠 Tools & Technologies Used
Power BI
Power Query (Data Cleaning & Transformation)
DAX (KPI Calculations)
Data Modeling

📊 Key Business Insights
Significant increase in content production observed after 2015
Drama and International Movies dominate overall catalog
Movies account for higher share compared to TV Shows
USA and India are among top content-producing countries

📈 KPIs Implemented --
Total Titles = COUNTROWS('Netflix')
Movies Count = 
CALCULATE(
    COUNTROWS('Netflix'),
    Netflix[type] = "Movie"
)
TV Shows Count = 
CALCULATE(
    COUNTROWS('Netflix'),
    Netflix[type] = "TV Show"
)
Titles by Year = 
COUNT('Netflix'[title])
Content Growth % = 
DIVIDE(
    [Total Titles] - CALCULATE([Total Titles], PREVIOUSYEAR(Netflix[release_year])),
    CALCULATE([Total Titles], PREVIOUSYEAR(Netflix[release_year]))
)
