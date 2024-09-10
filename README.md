
# SpaceX Falcon 9 Landing Prediction

## Project Overview

This project is part of the IBM Data Science Professional Certification. The objective is to predict the success of SpaceX Falcon 9's first-stage rocket landings. Successfully landing the first stage of Falcon 9 helps SpaceX reuse the rockets, drastically reducing the cost of launches. By predicting landing success, stakeholders can make informed decisions about future space missions, allowing for cost-efficient and reliable space exploration.

### Project Goals
- Predict the outcome of Falcon 9 first-stage rocket landings.
- Analyze the factors influencing landing success rates.
- Use historical data to build machine learning models for predictive analysis.

## Data Sources
1. **SpaceX API**: Used to collect launch data for Falcon 9 rockets.
2. **Web Scraping**: Employed to gather additional details on launches from static web pages.

## Methodology
The project is divided into several key steps:

1. **Data Collection**:
   - Data is collected using the SpaceX REST API and web scraping.
   - A combination of custom logic and Pandas was used to clean and structure the dataset for further analysis.

2. **Data Wrangling**:
   - Missing values were handled using `.fillna()`.
   - A `Class` column was created to represent successful (1) and unsuccessful (0) landings based on the `Outcome` field.

3. **Exploratory Data Analysis (EDA)**:
   - SQL queries were employed to explore the data, revealing insights like total payload mass by NASA and average payload mass by booster version.
   - Various visualizations such as bar charts, scatter plots, and line charts were created using Pandas, Matplotlib, and Seaborn.

4. **Interactive Data Visualizations**:
   - **Geospatial Analysis**: Created interactive maps with Folium to visualize launch sites.
   - **Plotly Dash Dashboard**: Built an interactive dashboard with dropdowns and sliders to explore the relationships between payload mass, flight success, and launch sites.

5. **Predictive Analysis (Classification)**:
   - Various classification models were developed to predict the success of rocket landings.
   - Models included Logistic Regression, Decision Trees, K-Nearest Neighbors (KNN), and Support Vector Machines (SVM).
   - Hyperparameter tuning was performed using `GridSearchCV` to optimize model performance.

## Key Findings
1. **EDA Findings**:
   - As the number of flights increases, the success rate for specific launch sites (e.g., CCAFS SLC 40) improves.
   - Orbits such as **ES-L1**, **SSO**, **HEO**, and **GEO** showed 100% success rates.
   - Success rates of Falcon 9 landings have steadily increased since 2010.

2. **Predictive Model Results**:
   - **Logistic Regression** achieved the highest accuracy at 83.33%.
   - Decision Trees, after hyperparameter tuning, achieved the best performance with an accuracy of 88.88%.
   - The models performed well, with minor misclassifications typically involving overestimation of successful landings.

## Technologies Used
- **Programming Languages**: Python
- **Libraries**: 
  - Data Wrangling: Pandas, NumPy
  - Data Visualization: Matplotlib, Seaborn, Folium, Plotly Dash
  - Machine Learning: Scikit-Learn (Logistic Regression, Decision Trees, KNN, SVM)
- **SQL**: Used for exploratory data analysis with complex queries to extract insights.

## How to Use
1. Clone the project repository from GitHub:
   ```bash
   git clone https://github.com/JavierOrdonezA/SpaceX-Falcon9-Landing-Prediction.git

## Conclusion

This project provides insights into the factors affecting SpaceX Falcon 9 landing outcomes and 
demonstrates the power of machine learning in predicting these outcomes. The models developed 
can help improve cost analysis and decision-making for future space missions.

