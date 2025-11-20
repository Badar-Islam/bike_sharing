# Evaluating Demand Determinants for Yulu's Micro-Mobility Solutions




## 🧩 **Business Problem**

India’s largest micro-mobility platform, wants to understand **what factors significantly impact the demand for electric bike rentals**.

The dataset contains two years of rental data with variables such as season, weather, holiday, working day, temperature, humidity, and more.
The company aims to identify **statistically significant demand drivers** to optimize:

* Fleet distribution
* Pricing strategies
* Operational planning
* Seasonal resource allocation

---

## 🎯 **Objective**

The goal of this project is to:

* Analyze the Yulu rental dataset across time, season, and environmental conditions.
* Perform hypothesis testing to determine **which factors significantly affect rental demand**.
* Identify patterns and trends in bike usage across seasons and working/holiday statuses.
* Translate analytical findings into business insights for Yulu’s operations team.

## Column Profiling:

|Column |	Description|
|-------|------------|
|datetime |	datetime|
|season	| season (1: spring, 2: summer, 3: fall, 4: winter)|
|holiday |	whether day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)|
|workingday |	if day is neither weekend nor holiday is 1, otherwise is 0.|
|temp |	temperature in Celsius|
|atemp |	feeling temperature in Celsius|
|humidity |	humidity|
|windspeed |	wind speed|
|casual	| count of casual users|
|registered |	count of registered users|
|count | Total_riders	count of total rental bikes including both casual and registered|

<b>weather</b>:
|Category |	Details|
|---------|--------|
|1	| Clear, Few clouds, partly cloudy, partly cloudy|
|2	| Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist|
|3	| Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds|
|4	| Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog|

---

## 🛠️ **Tasks Performed**

* Loaded and inspected the dataset for schema, completeness, and variable types.
* Corrected inconsistent data types through type-casting (e.g., categorical variables).
* Conducted missing value and duplicate checks (none found).
* Explored all numerical and categorical variables using EDA.
* Visualized relationships using distribution plots, boxplots, and scatterplots.
* Analyzed seasonal and weather-driven variations in rentals.
* Performed **Hypothesis Testing (t-tests, ANOVA)** based on:

  * Season
  * Holiday vs. non-holiday
  * Working day vs. weekend
  * Weather condition
* Evaluated statistical significance (p-values, confidence levels).
* Interpreted results into actionable business recommendations.

---

## 🧠 **Concepts Used**

### 🔹 Exploratory Data Analysis (EDA)

* Distribution analysis
* Trend identification
* Outlier detection
* Categorical vs numerical comparisons

### 🔹 Statistical Hypothesis Testing

* t-tests
* ANOVA
* Confidence interval interpretation
* Understanding p-values

### 🔹 Data Preprocessing

* Type casting
* Feature understanding
* Categorizing temporal variables

### 🔹 Business Interpretation

* Understanding seasonal demand
* Effect of environmental variables
* Operational decision support

---

## 🔍 **Findings & Observations**

### **1. Data Quality**

* No missing values
* No duplicates
* Two years of continuous rental data
* Season, holiday, workingday, and weather are clearly defined categorical variables

### **2. Seasonal Trends**

* Bike rentals show visible seasonal fluctuations.
* Certain seasons demonstrate significantly higher rental counts.

### **3. Weather Conditions**

* Adverse weather (rain, snow, storms) shows a noticeable drop in demand.
* Mild and clear weather conditions lead to peak rentals.

### **4. Working Day vs Weekend**

* Working days have **different rental patterns** compared to weekends.
* Demand curves vary significantly across day types.

### **5. Holiday Impact**

* Holidays show distinct usage patterns—often lower than working days.

---

## 📊 **Hypothesis Testing Results (Summary)**

| Factor Tested                          | Test Used           | Statistical Result  | Business Interpretation                            |
| -------------------------------------- | ------------------- | ------------------- | -------------------------------------------------- |
| **Season**                             | ANOVA               | Significant p-value | Season strongly influences rental demand           |
| **Holiday**                            | t-test              | Significant         | Rentals differ on holidays vs normal days          |
| **Workingday**                         | t-test              | Significant         | Weekdays vs weekends have different usage          |
| **Weather Situation**                  | ANOVA               | Significant         | Weather conditions influence demand                |
| **Temperature / Humidity / Windspeed** | Correlation + tests | Mixed significance  | Some environmental variables correlate with demand |

### **Conclusion:**

**Rental demand is statistically influenced by season, working day status, holiday status, and weather conditions.**

---

## 🌦️ **Demand Drivers & Seasonal Patterns**

Based on EDA + hypothesis results:

### **High Demand Conditions**

- ✔ Clear weather
- ✔ Moderate temperature
- ✔ Non-holiday weekdays
- ✔ Certain favorable seasons

### **Low Demand Conditions**

- ✘ Holidays
- ✘ Adverse weather (rain, storms)
- ✘ High humidity or extreme temperatures

---

## 💡 **Key Insights**

* Demand is **not uniform**—seasonality plays a major role.
* Weather is a strong external factor affecting operational planning.
* Working days show a predictable commuter-based demand pattern.
* Holidays shift usage behavior → often leisure-driven.
* Environmental variables like humidity and temperature create non-linear effects.

---

## 📌 **Recommendations**

### **1️⃣ Optimize Fleet Allocation**

* Increase the fleet during high-demand seasons.
* Reduce or redistribute during low-demand periods.

### **2️⃣ Weather-Aware Operations**

* Plan fleet availability dynamically based on weather forecasts.
* Offer discounts in low-demand weather to maintain utilization.

### **3️⃣ Holiday & Weekend Strategy**

* Weekend/holiday demand is different — promote leisure rides
* Offer weekend passes or tourist bundles

### **4️⃣ Pricing Strategy**

* Dynamic pricing based on:

  * Peak seasons
  * High commuter periods
  * Weather-based supply-demand changes

### **5️⃣ Infrastructure Planning**

* Place more bikes around office hubs for weekdays
* Add bikes near parks and public areas for weekends/holidays

---

## 🏁 **Conclusion**

This analysis demonstrates that Yulu’s bike rental demand is strongly driven by **seasonality, weather, and day-type (working day vs holiday)**.
Through hypothesis testing, we confirmed the statistical significance of these factors.



