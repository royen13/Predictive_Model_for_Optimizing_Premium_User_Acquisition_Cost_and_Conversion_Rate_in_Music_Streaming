# Optimize Premium User Acquisition Cost and Conversion Rate with Predictive Modeling for Music Streaming Service


### Introduction
XYZ is a music-listening social networking website, operates under a "freemium" business model where basic services are free, and users can subscribe to premium services for additional features. In an effort to maximize revenue while minimizing marketing costs, XYZ wanted to improve the efficiency of their marketing campaigns. The goal was to predict which free users are most likely to convert to premium subscribers within the next 6 months when targeted by a promotional campaign. This repository contains a predictive model that aims to accomplish this goal using the data from a previous marketing campaign.

### Business Challenges
XYZ’s main goal is to maximize revenue by:

1. Increasing the number of premium subscribers.

2. Minimizing marketing costs.

Currently, XYZ’s marketing strategy involves randomly targeting free users, hoping they will convert to premium subscribers. However, the previous marketing campaign achieved only a 3.7% success rate, which resulted in an inefficient use of resources.

### Solution
To solve this problem, we developed a predictive model that efficiently identifies users most likely to upgrade to premium. By using this model, XYZ can optimize their marketing efforts by targeting only those individuals with the highest probability of conversion. This approach will ultimately save money, reduce wasted marketing efforts, and maximize the chances of converting free users into paying premium subscribers.

### Data Source
The dataset used in this project is XYZData.csv, which contains 41,540 records of users targeted during a previous marketing campaign. Each record includes 25 attributes describing user behavior and demographics, such as:

* Adopter (binary): Whether the user became a premium subscriber within 6 months.

* Age (integer): The user's age.

* Male (binary): Gender information.

* Friend count (integer): Number of friends the user has on the platform.

* Songs listened (integer): Total number of songs the user listened to.

* Loved tracks (integer): Total number of songs the user liked.

* Tenure (integer): Number of months the user has been registered on the platform.

And several other features related to changes in user behavior (e.g., delta friend count, delta songs listened).


### Analysis Steps
The solution process involved building a predictive model using R, which includes the following steps:

1. Data Processing: Cleaning and preprocessing the data for use in the model.

2. Model Selection: Exploring various machine learning algorithms, including Decision Tree, k-NN, Naïve Bayes, Random Forest, and Logistic Regression. We used AUC score to evaluate model performance and selected the Decision Tree model due to its interpretability, simplicity, and efficiency.

3. Feature Selection: Using Filter Approach and Forward Selection to identify the most predictive features. We found that the top two features—"lovedTracks" and "delta_songsListened"—were the most informative.

4. Model Finalization: We built the final Decision Tree model using only the top two features to balance performance and complexity.

* Model Evaluation
  * To evaluate the model, we used AUC score, which measures how well the model distinguishes between users who are likely to upgrade and those who are not.

* Final Model
  * After considering performance and simplicity, the final model is a Decision Tree trained on the top two features:

  * lovedTracks: The total number of different songs the user liked.

  * delta_songsListened: The change in the number of songs a user listened to over the 3-month period before the campaign.

### Key Findings
Our predictive model was able to achieve the following results:

1. 60.7% reduction in cost per premium user: By targeting only the most likely adopters, XYZ can significantly reduce the cost of acquiring each premium user.

2. 6% increase in conversion rate: The model identifies users who are more likely to convert, thereby improving the effectiveness of the marketing campaign.

These results demonstrate the effectiveness of using predictive modeling to improve marketing strategy, reduce wasteful spending, and ultimately increase premium subscriptions.


