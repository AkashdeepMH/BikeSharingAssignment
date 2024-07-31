# Multiple Linear Regression model for the prediction of demand for shared bikes using BoomBikes Dataset

# Project Name
This assignment is a programming assignment wherein you have to build a multiple linear regression model for the prediction of demand for shared bikes.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

## General Information
Background
This project aims to predict the demand for shared bikes using multiple linear regression models. BoomBikes, a US-based bike-sharing provider, experienced significant revenue declines during the Corona pandemic. Understanding the factors influencing bike rental demand can help BoomBikes develop strategic plans to increase revenue post-pandemic.

  _Business Goal As mentioned in Upgrad.com assignment section:_
We are required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market. 

### Dataset Used
The dataset used in this project is a bike-sharing dataset from BoomBikes, a US bike-sharing provider. It contains daily records of bike rentals, along with various features that potentially influence the demand for bike rentals. The dataset includes the following fields:

- **instant**: Record index
- **dteday**: Date
- **season**: Season (1: spring, 2: summer, 3: fall, 4: winter)
- **yr**: Year (0: 2018, 1: 2019)
- **mnth**: Month (1 to 12)
- **holiday**: Whether the day is a holiday or not
- **weekday**: Day of the week
- **workingday**: Whether the day is neither weekend nor holiday
- **weathersit**: Weather situation (1: Clear, 2: Mist, 3: Light snow/rain, 4: Heavy rain/snow)
- **temp**: Temperature in Celsius
- **atemp**: Feels-like temperature in Celsius
- **hum**: Humidity
- **windspeed**: Wind speed
- **casual**: Count of casual users
- **registered**: Count of registered users
- **cnt**: Count of total rental bikes, including both casual and registered users

This dataset captures the various environmental and temporal factors that affect bike rentals, making it suitable for building a predictive model to understand and forecast demand.

## Conclusions
### Conclusions from the Analysis

1. **Variable Significance**: The analysis demonstrated that several variables significantly affect bike rental demands. Key predictors include temperature (`temp`), year (`yr`), weather conditions (`weathersit`), and specific months and seasons. This emphasizes the need to consider both temporal and weather-related factors in demand forecasting models for bike rentals.

2. **Yearly Increase in Demand**: Including the `yr` variable in the model confirmed that there is a noticeable increase in bike rentals from year to year, reflecting the growing popularity of the bike-sharing system. This insight is crucial for strategic planning and scaling operations to accommodate the increasing customer base.
![image](https://github.com/user-attachments/assets/d8f80b47-c36a-4186-b72e-9d04ec8b088e)

3. **Impact of Weather Conditions**: Weather conditions play a critical role in bike rental patterns. Bad weather conditions (like rain and snow) significantly decrease the demand, whereas clear and mild weather encourages more usage. This finding suggests that weather forecasts should be integrated into the demand prediction models for more accurate forecasting.
![image](https://github.com/user-attachments/assets/145d9656-e281-40f1-bc2e-654dcd79b4bd)

4. **Model Optimization and Refinement**: The analysis involved building multiple models (Model 1 to Model 5) to progressively refine the predictors and improve the model performance:
    - **Model 1**: Included all features and served as a baseline. It showed the highest R-squared value but likely suffered from overfitting due to the inclusion of all variables without selection.
    - **Model 2**: Utilized Recursive Feature Elimination (RFE) to select key features. This model had a lower R-squared value compared to Model 1, indicating the removal of some potentially useful features.
    - **Model 3**: Further refined by removing features with high Variance Inflation Factor (VIF) values to address multicollinearity. This model showed improved performance over Model 2.
    - **Model 4**: Further refinement based on both p-values and VIF, leading to a more stable model with lower multicollinearity.
    - **Model 5**: The final refined model with the lowest VIF and significant p-values, providing a balance between complexity and performance with an R-squared value close to Model 1 but with better generalizability.
![image](https://github.com/user-attachments/assets/85e80abe-9d6a-467c-ac0b-a11fd8132094)

The progression from Model 1 to Model 5 highlighted the importance of feature selection and multicollinearity handling in building a robust predictive model. Each step in the refinement process contributed to improving the model’s accuracy, stability, and interpretability.

## Technologies Used
### Libraries and Versions Used in This Project

To ensure reproducibility and compatibility of the results, it is crucial to mention the versions of the libraries used in this project. Below are the libraries and their respective versions:

- **pandas - version 1.0**: Used for data manipulation and analysis. It provides data structures and functions needed to manipulate structured data seamlessly.
- **numpy - version 1.18**: Utilized for numerical computations. It supports large multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays.
- **statsmodels - version 0.11**: Employed for building and evaluating the regression models. It provides classes and functions for the estimation of many different statistical models, as well as for conducting statistical tests and statistical data exploration.
- **sklearn (scikit-learn) - version 0.22**: Used for feature selection and evaluation. It includes simple and efficient tools for data mining and data analysis, built on NumPy, SciPy, and matplotlib.
- **matplotlib - version 3.1**: Used for creating static, interactive, and animated visualizations in Python. It provides an object-oriented API for embedding plots into applications.
- **seaborn - version 0.10**: A statistical data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.

By specifying these versions, users can recreate the environment and obtain consistent results. It is recommended to install these specific versions using a package manager like pip to avoid discrepancies due to version differences.

## Acknowledgements
I would like to thank the folowing for teaching important concepts needed to work on this BoomBikes Bike Share Prediction dataset:
Kshitij Jain (Director at upGrad), Mirza Rahim Baig(Lead Business Analyst at Flipkart) And all other educators affiliated to IITB or Upgrad.com
Gratitude to All the programmers/scholars who have contributed to the field of Machine learning and created libraries in python to make this repository possible.

### Project Credits and References

- **Inspiration**: This project was inspired by the need to understand and predict bike rental demand for BoomBikes, a US bike-sharing provider that experienced a significant dip in revenue during the Corona pandemic.
  
- **References**:
  - Residual Analysis and Predictions from: [UpGrad AI ML Masters Course](https://learn.upgrad.com/course/5800/segment/52631/312288/946786/4724982)
  - Variable Selection using RFE from: [UpGrad AI ML Masters Course](https://learn.upgrad.com/course/5800/segment/52631/312288/946788/4725004)

These resources provided valuable guidance and methodologies for performing residual analysis, predicting bike rental demand, and selecting variables using Recursive Feature Elimination (RFE). The techniques and insights gained from these references were instrumental in developing the regression model and refining it for better performance and accuracy.

## Contact
Created by [@AkashdeepMH] - feel free to contact me!
