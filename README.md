# House Price Data Preprocessing and Analysis
This project involves cleaning, preprocessing, and analyzing a dataset of house listings in Turkey. It focuses on preparing the data for potential modeling, performing exploratory data analysis, 
and generating insights for pricing and property characteristics.

## 📁 Dataset Information

The dataset includes the following features:

* id: House ID (dropped during cleaning)

* fiyat: House price in Turkish Lira (TL)

* oda_salon_sayisi: Number of rooms and living rooms

* net_m2: Net area in square meters

* bina_yasi: Age of the building

* isinma_tipi: Heating system

* krediye_uygunluk: Loan eligibility

* bulundugu_kat: Floor information

* banyo_sayisi: Number of bathrooms

* ilce: District

* nüfus: District population (removed after cleaning)

* eğitim: Education level in the district

* okuma_yazma_bilmeyen: Illiteracy rate in the district (removed after cleaning)

## 🔧 Steps

1.Data Reading and Cleaning

-Turkish character fix in column names

-Dropping unnecessary ID/index columns

-Conversion of data types (e.g., percentage strings to float)

-Typo correction for district and education level values

2.Handling Missing Values

-Imputing based on correlated fields like district

-For features like net_m2 and oda_salon_sayisi, values were imputed using medians

3.Encoding & Grouping

-Education: Lise → 0, Lisans → 1

-Heating and floor levels encoded to numerical values

-Age and district features grouped based on practical thresholds

4.Outlier Detection & Correction

-Visualizations and z-scores were used to detect anomalies

-Small net_m2 values corrected using a decision tree model

5.Data Optimization

-Downcasting numerical columns to reduce memory usage

6.Exploratory Data Analysis

-Visualizations to understand relationships (e.g., price vs m²)

-Identifying trends in student housing, building types, and heating types by district

## 📊 Key Visual Analyses

-Scatter plots showing preprocessing effects on price/m² correlation

-Pie charts revealing apartment distribution by district

-Bar plots comparing heating system prices by district

-Swarm plots for low-cost housing education & district distribution

## 📌 Technologies Used

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn (Decision Tree Regressor)

Google Colab

## 🔍 Notable Insights

Houses with <50 m² likely include errors and were corrected using regression.

District education and floor level influence housing prices significantly.

Merkezi (central) heating is more common in high-rise buildings.

Çankaya and Keçiören districts share many characteristics, so were grouped together.

