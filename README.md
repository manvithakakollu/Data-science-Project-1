Introduction

In this assignment, we analyze a dataset containing 39,643 online news articles with 61 attributes to predict the number of shares an article will receive.

Given the high dimensionality of the dataset, our focus is on applying feature selection and dimensionality reduction techniques to identify the most relevant explanatory variables for building an effective linear regression model.

🔑 Approach

Load the Data: Retrieve the dataset from GitHub and load it into a Pandas DataFrame.

Exploratory Data Analysis (EDA): Perform statistical and graphical analysis to understand distributions, relationships, and predictors.

Feature Selection & Dimensionality Reduction: Apply techniques such as correlation analysis, Principal Component Analysis (PCA), and stepwise selection.

Regression Model Development: Train and evaluate a linear regression model using the selected features.

Model Evaluation: Assess the model’s performance using relevant metrics.

Conclusion: Summarize findings, insights, and predictive performance.

📂 Dataset Summary
1. URL and Time-Related Features

url → Identifier, not predictive.

timedelta → Days since article publication.

2. Content-Based Features

n_tokens_title → Number of words in the title.

n_tokens_content → Number of words in the content.

n_unique_tokens → Vocabulary diversity.

n_non_stop_words / n_non_stop_unique_tokens → Proportion of meaningful words.

3. Link & Multimedia Features

num_hrefs → Number of hyperlinks.

num_self_hrefs → Internal links to same site.

num_imgs → Number of images.

num_videos → Number of videos.

4. Text & Keywords Features

average_token_length → Average word length.

num_keywords → Metadata keywords count.

5. Data Channel Features

data_channel_is_lifestyle, entertainment, bus, socmed, tech, world → Article category.

6. Keyword Sharing Metrics

kw_min_min, kw_max_min, kw_avg_min → Shares for least popular keyword.

kw_min_max, kw_max_max, kw_avg_max → Shares for most popular keyword.

kw_min_avg, kw_max_avg, kw_avg_avg → Shares for all keywords.

7. Self-Reference Features

self_reference_min_shares / max_shares / avg_sharess → Impact of referenced article popularity.

8. Publication Timing Features

weekday_is_xxx → Publication weekday.

is_weekend → Boolean for weekend publication.

9. Topic Modeling Features (LDA)

LDA_00 – LDA_04 → Closeness to latent topics.

10. Sentiment & Polarity Features

global_subjectivity, global_sentiment_polarity

rate_positive_words / rate_negative_words

avg_positive_polarity / avg_negative_polarity

title_subjectivity, title_sentiment_polarity

abs_title_subjectivity, abs_title_sentiment_polarity

11. Target Variable

shares → Number of times an article was shared.

⚙️ Step 1: Load the Data
A. Import Python Libraries

Libraries used for this assignment:

# Data Manipulation
import pandas as pd
import numpy as np

# Visualization
import matplotlib.pyplot as plt
import seaborn as sns


Pandas / NumPy → Data manipulation & numerical calculations

Matplotlib / Seaborn → Data visualizations

📊 Methods Applied

Exploratory Data Analysis (EDA) → Histograms, correlations, distributions

Feature Selection → Correlation filtering, forward/backward selection

Dimensionality Reduction → Principal Component Analysis (PCA)

Regression Model → Linear Regression using selected features

Model Evaluation → Performance metrics such as RMSE, R²

✅ Conclusion

Identified the most relevant explanatory variables that significantly impact article shares.

Reduced dimensionality to improve model interpretability and efficiency.

Trained a linear regression model that demonstrates reasonable predictive performance.

📜 License
