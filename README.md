# myproject123

Video Game Quality vs. Popularity Analysis (DSA210 Term Project)

Student: Ömer Baran Sına
Academic Year: Spring 2025-2026

Status: Data Collection, EDA, and Hypothesis Testing Complete.

Motivation:
The video game industry is a multi-billion dollar market, but a common question remains: Does a "good" game always sell well? We often see high-rated indie gems struggle while "AAA" titles with mixed reviews break sales records.My motivation for this project is to investigate the Quality-Popularity Gap. I want to see if critic/user ratings have a statistically significant correlation with global sales, or if marketing and brand power (popularity) are the true drivers of success.

Overview:
This project explores the relationship between a game's critical/user success and its commercial performance. By merging historical sales data with modern popularity metrics, I aim to determine if "Quality" (Ratings) can reliably predict "Success" (Sales).

Data to be Used: 
     1. Video Game Sales DataSource: Kaggle (Historical Sales Dataset)Data: Over 16,000 games with sales figures across North America, Europe, Japan, and globally.Features: Rank, Name, Platform, Year, Genre, Publisher, Global_Sales.
     
     2. Popular Games & Ratings DataSource: Kaggle (Games/Popularity Dataset)Data: Modern ratings and popularity scores.Features: Title, Rating (User/Critic scores), Release_Date.
                 
Exploratory Data Analysis (EDA):
     Analyzed the distribution of sales across different genres.
     Created Regression Plots to visually inspect the trend between Rating and Global_Sales.
     Identified outliers—games with low ratings but massive sales, and vice versa.
     
Hypothesis Testing: I performed Pearson Correlation Tests to validate my primary hypothesis:
     Null Hypothesis: There is no significant correlation between a game's rating and its global sales.
     Alternative Hypothesis: Higher ratings lead to significantly higher global sales.
     
Current Results:
     Finding: The correlation coefficient ($r$) was found to be 0.0733, indicating a Weak Correlation.
     P-Value: The p-value was significantly low: 5.9292e-03, making the results statistically significant.
     Conclusion: While a relationship exists, it is weak. This suggests that "Quality" (Rating) is not the primary driver of "Success" (Sales), supporting the Quality-Popularity Gap theory.
     
Project Structure:
     vgsales.csv.zip: Raw historical sales data.games.
     csv.zip: Raw ratings and popularity 

AI Usage DisclaimerAI (Gemini) was utilized for:
      Coding Support: Debugging Python KeyError issues and optimizing Pandas merge operations.
      Documentation: Assisting in structuring the project report and README for clarity.
