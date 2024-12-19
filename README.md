---

# **Airbnb Listing Price Analysis: Statistical Modeling** 🏠

This project analyzes the factors influencing Airbnb listing prices using statistical modeling techniques. The dataset was sourced from Kaggle and includes a variety of features such as room types, cleanliness ratings, distance from the city center, and guest satisfaction ratings. Through rigorous analysis and modeling, this project provides insights to optimize pricing strategies.

---

## **Project Overview**
Airbnb pricing strategies are influenced by several key factors. This project aims to:
- Identify the most influential factors on listing prices.
- Analyze the impact of room types, cleanliness ratings, distance, and person capacity on prices.
- Provide actionable insights for optimizing pricing strategies.

The project uses linear regression, hypothesis testing, ANOVA, and model selection techniques to uncover insights.

---

## **Dataset**
- **Source**: [Kaggle](https://www.kaggle.com/)
- **Rows**: 4,303 (training set), 1,076 (testing set)
- **Columns**: 13 features, including:
  - `realSum`: Listing price
  - `room_type`
  - `person_capacity`
  - `cleanliness_rating`
  - `distance` and `metro_dist` (from city center)
  - `guest_satisfaction_overall`

---

## **Methods and Techniques**
### **1. Data Preprocessing**
- Checked for missing values (none found).
- Encoded categorical variables (`room_type`, `host_is_superhost`) to numeric formats.
- Transformed data using cube root transformations to standardize and reduce variance.
- Outliers removed iteratively based on diagnostic plots.

### **2. Regression Modeling**
- Created a linear regression model with `realSum` as the response variable.
- Model diagnostics included:
  - Homoscedasticity
  - Normality of residuals
  - Handling high-leverage points.

### **3. Model Selection**
- **Backward Selection**: Iteratively removed predictors with high p-values.
- **Forward Selection**: Used AIC and BIC criteria for optimal predictor selection.
- Final model included 9 predictors.

### **4. ANOVA Testing**
- Identified the most significant predictors:
  - `person_capacity` (highest F-value and lowest p-value).
  - Business-oriented listings also significantly influenced pricing.

### **5. Hypothesis Testing**
- Significant relationships were identified:
  - **Distance from city center**: Negative impact on price.
  - **Cleanliness rating**: Positive correlation with price.
  - **Room type**: Private rooms priced higher than shared rooms.

---

## **Key Results**
- **Most Influential Factor**: `person_capacity`.
- **Impactful Features**:
  - Room type, cleanliness rating, distance, and business orientation.
- **MSPE Values**:
  - Test dataset performance for both backward and forward selection: 229,556.4.

---

## **Visualizations**
- **Correlation Plots**: Relationships between predictors.
- **Diagnostic Plots**: Residuals and fitted values.
- **ANOVA Plots**: Impact of each predictor on price.

---

## **Conclusions**
- Listing prices are significantly influenced by room capacity, cleanliness, distance, and business orientation.
- Statistical modeling provides a robust framework for understanding pricing strategies.
- Future research could incorporate property amenities, seasonal trends, and geographical variations for further insights.

---

## **Setup and Usage**
1. Clone the repository:
   ```bash
   git clone https://github.com/ShreCodes2809/Stat_Modeling.git
   cd Stat_Modeling
   ```
2. Install required R packages:
   ```R
   install.packages(c("corrplot", "ggplot2", "leaps", "MASS"))
   ```

---

## **Future Enhancements**
- Explore additional variables such as neighborhood characteristics and seasonal trends.
- Use advanced predictive modeling techniques like random forests or neural networks.
- Analyze price variations across geographical locations.

---

This project was completed as part of the **STATS 4010** coursework.
