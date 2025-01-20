# **Real Estate Analysis for Bay Area**

## **Objective**
The main goal of this project was to analyze real estate data from the Bay Area to uncover factors that influence property prices. To do this, I scraped property listings from Redfin, cleaned the raw data, and conducted exploratory data analysis (EDA) to draw meaningful insights. 

---

## **How I Approached This Project**
1. **Data Collection**:
   - I used `BeautifulSoup` and `requests` to scrape property details from Redfin for multiple counties in the Bay Area.
   - The data included key details like:
     - Price
     - Property size (SQFT)
     - Walk, Bike, and Transit scores
     - Bedrooms and bathrooms
     - Garage availability
     - School ratings

2. **Data Cleaning**:
   - The raw data needed a lot of work before I could start analyzing it. I:
     - Handled missing values by filling numeric columns with their means.
     - Standardized the formats to ensure consistency across columns.
     - Removed outliers in price and SQFT using the IQR (Interquartile Range) method.
     - Dropped irrelevant columns like `State` and `Street` to keep the dataset focused.

3. **Exploratory Data Analysis (EDA)**:
   - I dove into the data to answer questions like:
     - Which counties are the most and least expensive?
     - Does having a garage significantly increase property prices?
     - What’s the relationship between property size (SQFT) and price?

---

## **Key Takeaways**

### **1. Price Trends by County**
- **San Francisco County** came out as the most expensive in terms of price per square foot, closely followed by **Santa Clara County**.
- **Solano County** turned out to be the most affordable, with prices per square foot much lower than the Bay Area average.
- High variability in prices was observed in counties like **San Francisco**, where luxury and standard properties coexist.

---

### **2. Property Prices**
- Most properties are clustered around the median price, but a smaller subset of properties skew the price distribution toward higher values. 
- This pattern highlights the wide range of property values in the Bay Area.

---

### **3. Impact of Garage Availability**
- Properties with garages were significantly more expensive than those without.
- **Statistical Findings**:
  - T-Test showed a P-value of **0.000457**, meaning the difference is statistically significant.
  - On average, properties with garages are priced **$440,632.89** higher than those without.
  - Conclusion: Garage availability adds a significant premium to property prices.

---

### **4. Bedroom and Bathroom Trends**
- Properties with **3 bedrooms** and **2 bathrooms** are the most common configurations in the Bay Area.
- Larger configurations like **10+ bedrooms or bathrooms** were very rare in the dataset.

---

### **5. The Role of Walk, Bike, and Transit Scores**
- Interestingly, WalkScore, BikeScore, and TransitScore had minimal impact on property prices:
  - **WalkScore**: Correlation = **-0.06**
  - **BikeScore**: Correlation = **-0.04**
  - **TransitScore**: Correlation = **0.11**
- Conclusion: While these factors are important for livability, they don’t seem to have a major influence on property prices in this region.

---

### **6. Property Size (SQFT) and Price**
- Larger properties are generally more expensive.
- **Linear Regression Analysis**:
  - R-squared = **0.50**, showing a moderate relationship between property size and price.
- **Hypothesis Testing**:
  - Result: **Reject the null hypothesis**, meaning there is a statistically significant relationship between property size and price.
  - Conclusion: Property size plays a major role in determining property prices.

---

## **Technologies and Tools**
Here’s a quick summary of the tools I used:
- **Python Libraries**: 
  - `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`, `statsmodels`
- **Web Scraping**: `BeautifulSoup`, `requests`
- **Statistical Analysis**: T-tests, hypothesis testing, linear regression

---

## **Files in This Repository**
- `Data_Collection_Cleaning.ipynb`: This file contains the code for scraping data from Redfin and cleaning the raw data.
- `EDA_and_Analysis.ipynb`: This file includes the exploratory data analysis and detailed findings.
- `Data_clean.csv`: The cleaned dataset that was used for analysis.

---

## **Future Plans**
I feel like this project could be taken further, and here’s how I’d like to expand it:
1. Add more features like proximity to amenities, crime rates, or neighborhood demographics.
2. Build predictive models using machine learning to forecast property prices.
3. Analyze trends over time to understand how property prices have evolved in the Bay Area.

---

## **Want to See Visuals?**
I’ve created some detailed visualizations to make the findings easier to understand. You can check them out on my [**portfolio**](https://your-portfolio-link.com).

---

This project was a great opportunity to apply my skills in data collection, cleaning, and analysis while also gaining deeper insights into the real estate market. I hope you find it as interesting as I did!
