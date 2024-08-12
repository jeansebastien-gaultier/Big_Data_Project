# Big Data Analytics for Airline Industry

## Overview

This project was completed as part of the ADSP 31013 - Big Data course for my Master of Science degree. The project investigates how Big Data Analytics can be utilized by airline companies to enhance operational efficiency, improve customer satisfaction, and reduce costs associated with flight delays. 

## Project Objectives

The project focused on four key objectives:

1. **Association Mining for Targeted Marketing**: Identify traveler behavior patterns by uncovering correlations between airports and preferred airlines. This helps airline marketing teams tailor strategies for route planning and passenger engagement.
   
2. **Graph-Based Analysis for Delay Reduction**: Use delay-integrated network representation to analyze delay propagation across airports and airlines. This aids airline operations teams in identifying influential nodes and routes to minimize delays.

3. **Flight Delay Prediction for Improved Operations**: Develop predictive models to forecast flight delays, empowering airline operations and passenger service teams to proactively manage schedules and provide timely information.

4. **Predictive Maintenance for Optimal Aircraft Rotation**: Forecast maintenance needs to optimize aircraft rotation schedules, ensuring safety, reliability, and cost-effectiveness in fleet management.

## Tools and Technologies

- **Big Data Tools**: The analysis was performed using PySpark and SparkSQL, with data processed in Apache Hadoop.
- **Machine Learning Models**: Classification models including Random Forest, Gradient Boosted Trees, and Support Vector Machines were used for delay prediction.
- **Graph Theory**: Applied graph theory algorithms to model and analyze flight delay propagation across airports.

## Data Source

The dataset was sourced from Kaggle and includes detailed flight information from January 2018 to December 2022, totaling over 29 million records. The dataset includes various attributes such as flight delays, cancellations, and airport information.

- **Data Size**: 11GB in CSV and Parquet formats.
- **Challenges**: Data quality issues like missing values, outliers, and complex relationships between variables.

## Methodology

### Data Preprocessing

- **Feature Engineering**: Categorical data was transformed using String Indexing and One-Hot Encoding. New features like 'IsWeekend' were created to enhance model performance.
- **Feature Scaling**: Numeric features were scaled to ensure consistent impact on the models.
- **Feature Selection**: Selected features relevant to delay prediction, such as 'DepDelayMinutes,' 'Distance,' and 'IsWeekend.'

### Machine Learning Models

- **Flight Delay Prediction**: 
  - **Models**: Random Forest, Gradient Boosted Trees, and SVM.
  - **Metrics**: The best-performing model was the Gradient Boosted Tree with an AUC of 0.602, F1 Score of 0.744, and Accuracy of 0.824.

- **Predictive Maintenance**: 
  - A regression model was used to predict remaining hours before maintenance is needed, considering factors like delay minutes, total taxi time, and flight hours.

### Graph Theory Analysis

- **Delay Reduction**: Incorporated delays as weights in the graph to identify influential airports and minimize operational disruptions.
- **Route Optimization**: Analyzed indirect flight paths and connectivity between airports to optimize routes and introduce new flight schedules.

### Association Mining

- **Targeted Marketing**: Identified strong associations between airlines and airports, particularly between American Airlines and ORD (Chicago O'Hare), to aid in strategic route planning.

## Results and Conclusion

The project delivered significant insights that can be used to enhance the operational strategies of airlines, potentially reducing the $28 billion annual delay costs estimated by the FAA/Nextor. The integration of machine learning models, graph theory, and association mining offers a comprehensive approach to tackling the complex challenges faced by the airline industry.
