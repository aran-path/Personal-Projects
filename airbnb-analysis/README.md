# Airbnb Listings Analyzer & Price Prediction (Python)

## Overview
This project analyzes Airbnb listing data to understand the factors that influence listing prices and to build predictive models for estimating Airbnb prices in the city of Columbus Ohio. The project combines exploratory data analysis, feature engineering, natural language processing, geospatial visualization, and machine learning.

The main goal was to explore how listing characteristics such as location, room type, bedrooms, reviews, amenities, and listing descriptions relate to price, and then use those features to predict listing prices more effectively.

---

## Objectives
- Explore patterns in Airbnb listing prices
- Identify important features related to price
- Engineer new structured and unstructured features
- Build and compare predictive models
- Interpret model results using evaluation metrics and feature importance

---

## Tools & Libraries
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Folium
- Scikit-learn

---

## Dataset
This project uses Airbnb listing data from **Inside Airbnb**, an open-data source that provides public Airbnb market data for many cities.

- Source: [Inside Airbnb](http://insideairbnb.com/get-the-data.html)
- File used: `listings.csv.gz`
- Dataset includes variables such as price, room type, neighborhood, bedrooms, bathrooms, reviews, amenities, location coordinates, and listing descriptions.

> Replace this section with your exact city, for example:  
> **City used:** New York City / Chicago / Los Angeles / whichever you chose.

---

## Project Workflow

### 1. Data Cleaning & Preprocessing
- Loaded the Airbnb listings dataset into Python
- Cleaned the `price` column by removing dollar signs and commas, then converted it to numeric format
- Handled missing values in relevant columns
- Filtered out extreme price outliers
- Applied a log transformation to price to reduce skew before modeling

### 2. Exploratory Data Analysis
- Examined price distributions using histograms
- Compared prices across room types and neighborhoods
- Explored relationships between price, reviews, and availability
- Created correlation heatmaps for numeric variables
- Built scatter plots to visualize relationships between key features

### 3. Geospatial Visualization
- Used Folium to create interactive maps of Airbnb listings
- Visualized geographic distribution of listings
- Built a more advanced map showing price-based patterns by location

### 4. Feature Engineering
- Created structured features from existing variables such as bedrooms, review scores, and availability
- Extracted binary amenity features such as:
  - WiFi
  - Kitchen
  - Air conditioning
  - Heating
  - Parking
  - Pool
  - Washer / Dryer
- Applied **TF-IDF vectorization** to listing descriptions to convert text into numeric features for modeling

### 5. Predictive Modeling
#### Linear Regression
- Built an initial linear regression model as a baseline
- Evaluated performance using RMSE and R²
- Improved the baseline model by adding more features and applying transformations

#### Random Forest Regressor
- Built a Random Forest model to capture more complex and nonlinear relationships
- Used structured features, amenity features, and TF-IDF text features
- Compared model performance against the baseline model

### 6. Model Evaluation & Interpretation
- Evaluated models using:
  - **RMSE (Root Mean Squared Error)**
  - **R² Score**
- Interpreted feature importance from the Random Forest model to identify which variables most influenced listing prices

---

## Key Results
- Improved the baseline linear regression model by adding relevant features and transforming the target variable
- Reduced prediction error after feature engineering and preprocessing
- Built a Random Forest model that captured more complex price patterns
- Identified important drivers of Airbnb price, including structured features, amenities, and descriptive text

---

## Skills Demonstrated
- Data cleaning and preprocessing
- Exploratory data analysis
- Data visualization
- Feature engineering
- Natural language processing with TF-IDF
- Geospatial analysis with Folium
- Supervised machine learning
- Model evaluation and interpretation

---

## Files
- `airbnb_analysis.ipynb` – main notebook with cleaning, EDA, feature engineering, and modeling
- `README.md` – project overview and documentation



---

## How to Run
1. Download the Airbnb dataset from Inside Airbnb
2. Upload the dataset to Google Colab or open the notebook in Jupyter
3. Run the notebook cells from top to bottom
4. Review visualizations, model outputs, and feature importance results

---

## Future Improvements
- Try XGBoost or Gradient Boosting for stronger predictive performance
- Add more advanced text analysis on listing descriptions
- Build an interactive dashboard in Tableau or Streamlit
- Compare pricing patterns across multiple cities

---

## Dataset
This project uses Airbnb listing data from **Inside Airbnb**, an open-data source that provides publicly available Airbnb market data for cities around the world.

- Source: [Inside Airbnb](http://insideairbnb.com/get-the-data.html)
- File used: `listings.csv.gz`
- City analyzed: [Columbus OH]

---

## Author
Aran Pathmarajah

This project was created as part of my data science portfolio to strengthen my skills in data analysis, machine learning, and real-world business insight generation.
