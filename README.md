# eastwest-airlines-clustering
Unsupervised K-Means clustering project on EastWest Airlines frequent flyer data to segment travelers, identify optimal cluster counts using scree plots, and derive targeted loyalty marketing strategies.

# EastWest Airlines Customer Segmentation & Clustering

## 1. Business Problem
* **1.1. Business Objective:** Segment frequent flyer program members based on their travel patterns, mileage accumulation, and flight activity to design customized loyalty rewards and targeted promotional campaigns.
* **1.2. Constraints:** High skewness in mileage accumulation distributions and potential outliers (super-frequent flyers) requiring careful scaling and outlier handling.

## 2. Data Dictionary
| Feature | Data Type | Description |
| :--- | :--- | :--- |
| `ID` | Integer | Unique identifier for the flight member. |
| `Balance` | Integer | Number of miles eligible for award travel. |
| `Qual_miles` | Integer | Miles counted as qualifying for top-flight status. |
| `cc1_miles` / `cc2_miles` / `cc3_miles` | Integer | Miles earned with/under credit card transacting (bins 1-5). |
| `Bonus_miles` | Integer | Miles earned from non-flight bonus transactions. |
| `Bonus_trans` | Integer | Number of non-flight bonus transactions/awards. |
| `Flight_miles_12mo` | Integer | Number of flight miles in the past 12 months. |
| `Flight_trans_12` | Integer | Number of flight transactions in the past 12 months. |
| `Days_since_enrolled` | Integer | Number of days since the member's account was opened. |

## 3. Exploratory Data Analysis (EDA)
* **3.1. Summary:** Statistical summary reveals heavily right-skewed distributions across mileage and transaction counts.
* **3.2. Univariate Analysis:** Visualized distributions of balances, bonus miles, and enrollment durations using histograms and boxplots.
* **3.3. Bivariate Analysis:** Examined correlations between total miles earned, flight frequency, and account age.

## 4. Data Pre-processing
* **4.1. Data Cleaning & Feature Engineering:** Handled missing values, dropped redundant ID columns, and applied standard scaling techniques to normalize varying magnitude features.

## 5. Model Building
* **5.1. Model Execution:** Scaled features using `StandardScaler` and experimented with various initializations.
* **5.2. Scree Plot & Optimum Clusters:** Implemented the Elbow curve method (inertia vs. number of clusters $k$) to find the optimal cluster count.
* **5.3. Validation & Insights:** Validated stability across alternative cluster choices, labeled clusters (e.g., "Frequent Flyers", "Low-Activity Base", "High-Bonus Earners"), and extracted actionable marketing profiles.

## 6. Business Benefits & Impact
* Enables marketing teams to target high-value loyalty members effectively, optimize promotional budget allocations, and reduce customer churn through tailored rewards.
