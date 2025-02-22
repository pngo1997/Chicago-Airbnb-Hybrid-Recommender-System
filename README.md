# 🏠 Chicago Airbnb Hybrid Recommender System

## 📜 Overview
This project develops a hybrid recommender system for Chicago Airbnb listings using data from Inside Airbnb. The system recommends listings based on three main preferences:
- 👥 Guest count
- 💲 Price point
- 📝 Text comments
  
Each recommendation includes the location and distance to the nearest CTA subway station for enhanced accessibility.

## 📊 Datasets
### 📌 1. Chicago Airbnb Listings
- Contains 7,952 listings with attributes like amenities, price, and location.
### 📝 2. Chicago Airbnb Reviews
- Includes 417,795 reviews, used for sentiment analysis.
### 🚇 3. Chicago CTA Stations
- Contains 145 train stations, used to compute distances from Airbnb listings.

## 🛠️ Methodology
### 1️⃣ Exploratory Analysis
🔹 Data visualization and attribute relationship analysis.
### 2️⃣ Review Scoring
🔹 Sentiment analysis using VADER and machine learning models (Logistic Regression, Linear SVC, Naive Bayes) to understand guest feedback.
### 3️⃣ Listing Clustering
🔹 Hierarchical clustering of Airbnb listings based on name and description embeddings to identify characteristic patterns.
### 4️⃣ Recommender System
🔹 Build a recommender system uses embeddings and cosine similarity for personalized recommendations and user preferences.

## 📈 Reviews Scoring - Sentiment Analysis
✅ VADER sentiment scores benchmarked against: Logistic Regression, Linear SVC, and Naive Bayes. <br /> 
📌 **Sentiment classes:** Positive, Neutral, and Negative. <br />
📌 Final sentiment score computed using a **weighted average approach.** <br />
📌 **Key Steps:** 
- Clean the review dataset.
- Address dataset skewness (majority of listings have high ratings).
- Utilize sentiment analysis techniques such as VADER to evaluate text sentiment.
- Generate word clouds to visualize sentiment trends.
- **Libraries Used:** nltk, pandas, matplotlib, wordcloud
  
## 🔍 Clustering
✅ Listings were grouped into **three clusters based on semantic similarities.** <br /> 
1️⃣ **Vibrant Social Spaces:** Near entertainment and nightlife. <br /> 
![Word Cloud](https://github.com/pngo1997/Images/blob/main/Vibrant%20Social.png)  

2️⃣ **Cultural and Scenic Attractions:** Near museums, parks, and historical sites. <br /> 
![Word Cloud](https://github.com/pngo1997/Images/blob/main/Cultural%20and%20Attraction.png)  

3️⃣ **Accessible with Public Transportation:** Easy access to CTA train stations.
![Word Cloud](https://github.com/pngo1997/Images/blob/main/Transportation.png)  <br /> 
📌 **Key Steps:**
- Consolidate data from various sources.
- Process and clean text-based listing information.
- Apply Agglomerative Clustering to group similar listings.
- Visualize clustering results.
- **Libraries Used:** pandas, numpy, sklearn, spacy, matplotlib, geopy

## 🔥 Recommender System
✅ Implement a **content-based recommendation model.** <br /> 
📌 **Key Steps:** <br /> 
1️⃣ User Input & Preferences: Collects guest count, price, amenities, and text input to extract relevant features. <br /> 
2️⃣ Filtering Listings: Filters listings based on user preferences. <br /> 
3️⃣ Enhancing Rankings: Uses a combined sentiment and cosine similarity score between listings. <br /> 
4️⃣ Personalized Recommendations: Outputs top-k listings from different clusters. <br /> 
5️⃣ Geospatial Visualization: Displays results using an interactive Folium map. <br /> 
- Libraries Used: pandas, numpy, sklearn, folium, spacy, geopandas
  
## 🎯 Results
✅ Best sentiment analysis model: Linear SVC (92.45% accuracy). <br /> 
✅ Clustering provided interpretable themes for better recommendations. <br /> 
✅ Embedding-based similarity scoring improved personalized recommendations. <br /> 

## 🚀 Future Work <br /> 
🔹 Implement dynamic weighting for ranking. <br /> 
🔹 Integrate transformer-based models for better NLP understanding. <br /> 
🔹 Expand the system to include real-time updates and user feedback mechanisms. <br /> 

## 🌎 Links <br /> 
🔹 🏠 Chicago Airbnb Listings Map: 🔗 [📍 Chicago Airbnb Listings Map](https://pngo1997.github.io/Chicago-Airbnb-Listings/) <br /> 
🔹 🚇 Chicago Train Stations Map: 🔗 [📍 View Chicago CTA Map](https://pngo1997.github.io/Chicago-Airbnb-CTA/) <br /> 

👨‍💻 Author independently developed all aspects of the project including data preprocessing, analysis, model development, and report creation.
