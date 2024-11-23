# Leveraging Machine Learning to Better Predict Traffic Density

## Overview
This project focuses on predicting traffic volume using advanced machine learning models, including Support Vector Regressor (SVM), XGBoost, Decision Tree, Random Forest, and Recurrent Neural Networks (RNN). The goal is to enhance traffic management and urban planning through accurate and robust traffic volume predictions.

In addition to predicting traffic volumes, this project incorporates **Conformal Prediction** and **Confidence Intervals** with the XGBoost model to quantify uncertainty in predictions, making them more reliable for real-world applications.

---

## Features and Contributions
- Developed and evaluated models: SVM, XGBoost, Decision Tree, Random Forest, and RNN.
- Transformed non-time-series data into time-series using lagged features to capture temporal dependencies.
- Identified **XGBoost** as the best-performing model based on evaluation metrics.
- Implemented **Conformal Prediction** and **Confidence Intervals** for uncertainty estimation in predictions.
- Conducted a detailed performance analysis, emphasizing the advantages of sequential modeling and uncertainty quantification.

---

## Methodology
### Data Preprocessing and Feature Engineering:
1. **Outlier Removal**: Outliers were identified using statistical techniques (e.g., interquartile range).
2. **Scaling**: Input features and the target variable were normalized using MinMaxScaler.
3. **Sequence Creation**: Sliding windows of 5 timesteps were created to incorporate temporal dependencies.

### Models:
- **Decision Tree & Random Forest**: Baseline models with hyperparameter tuning using GridSearchCV and RandomizedSearchCV.
- **XGBoost**: Basic regression and time series-enhanced models with lagged features.
- **Support Vector Regressor (SVM)**: Applied with Radial Basis Function (RBF) kernel; hyperparameters tuned for better performance.
- **Recurrent Neural Network (RNN)**: Sequential model fine-tuned using Keras Tuner.

---

## Installation Instructions

### Install Dependencies
```bash
pip install -r requirements.txt

```

---

## Dataset
The project uses the [Metro Interstate Traffic Volume dataset](https://www.kaggle.com/code/xreina8/traffic-volume-prediction/input), which contains 48,204 instances and 9 attributes. The data includes features such as:
- Traffic volume
- Weather-related features (temperature, rain, snow, cloud cover)
- Date and time

---

## Limitations and Future Work
### Limitations:
- Static lagged features may not adapt to dynamic traffic patterns.
- Lack of domain-specific features like road type or proximity to urban centers.
- Models rely on historical patterns, limiting performance during extreme or rare events.

### Future Improvements:
- Incorporating dynamic feature engineering with adaptive window sizes.
- Adding domain-specific attributes to improve contextual understanding.
- Exploring ensemble methods for combining strengths of multiple models.

---

## Conclusion
This project demonstrates the effectiveness of machine learning for traffic volume prediction, with **XGBoost** emerging as the best model. By integrating **Conformal Prediction** and **Confidence Intervals**, the framework achieves accurate and reliable predictions, making it highly applicable for real-world scenarios. This work contributes to the advancement of predictive analytics in transportation systems, offering tools to improve urban planning and traffic management.

---

## Authors
- **Maryam Al Shamsi**
- **Shamsa Hamad**
- **Shaikha Al Hosani**

For questions or collaboration, feel free to reach out:
- maryam.alshamsi@mbzuai.ac.ae
- shaikha.al-nahyan@mbzuai.ac.ae
- shaikha.alhosani@mbzuai.ac.ae
