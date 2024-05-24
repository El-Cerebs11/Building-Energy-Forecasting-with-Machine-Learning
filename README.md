
### Building Energy Consumption Forecasting

#### Objective
The primary objective of this project is to predict the monthly energy budget of a building. This involves using historical weather data and energy consumption records spanning three years to forecast energy costs.

#### Data Overview
- **Weather Data**: 3 years of historical data
- **Energy Consumption Data**: 3 years of building electricity consumption records
- **Energy Cost**: Monthly energy cost data

#### Data Analysis and Preprocessing
1. **Data Loading**: The building electricity consumption data was loaded and checked for missing values. No missing values were found.
2. **Correlation Analysis**:
   - Utilized Pearson's correlation coefficient to identify the strength of linear associations between variables.
   - **Key Findings**:
     - Temperature (Temp) shows a strong positive correlation with building electricity demand.
     - Relative Humidity (U) and Hourly Sum of Precipitation (RH) are highly negatively correlated with energy demand and are also multicollinear, indicating that either can be used for prediction purposes.
3. **Feature Visualization**:
   - Energy demand varies with temperature, with visible seasonal variations.
   - Negative linear correlation between Relative Humidity and Energy Consumption can be explained by its high negative correlation with temperature (-0.57).

#### Feature Selection
- Features were selected based on their strong correlation with the target variable (energy consumption).
- To avoid multicollinearity, input features with strong correlations among themselves were removed. Multicollinearity can cause one predictor variable in a multiple regression model to be linearly predicted from others with high accuracy.

#### Exploring Non-Linear Correlations
- **Spearman's Rank-Order Correlation Coefficient**: Used to explore the monotonic relationships between energy consumption and other variables like Hour and Month.

#### Additional Findings
- Maximum error allowed in the function was set to ensure robust modeling.
- The tolerance for points falling outside the error boundaries (ϵ) was adjusted to improve model accuracy.
- Considered the influence of single points on the model to enhance prediction reliability.

#### Figures
- **Figure 1**: Visualization of temperature vs. energy consumption.
- **Figure 2**: Correlation heatmap of weather features and energy consumption.
- **Figure 3**: Seasonal variations in energy consumption.
- **Figure 4**: Energy consumption trends over months.
- **Figure 5**: Impact of humidity on energy consumption.
- **Figure 6**: Linear regression model fit.
- **Figure 7**: Residual analysis of the model.
- **Figure 8**: Non-linear correlation analysis between energy and hour.
- **Figure 9**: Non-linear correlation analysis between energy and month.
- **Figure 10**: Feature importance plot.
- **Figure 11**: Cross-validation results.
- **Figure 12**: Model performance metrics.
- **Figure 13**: Error distribution plot.
- **Figure 14**: Final model predictions vs. actual energy consumption.

#### Conclusion
This notebook provides a comprehensive approach to forecasting building energy consumption by leveraging historical weather and energy data. The correlation analyses and feature selection steps are crucial in building an effective predictive model, accounting for both linear and non-linear relationships.

---

This summary serves as a conclusive overview of the contents and methodologies applied in the notebook, designed for inclusion in a GitHub repository README file.
