# E-Commerce-Consumer-Behavior-Predictor-End-to-End-Machine-Learning-Pipeline.ipynb

This repository builds an end-to-end Machine Learning pipeline to analyze and predict user conversion behavior (views, additions to cart, removals, and purchases) based on multi-month real-time e-commerce logs.

## 🚀 Project Overview
- **Objective**: Predict consumer activity (`event_type`) utilizing transactional pricing, timing, brand attributes, and product IDs.
- **Scale**: Consolidated over **5.29 Million user action logs** across 4 months.
- **Engineering Pattern**: Developed as a modular, object-oriented pipeline class (`ECommercePredictorPipeline`) prepared for REST API integration.

## 🛠️ Tech Stack
- **Data Manipulation**: Pandas, NumPy
- **Visualization**: Seaborn, Matplotlib
- **Modeling & Evaluation**: Scikit-Learn (Random Forest, Decision Trees, KNN, Metrics modules)

## 📊 Performance Insights
- Our **Random Forest Classifier** achieved the highest baseline prediction score of **~48.5%** on the validation split.
- **Key Features**: Product pricing and timing attributes proved to have the highest predictive weight in user conversion paths.

## 💻 How to Use
```python
# Initialize and run pipeline
predictor = ECommercePredictorPipeline()
predictor.fit(training_dataframe)
predictions = predictor.predict(new_data)
print(predictions)
