# EDA_Social_media_Addiction_FM1113
This repository contains a cleaned version of a student social media dataset. The Jupyter Notebook includes steps for handling missing and invalid values, correcting negative entries, removing duplicates, and encoding categorical variables. The dataset is preprocessed and ready for analysis or modeling.

# Dataset Name : Students_Social_Media_Addiction
# Total column : 13
# Total records : 250
# Column-wise Information of the Dataset
1] Student_ID: Unique identifier for each student (contains duplicates).
2] Age: Age of the student in years.
3] Gender: Male or Female.
4] Academic_Level: Education level (High School, Undergraduate, Graduate).
5] Country: Country of the student.
6] Avg_Daily_Usage_Hours: Average social media usage per day (contains missing and negative values).
7] Most_Used_Platform: Most frequently used social media platform.
8] Sleep_Hours_Per_Night: Average sleep hours per night (contains negative values).
9] Mental_Health_Score: Score indicating mental health status (contains negative values).
10] Conflicts_Over_Social_Media: Number of conflicts due to social media (contains missing values).
11] Addicted_Score: Social media addiction score (contains missing values).
12] Affects_Academic_Performance: Indicates if social media affects academics (Yes/No).

# Analysis of Data
1. Dataset Overview :
Dataset with 250 rows × 13 columns containing student demographics, social media usage, sleep patterns, and academic impact.
Dropped irrelevant column Unnamed: 11.
Includes 6 categorical and 7 numerical features.

2. Data Quality Checks:
Missing values found in Avg_Daily_Usage_Hours, Conflicts_Over_Social_Media, and Addicted_Score.
One duplicate Student_ID removed.
Negative values corrected in Avg_Daily_Usage_Hours, Sleep_Hours_Per_Night, and Mental_Health_Score.
All categorical values standardized.

3. Data Cleaning :
Handled missing data using mean/median for numeric and mode for categorical columns.
Removed duplicates and cleaned invalid entries.
Converted text to lowercase and trimmed spaces.

4. Descriptive Statistics :
Average student age: ~20 years.
Average daily usage: ~4.5 hours.
Average sleep: ~6.8 hours.
Mean mental health score: ~6.3.
About 55% of students reported an effect on academics.

5. Data Transformation & Encoding :
Applied Label Encoding to categorical columns.
Normalized numerical columns using MinMaxScaler.
Created derived features for better analysis.

6. Outlier Detection & Treatment :
Used IQR and Z-Score methods to identify and cap outliers.
Ensured realistic value ranges across numeric columns.

7. Data Visualization
Visualized key insights using bar charts, histograms, box plots, and correlation heatmaps to explore relationships between social media usage, sleep, and mental health.

# Insights & Interpretation
A] Key findings :
✅Usage and addiction patterns:
1] Students with higher Avg_Daily_Usage_Hours tend to have higher Addicted_Score.
2] Those spending more time on social media show higher Conflicts_Over_Social_Media.

✅Sleep and mental health:
1] Students with less Sleep_Hours_Per_Night often report lower Mental_Health_Score.

✅Demographic observations:
1] Certain Academic_Level or Gender groups spend more time on social media platforms.
2] Platform usage (e.g., TikTok, YouTube) varies across Age and Country.

B]Trends and Anomalies :
✅Trends:
1] Positive correlation between Avg_Daily_Usage_Hours and Conflicts_Over_Social_Media.
2] Negative correlation between Sleep_Hours_Per_Night and Addicted_Score.
3] Older students tend to have slightly higher Mental_Health_Score.

✅Anomalies / Outliers:
1] Some students have extremely high Student_ID (possibly data entry errors).
2]Unusually high Conflicts_Over_Social_Media in a few cases despite low usage.
3] Zero or missing values in Unnamed: 11 — removed as irrelevant.

C] Relationships Between Features : 
✅Correlation insights:
1] Avg_Daily_Usage_Hours ↔ Addicted_Score: strong positive correlation.
2] Sleep_Hours_Per_Night ↔ Mental_Health_Score: mild positive correlation.
3]Conflicts_Over_Social_Media ↔ Addicted_Score: moderate positive correlation.

✅Categorical vs numeric relationships:
1] Gender and Academic_Level show differences in platform usage and usage patterns.
2] Students affecting academic performance (Affects_Academic_Performance) show higher social media usage and conflicts.

D] Implications for Modeling :
✅Predictive modeling:
1] Addicted_Score or Mental_Health_Score can be predicted using numeric features like Avg_Daily_Usage_Hours, Sleep_Hours_Per_Night, Conflicts_Over_Social_Media.
2] Categorical variables (Gender, Academic_Level, Most_Used_Platform) can be included via 
   One-Hot Encoding.

✅Feature selection:
1] Highly correlated features (like Avg_Daily_Usage_Hours and Addicted_Score) may need careful handling to avoid multicollinearity.
2] Outlier treatment (capping or Winsorization) ensures robust model performance.

✅Potential interventions / insights:
1] Reducing daily usage or encouraging better sleep might improve Mental_Health_Score.
2] Understanding platform-specific conflicts can guide student counseling or awareness programs.

# Project Summary
The cleaned student social media dataset provides valuable insights into how social media usage affects students’ sleep, mental health, and academic performance. After handling missing values, correcting invalid entries, and standardizing data, the dataset is now accurate, consistent, and ready for analysis or modeling. The visualizations and statistical summaries highlight meaningful patterns that can help understand students’ online behavior and its academic impact.
