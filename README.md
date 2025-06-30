Google Play Store Data Analysis
This project presents a detailed analysis of the Google Play Store dataset consisting of 10,841 Android applications. The objective is to uncover trends and insights related to app ratings, installs, reviews, pricing, and categories by applying structured data analysis, visual exploration, statistical testing, and regression modeling.

Project Overview
Loaded and cleaned the dataset by handling missing values, converting data types, and removing duplicates.

Performed exploratory data analysis (EDA) to identify key trends in app ratings, content ratings, categories, and price distributions.

Conducted statistical hypothesis testing including T-tests and Z-tests to validate assumptions about ratings across app types.

Applied feature engineering to improve predictive modeling by creating new variables such as log-transformed features, app age, price flags, and categorical bins.

Developed regression models to predict app ratings using both base and engineered features, and evaluated performance using R² scores and cross-validation.

Tools and Libraries Used
The following Python libraries were used to carry out the analysis:

Pandas and NumPy: For efficient data manipulation and numerical computation

Matplotlib and Seaborn: For creating statistical visualizations and plots

Scipy: For hypothesis testing including T-test and Z-test

Scikit-learn: For model building, data splitting, and evaluation

Warnings: Suppressed to ensure clean output during execution

Key Steps and Insights
1. Data Cleaning and Preprocessing
Cleaned data types: Converted columns such as Reviews, Installs, Price, and Size to appropriate numeric formats.

Parsed Last Updated to datetime and calculated app age in days.

Filled missing values in Rating, Android Version, and Current Version using median or mode.

Removed 483 duplicate rows to finalize a clean dataset with 10,356 records.

2. Exploratory Data Analysis
Rating Distribution: Majority of apps have ratings between 4.0 and 4.5.

Content Rating vs Rating: Explored age-based category impact using boxplots.

Correlation Heatmap: Revealed relationships between numerical features like Rating, Reviews, Installs, and Price.

Category Analysis: Identified top 10 app categories, showing FAMILY and GAME as most common.

Free vs Paid Apps: ~93% of apps are free; analyzed their distribution and price patterns.

Top Reviewed Apps: Highlighted popular apps like Facebook, WhatsApp, and Instagram.

3. Statistical Testing
T-Test: Tested whether the mean ratings of free and paid apps are significantly different. Result was statistically significant (p < 0.001).

Z-Test: Assessed whether the mean rating differs significantly from a baseline of 4.0. Result showed a meaningful difference.

4. Feature Engineering
Created several new features to improve regression model performance:

App Age (in days)

Log_Reviews, Log_Installs

High Price binary flag

Size Bins (Small, Medium, Large, Very Large)

Interaction term: Reviews × Rating

One-hot encoding of categorical variables such as app Category

5. Regression Modeling
Built a baseline regression model using raw numerical features (Reviews, Installs, Price, Size).

Built an enhanced model using engineered features and one-hot encoded variables.

Evaluated models using R² scores and residual plots to validate predictive power.

Final model showed improved performance, demonstrating the value of domain-specific feature engineering.

Files Included
Google play store analysis.ipynb – Jupyter Notebook containing full code, visualizations, and regression modeling steps.

Google play store analysis summary report.pdf – PDF summary of the methodology and findings.

Author
K. Kiran Sai Karthik
Email: kanagarlakiransaikarthik@gmail.com
