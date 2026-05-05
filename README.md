# myproject123

Video Game Quality vs. Popularity Analysis (DSA210 Term Project)
Student: Ömer Baran Sına
Academic Year: Spring 2025-2026
Status: Data Collection, Advanced EDA, and Multi-Layered Hypothesis Testing Complete.

Motivation:The video game industry is a multi-billion dollar market, but a common question remains: Does a "good" game always sell well? We often see high-rated indie gems struggle while "AAA" titles with mixed reviews break sales records. My motivation for this project is to investigate the Quality-Popularity Gap. I want to see if critic/user ratings have a statistically significant correlation with global sales, or if factors like Genre and Market Positioning (marketing/brand power) are the true drivers of success.

Overview: This project explores the relationship between a game's critical success and its commercial performance. By merging historical sales data with modern popularity metrics, I aim to determine if "Quality" (Ratings) can reliably predict "Success" (Sales) or if this relationship is structurally different across different segments of the industry.

Data to be Used:
1. Video Game Sales Data * Source: Kaggle (Historical Sales Dataset)
  - Data: Over 16,000 games with sales figures across NA, EU, JP, and Globally.
  - Features: Rank, Name, Platform, Year, Genre, Publisher, Global_Sales.
2. Popular Games & Ratings Data * Source: Kaggle (Games/Popularity Dataset)
  - Data: Modern ratings and popularity scores (1980-2023).
  - Features: Title, Rating (User/Critic scores), Release_Date.
   
Exploratory Data Analysis (EDA)
  - Global Trend: Created Regression Plots to visually inspect the link between Rating and Global_Sales.
  - Genre Distribution: Analyzed sales across different genres using Logarithmic Scaling to account for massive "Blockbuster" outliers.
  - Quadrant Analysis: Statistically defined and visualized the "Gap" by identifying Overhyped games (High Sales, Low Rating) and Hidden Gems (Low Sales, High Rating).
  
Hypothesis Testing: I performed three levels of statistical testing to validate the "Quality-Popularity Gap":
1. H1 (Global Relationship): Tested the Pearson Correlation between ratings and global sales.
   - Null: No significant correlation exists.
2. H2 (Genre Impact): Tested if "Quality Sensitivity" varies by genre using Spearman Rank Correlation.
   - Null: Correlation is uniform across all genres.
3. H3 (Market Category): Used a Chi-Square Test of Independence to see if "Overhyped" status is tied to specific genres.
   - Null: Overhyped games occur randomly regardless of genre.

Machine Learning Methods: 
To move beyond basic statistics, I applied two Machine Learning methods:

   - Random Forest Classification: Used to predict if a game will be a "Hit" based on its Rating, Genre, and Platform.
       Performance: Achieved 77% Accuracy.
       Outcome: Feature Importance showed that Platform is the most dominant predictor of success, outweighing the actual Quality Rating.

   - K-Means Clustering: An unsupervised learning method used to mathematically group games into natural clusters. This provided an objective, AI-driven validation of the "Hidden Gems" vs. "Blockbusters" market segments.   
   
Current Results
  1. Finding 1: Global correlation is weak ($r \approx 0.07$). While statistically significant ($p < 0.05$), quality is a poor predictor of global sales. (Null H1 Rejected).
  2. Finding 2: Quality sensitivity is highly genre-dependent. RPG fans are significantly more "quality-sensitive" than Sports fans. (Null H2 Rejected).
  3. Finding 3: The "Quality-Popularity Gap" is a structural trend. Chi-Square results prove that "Overhyped" status is significantly tied to specific market segments. (Null H3 Rejected).
  
Project Structure
   - vgsales.csv.zip: Raw historical sales data.
   - games.csv.zip: Raw ratings and popularity data.
   - Data_Collection_EDA.py: Script for merging and advanced visualizations.
   - Hypothesis_Testing.py: Script for Pearson, Spearman, and Chi-Square statistical proofs.
   
AI Usage Disclaimer: AI (Gemini) was utilized for:
   - Coding Support: Debugging Python KeyError issues, optimizing Pandas merge operations, and implementing advanced statistical tests (Spearman/Chi-Square).
   - Documentation: Assisting in structuring the project report, README, and articulating the "Statistical Verdicts" for clarity.
    
