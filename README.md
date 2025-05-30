# DSA210 PROJECT

## Project Idea

The objective of this project is to investigate the effects of climate change on agricultural prosuctivity and sustainability by exploring key factors such as temperature, rainfall, CO2 levels, and crop yield. by applying statistical analysis and machine learning methos, the aim is to uncover patterns, correlations, and trends that could help predict future impacts on agriculture. The dataset used for this project is provided by the Kaggle, 'Waqar Ali'. 

---
## Hypothesis

1. **Null Hypothesis (H₀):** Climate variables have no significant impact on crop yield.
2. **Alternative Hypothesis (H₁):** Climate variables (temperature, precipitation, CO2) significantly impact crop yield.

---

## Plan 

1. **Data Collection**
   
   Import and preprocess the dataset from Kaggle, ensuring the correct handling of missing data and standardizing the data formats.
2. **Data Analysis**
   
   Investigate the relationships between climate factors (such as temperature and rainfall) and crop yield through visual tools like scatter plots. To measure the influence of climate variables on crop yield, regression analysis will be employed. Also examine how crop yield trends evolve over time in various regions to understand the role of geographic differences on agricultural productivity. Furthermore, evaluate the effect of extreme weather events on crop yield by correlating these events with changes in yield. Finally, various visualizations, such as line graphs and bar charts will be used to display the trends and relationships identified in the analysis.
 
  
4. **Reporting**

   Create a etailed report summarizing key findings, limitations, and suggestions for future research.
   
---

## Motivation 

Climate change presents a critical threat to global food security and the sustainability of agriculture. It is crucial to understand how changes in temperature, rainfall, and CO2 levels affect crop productivity in order to create effective adaptation strategies. This project integrates data science and environmental research to provide valuable insights for farmers, researchers who are working to reduce the negative impacts of climate change on agriculture. 

---

## Dataset

The dataset used in this project is "Climate Change Impact on Agriculture" provided by Kaggle user 'Waqar Ali'. It includes the following variables:
- **Region**: The location where the data was collected.
- **Year**: The year of record.
- **Average_Temperature**: The average annual temperature (°C).
- **Precipitation**: The total annual rainfall (mm).
- **Crop_Yield**: The crop yield, measured in tons per hectare.
- **Extreme_Weather_Events**: Number of modeled extreme weather occurrences per year.

---
## Machine Learning Analysis
To further explore how various environmental variables affect agricultural productivity, we implemented supervised machine learning models to predict crop yield. As required, linear regression was excluded, and hyperparameter tuning was applied using GridSearchCV.

### Regression Models with Hyperparameter Tuning
- **Random Forest Regressor**
- **Decision Tree Regressor**
- **K-Nearest Neighbors (KNN) Regressor**

Each model was evaluated using:
- **R² Score** – Measures explanatory power of the model  
- **Mean Squared Error (MSE)** – Measures average squared difference between actual and predicted values  
- **Mean Absolute Error (MAE)** – Measures the average magnitude of the errors  
- **Visual analysis** – Actual vs. predicted crop yield plots

## Results of the Analysis

### Univariate Analysis
- **Average Temperature**: Histogram showed a slightly right-skewed distribution, with most values clustered around moderate climates. High temperature values were less frequent.
- **Crop Yield**: Most yields ranged between 2.0 and 4.5 MT/HA, indicating variability in productivity across regions and years.
- **CO₂ Emissions**: Distribution suggested higher emissions in recent years, which may correlate with industrial or population growth.
- **Extreme Weather Events**: The majority of records showed low to moderate occurrences per year.

### Bivariate Analysis
- **CO₂ Emissions vs. Crop Yield**: Scatter plots indicated a complex, slightly nonlinear negative trend between emissions and productivity.
- **Extreme Weather Events vs. Crop Yield**: Boxplots revealed that years with more extreme weather were generally associated with lower yields.
- **Soil Health and Irrigation vs. Crop Yield**: Both factors showed positive correlation with yield—regions with better irrigation and healthier soil had higher productivity.

### Multivariate Analysis
- **Correlation Heatmap**: Key observations included:
  - Negative correlation between extreme weather and crop yield  
  - Positive correlation between soil health and irrigation access with crop yield  
  - Weak correlations among some climate variables and yield, suggesting interaction effects  
- **Combined Influence**: Regions with moderate temperature, stable rainfall, and low extreme weather incidents consistently showed better crop performance.

## Machine Learning Results
The performance of the trained models is summarized below:

| Model            | Mean Squared Error (MSE) | R² Score | Mean Absolute Error (MAE) |
|------------------|--------------------------|----------|----------------------------|
| Random Forest    | 29045.67                 | -0.978   | 102.95                     |
| Decision Tree    | 55545.78                 | -2.782   | 86.21                      |
| KNN              | 20521.98                 | -0.397   | 77.88                      |

**Interpretation**:  
Although KNN had the lowest MSE and MAE, none of the models achieved a positive R² score, indicating limited predictive power. This could be due to data noise, unaccounted categorical effects (e.g. crop type), or limitations in data quality.

### Findings
- **Soil Health** and **Irrigation Access** positively influence yield.  
- **Extreme Weather Events** and **CO₂ Emissions** generally correlate negatively with yield.  
- **Temperature and Precipitation** have mixed or nonlinear effects.  
- Combining multiple favorable environmental factors leads to higher crop performance.

## Conclusion

The proposed project aims to examine the connection between climate variables and agricultural productivity. By identifying key correlations and trends, this analysis can support more informed decision-making for adapting farming practices to the evolving climate. Future research could expand the project by incorporating additional datasets, such as soil quality, fertilizer use, and socio-economic factors, to enhance the accuracy and applicability of predictions.
