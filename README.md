# Anime-Rating-Regression-Analysis

# Introduction
This project explores the factors influencing anime ratings through multiple linear regression
It analyzes various features such as rank, popularity, media type, and season of release,etc. providing insights for anime producers and enthusiasts. The repository includes data preprocessing, model fitting, and d interpretations of the regression results.


###  Dataset

**Source**:  
The dataset for this analysis was sourced from a GitHub repository.

**Key Variables**:  
The dataset contains several features related to anime characteristics, including:
- **Year of Production**: The year in which the anime was produced.
- **Number of Episodes**: Total episodes in the anime series.
- **Average Length of Episode**: The average duration of each episode in minutes.
- **Studio**: The studio(s) responsible for producing the anime.
- Other features include rank, popularity, media type, ratings, and more.

**Preprocessing**:  
- **Handling Missing Values**:  
  - A small number of missing values (NAs) were found in the dataset. Where necessary, NAs were removed, and in some cases, missing numerical data was replaced by the mean of the respective feature.
  
- **Categorical Variables**:  
  - One-Hot Encoding (OHE) was applied to categorical variables (e.g., media type, rating) to prepare them for the regression analysis.

Here's the revised structure for **Point 5: Modeling**, with the order adjusted:

Here’s a revised structure for **Point 4: Exploratory Data Analysis (EDA)**, following the format you provided:

---

###  Exploratory Data Analysis (EDA)

**Libraries Used**:  
For exploratory data analysis (EDA), Seaborn and Matplotlib were utilized to create visualizations that aid in understanding the dataset.

**Types of Visualizations**:  
Various plots were generated, including scatter plots, bar plots, and line plots, to explore relationships among variables and identify trends in anime ratings, genres, and production patterns.

---

Let me know if you want to make any changes or if we can move on!


###  Modeling

**Assumptions Check**:  
Before building the regression model, the assumptions of Multiple Linear Regression (MLR) were verified, including linearity, independence, homoscedasticity, and normality of residuals.

**Multicollinearity**:  
To address multicollinearity, the Variance Inflation Factor (VIF) was calculated for each feature. Variables with high VIF scores were monitored, and adjustments were made as needed to improve the model's robustness and reduce redundancy among predictors.

**Model Fitting**:  
The Multiple Linear Regression model was then fitted using the `scikit-learn` library, incorporating the selected independent variables to predict the mean rating of the animes.

**Model Accuracy**:  
The adjusted R² value was calculated to assess the accuracy of the model and its explanatory power, considering the number of predictors used. This metric helped evaluate how well the model fits the data.

Here are the key takeaways from your analysis formatted as bullet points:

---

### Important Takeaways from the Analysis

- As anime gains popularity through strong marketing, viewers set higher expectations. If these are unmet, it may lead to lower average ratings despite the anime’s wide appeal.
  
- Popular anime often attracts a larger, more diverse audience, including casual viewers who may not deeply connect with the content, potentially resulting in lower ratings.

- Comedy is the most commonly produced genre among animes.

- Studios like Kyoto Animation, ufotable, and Bones focus on quality over quantity, producing fewer anime but achieving higher average ratings.

- High-output studios like Sunrise may produce more anime but don’t always reach the same level of average ratings, indicating a balance between quantity and quality.

- Spring leads in anime releases, while summer sees the fewest. Interestingly, fall releases tend to have the highest average ratings. As seasons progress from fall to summer, both the number of anime releases and their mean ratings decline, suggesting that audience engagement may taper off as the year progresses.

- G-rated animes have the lowest mean rating, indicating that family-friendly content may not resonate as strongly with audiences seeking more diverse themes.

- Ratings increase from G to PG to R-rated content, reflecting a preference for more mature themes, despite fewer animes in these categories.

- Real-life data often deviates from strict mathematical assumptions. In the current regression process, homoscedasticity is not fully followed, which is a limitation of this analysis.

- Recent anime tend to have lower mean ratings, suggesting newer content is rated lower, while audiences still prefer classic, older animes.

- **Information from the Regression Coefficients**:
    - Among all non-categorical regressors, only 'Year of production' has a significant impact on mean rating, with mean ratings decreasing as the year progresses.

- Interpretation of encoded variable coefficients is relative to the baseline category (which was dropped to avoid multicollinearity):
    - For the media type category, 'Movie' was dropped as the baseline for comparison. Music-type animes have a coefficient of 0.025, indicating that, with other factors constant, a music-type anime will have a rating 0.025 higher than a movie.
    - ONAs (Original Net Animations) perform better than other types when controlling for other regressors.

- For the airing category (finished or currently airing), animes that have finished airing generally receive higher ratings, as viewers may appreciate the complete series more fully.

- For the rating category, the baseline is general rated. Although general-rated animes have the lowest average rating among all, they perform better than R and R+ rated animes after controlling for other regressors. Only PG-rated animes show a slightly positive effect compared to general-rated ones, implying that general-rated content may have broader appeal.

- For the last categorical variable (season in which anime is released), fall is used as the baseline:
    - Similar to the previous category, summer had the least average rating in the EDA, but after controlling for other factors, animes released in summer have a better average rating than others.



"Thank you for taking the time to read this information!"







