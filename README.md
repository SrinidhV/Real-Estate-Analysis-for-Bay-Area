# **Real Estate Analysis for Bay Area**

## **Objective**
The goal of this project is to analyze real estate data from the Bay Area to identify the factors influencing property prices. This was achieved through web scraping Redfin property listings, cleaning the data, and performing exploratory data analysis (EDA) to derive actionable insights.

---

## **Project Workflow**
1. **Data Collection**:
   - Used `BeautifulSoup` and `requests` to scrape Redfin property listings for multiple counties in the Bay Area.
   - Collected data on:
     - Price
     - Property size (SQFT)
     - Walk, Bike, and Transit scores
     - Number of bedrooms and bathrooms
     - Garage availability
     - School ratings

2. **Data Cleaning**:
   - Handled missing values by filling numeric columns with their respective means.
   - Standardized data formats for consistency.
   - Removed outliers in price and SQFT using the IQR (Interquartile Range) method.
   - Dropped irrelevant columns such as `State` and `Street` to focus on key attributes.

3. **Exploratory Data Analysis (EDA)**:
   - Conducted analysis to answer key business questions:
     - What counties have the highest and lowest property prices?
     - Does the presence of a garage significantly impact property prices?
     - What is the relationship between property size (SQFT) and price?

---

## **Key Insights**

### **1. Price Trends by County**
- **San Francisco County** has the highest price per square foot, followed by **Santa Clara County**.
- **Solano County** is the most affordable, with prices per square foot significantly lower than other counties.
- Price variability is higher in expensive counties like **San Francisco**, indicating a wider range of property values.

---

### **2. Distribution of Property Prices**
- Property prices in the Bay Area exhibit a right-skewed distribution, meaning most properties are clustered around a median price, while a smaller subset has significantly higher prices.
- High variability in prices is observed across counties.

---

### **3. Impact of Garage Availability**
- Properties with garages are significantly more expensive than those without.
- **Statistical Analysis**:
  - **T-Test**:
    - P-value: **0.000457** (statistically significant)
    - Price difference: **$440,632.89** on average (higher for properties with garages).
  - Conclusion: The presence of a garage positively influences property prices.

---

### **4. Distribution of Bedrooms and Bathrooms**
- Properties with **3 bedrooms** and **2 bathrooms** are the most common configurations.
- Rare configurations include properties with **10+ bedrooms and bathrooms**.

---

### **5. Influence of Walk, Bike, and Transit Scores**
- Weak correlations were observed between property prices and the following:
  - **WalkScore**: Correlation = **-0.06**
  - **BikeScore**: Correlation = **-0.04**
  - **TransitScore**: Correlation = **0.11**
- **Conclusion**: Walkability and transit access have minimal impact on property prices in the Bay Area.

---

### **6. Relationship Between Property Size (SQFT) and Price**
- Larger properties tend to have higher prices.
- **Linear Regression**:
  - R-squared: **0.50** (moderate relationship between property size and price).
- **Hypothesis Testing**:
  - Null Hypothesis (H0): There is no significant difference in property prices based on property size.
  - Result: **Reject H0** (P-value < 0.05).
  - Conclusion: Property size has a statistically significant impact on price.

---

## **Technologies and Tools**
- **Python Libraries**:
  - `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`, `statsmodels`
- **Web Scraping**: `BeautifulSoup`, `requests`
- **Statistical Analysis**: T-tests, hypothesis testing, linear regression

---

## **Files in the Repository**
- `Data_Collection_Cleaning.ipynb`: Web scraping and data cleaning code.
- `EDA_and_Analysis.ipynb`: Exploratory data analysis and insights.
- `Data_clean.csv`: Cleaned dataset used for analysis.

---

## **Future Enhancements**
1. Incorporate additional features such as proximity to key amenities, crime rates, and neighborhood demographics.
2. Build machine learning models to predict property prices.
3. Extend the analysis to include temporal trends in property prices.

---

## **Portfolio Link**
For detailed visualizations and an interactive view of the analysis, visit my [**portfolio website**](https://your-portfolio-link.com).

---

This README provides a structured summary of the project, focusing on the analysis while encouraging viewers to explore visualizations via your portfolio.
