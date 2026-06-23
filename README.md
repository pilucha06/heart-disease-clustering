# heart-disease-clustering
Analizes a dataset of cardiac pacients, using unsupervised clustering, and calculates which group of patients is more at risk only with clinical data, what variables led to that conclusion, and how. 

Objective: This project applies unsupervised machine learning to a dataset (CSV file) of 303 cardiac patients from the UCI Machine Learning Repository. Without using the diagnosis label, a K-Means clustering algorithm identifies three natural patient profiles based on clinical variables such as age, cholesterol, resting blood pressure, and maximum heart rate. The resulting clusters reveal distinct cardiovascular risk profiles, supported by graphics and metrics calculated.

The project follows a five-stage pipeline:
1. Data loading & exploration of meaning: Loaded the UCI Heart Disease dataset using Pandas and inspected its structure, data types, and missing values.
2. Exploratory Data Analysis (EDA): Visualized the distribution of key variables (age, cholesterol, sex) and analyzed correlations between features using a heatmap.
3. Preprocessing: Removed the target column to ensure unsupervised learning, imputed missing values using the median strategy, and standardized all features with StandardScaler.
4. Clustering: Applied the Elbow Method to determine the optimal number of clusters (K=3) and ran K-Means to assign each patient to a risk profile.
5. Visualization & interpretation: Reduced dimensionality with PCA to visualize clusters in 2D, and analyzed the mean clinical values per cluster to characterize each risk profile.

In the end, the K-Means algorithm identified three distinct patient profiles without access to the original diagnosis:

Cluster 1 — Low Risk: Youngest patients (avg. 48.9 years), lowest cholesterol (228.6 mg/dl), and highest maximum heart rate (164.7 bpm). Most favorable cardiovascular indicators.

Cluster 0 — Moderate Risk: Older patients (avg. 58.1 years) with elevated cholesterol (268.9 mg/dl) and moderately reduced maximum heart rate (151.3 bpm).

Cluster 2 — High Risk: Same age range as Cluster 0 (avg. 58.1 years) but significantly higher cardiac stress (oldpeak: 1.9 vs 0.5–0.6 in other clusters) and the lowest maximum heart rate (131.4 bpm), indicating reduced cardiac function.

These profiles were discovered purely from clinical variables, without using the diagnosis column, demonstrating the power of unsupervised learning to reveal structure in medical data.
