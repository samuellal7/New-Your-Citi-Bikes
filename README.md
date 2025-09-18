# 🚲 Citi Bike Usage Analysis – New York City

## 📌 Project Overview  
This project analyzes **New York City’s Citi Bike dataset** to uncover insights into rider behavior, commuting patterns, and station usage. The analysis applies **exploratory data analysis (EDA), statistical methods, linear regression, and clustering** to understand how, when, and by whom Citi Bikes are used.  

The goal is to answer key questions about **urban mobility trends** and provide **data-driven recommendations** for bike-sharing operations and city planning.  

---

## 📂 Data Source  
- **Dataset**: Citi Bike Trip Data (publicly available on [Kaggle](https://www.kaggle.com/))  
- **Coverage**: Thousands of bike trips in New York City  
- **Key Features**:  
  - Trip duration (seconds, converted to minutes)  
  - Start & end times  
  - Start & end stations (400+ unique stations)  
  - Rider demographics: birth year, gender  
  - User type: Subscriber vs Customer (casual rider)  

---

## 🔧 Data Preparation & Feature Engineering  
- Converted timestamps into **datetime** format  
- Derived features:  
  - `trip_duration_min` (minutes instead of seconds)  
  - `age` (based on birth year)  
  - `weekday` and `start_hour`  
- Removed errors: negative durations, unrealistic ages  
- Handled missing values (≈6,979 missing birth years)  
- Checked for duplicates and inconsistencies  

---

## ❓ Research Questions  
1. What are the **most popular start and end stations**?  
2. How does **trip duration vary** by weekday and time of day?  
3. What are the **peak usage times** across the day?  
4. How do **subscribers and casual riders differ** in usage?  
5. What **demographic patterns** (age, gender) are visible?  
6. How do **station flows** reveal commuting vs leisure usage?  

---

## 🧪 Hypotheses  
- **H1:** Weekday trips peak during **commuting hours (8–9 AM, 5–6 PM)**.  
- **H2:** **Subscribers** take more frequent but shorter trips compared to casual riders.  
- **H3:** Younger riders (20–40) dominate Citi Bike usage, especially for commuting.  
- **H4:** Older riders (60+) use Citi Bikes mostly for **longer leisure trips**.  
- **H5:** Station demand is concentrated in **Manhattan near transit hubs**.  

---

## 📊 Exploratory Data Analysis  

- **Trips by Weekday & Time:**  
  - Sharp weekday peaks at **commuting hours**.  
  - Weekend usage more evenly spread (recreational).  

- **Subscribers vs Casual Riders:**  
  - Subscribers dominate usage; trips are **short & frequent**.  
  - Casual riders take **fewer but longer trips** (weekends/tourists).  

- **Rider Demographics:**  
  - Core segment: **20–40-year-old subscribers**.  
  - Older riders (60+) show **longer, scattered trips**.  

- **Clusters (K-Means by Age & Trip Duration):**  
  - Cluster 1: **Commuters** (ages 25–50, short trips).  
  - Cluster 2: **Leisure riders** (ages 40–70+, longer trips).  
  - Cluster 3: **Outliers** (extreme ages/durations).  

- **Geospatial Analysis:**  
  - Demand concentrated in **Manhattan (Midtown, Downtown)**.  
  - Start/end stations overlap, confirming **short local trips**.  
  - High usage near **Penn Station & Grand Central** → last-mile commuting.  

---

## 📈 Modeling  

- **Linear Regression:** Attempted to predict **trip duration** based on demographics and time features.  
- **K-Means Clustering:** Grouped riders by **age & trip duration** into distinct commuter vs leisure segments.  

---

## 🔑 Key Findings  

1. Citi Bike is **commuter-driven**, especially weekday mornings and evenings.  
2. **Subscribers (20–40 years old)** form the largest and most consistent rider group.  
3. **Casual riders** take longer leisure-oriented trips (tourism, weekends).  
4. **Station demand** is concentrated in Manhattan, reinforcing its role in **last-mile connectivity**.  
5. Outliers highlight the need for **data cleaning** and may represent **special events/tourism**.  

---

## ⚠️ Limitations & Ethical Considerations  
- Missing demographic data (e.g., birth years).  
- Outliers (multi-day trips, unrealistic ages).  
- Data represents **Citi Bike users only** (not all NYC commuters).  
- Ethical reporting: focus on **aggregated insights** without identifying individuals.  

---

## 💡 Recommendations  

- **Subscriber Growth:** Encourage casual riders to become subscribers via discounts or weekend plans.  
- **Tourism Packages:** Introduce tourist passes for longer leisure trips.  
- **Station Expansion:** Expand in high-demand areas and improve coverage in under-served boroughs.  
- **Engagement Programs:** Incentivize older riders and leisure users with health or recreation-focused campaigns.  
- **Operational Efficiency:** Use demand hotspots to optimize bike rebalancing and reduce shortages.  

---

## Additional Visual Analysis with Tableau
https://public.tableau.com/app/profile/samuel.lal7799/viz/Book1_17581430061580/CitiBikeUsageStoryboard



