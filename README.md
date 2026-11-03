# 🍔 Food Delivery Time Prediction Using Machine Learning

### An End-to-End Machine Learning Project for Intelligent Food Delivery Time Estimation

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Regression-orange)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Modeling-yellow?logo=scikitlearn)
![Gradio](https://img.shields.io/badge/Gradio-Deployment-orange?logo=gradio)

---

## 📌 Project Overview

Food delivery platforms need accurate delivery time estimates to improve customer satisfaction and operational efficiency.

This project develops a **Machine Learning-based Food Delivery Time Prediction System** that estimates delivery time using factors such as traffic conditions, weather, road distance, vehicle type, rider experience, and restaurant preparation time.

The project covers the complete Machine Learning workflow, from data preprocessing and exploratory data analysis to model development, evaluation, and deployment using Gradio.

## 🎯 Problem Statement

To develop a supervised Machine Learning regression model that predicts food delivery time (`Time_taken_min`) based on historical delivery data and relevant operational features.

## 📊 Dataset Description

The dataset contains information about food orders, delivery partners, routes, and environmental conditions.

**Input Features:**

| Feature | Description |
|---|---|
| Order_Hour | Hour of order placement |
| Weather | Weather conditions |
| Vehicle_Type | Delivery vehicle type |
| Rider_Experience_Years | Rider experience |
| Order_Items | Number of items |
| Preparation_Time_Min | Restaurant preparation time |
| Road_Distance_km | Delivery distance |
| Traffic_Level | Traffic conditions |
| Number_of_Signals | Number of traffic signals |

**Target Variable:** `Time_taken_min` – Total delivery time in minutes.

*Note: Average_Speed_kmph was excluded to avoid potential data leakage.*

## 🔄 Machine Learning Workflow

The project follows these steps:

```text
       Dataset Loading
              |
              ▼
       Data Understanding
              |
              ▼
      Data Cleaning & EDA
              |
              ▼
       Feature Selection
              |
              ▼
      Data Preprocessing
     (Encoding & Scaling)
              |
              ▼
        Train-Test Split
             (80:20)
              |
              ▼
       Model Development
              |
              ▼
        Model Evaluation
              |
              ▼
      Hyperparameter Tuning
              |
              ▼
        Model Selection
              |
              ▼
         Model Saving
              |
              ▼
       Gradio Deployment
              |
              ▼
       Final Prediction
```

## 🔍 Exploratory Data Analysis (EDA)

Performed EDA to understand data patterns and relationships between delivery time and different features.

Key analyses included:
- Delivery time distribution.
- Traffic and weather impact on delivery time.
- Relationship between road distance and delivery time.
- Delivery time across different vehicle types.
- Peak-hour delivery analysis.
- Correlation analysis.

## ⚙️ Data Preprocessing

The following techniques were implemented:

- Missing value and duplicate checks.
- Outlier examination using the IQR method.
- Feature selection to identify relevant predictors.
- One-Hot Encoding for categorical variables.
- StandardScaler for numerical features.
- 80:20 train-test split with `random_state=42`.

## 🤖 Machine Learning Algorithms

Implemented and compared multiple regression algorithms:

| Algorithm | Purpose |
|---|---|
| Dummy Regressor | Baseline comparison |
| Linear Regression | Linear relationship modelling |
| Decision Tree Regressor | Capturing nonlinear patterns |
| Random Forest Regressor | Ensemble-based prediction |
| Gradient Boosting Regressor | Sequential error reduction |

**Evaluation Metrics:**
- MAE – Mean Absolute Error
- RMSE – Root Mean Squared Error
- R² Score – Coefficient of Determination
- Five-fold Cross-Validation

## 🏆 Model Performance

The Random Forest Regressor achieved the following performance on the test dataset:

| Evaluation Metric | Result |
|---|---:|
| MAE | 3.604 |
| RMSE | 5.054 |
| R² Score | 0.980 |

**Key Achievement:** Achieved approximately **98% R² score**, demonstrating strong predictive performance on the test dataset.

Random Forest was selected based on its test performance. Hyperparameter tuning was also explored using `RandomizedSearchCV`.

## 🌐 Model Deployment Using Gradio

An interactive Gradio application was developed to allow users to enter delivery-related details and obtain predicted delivery time in minutes.

Users can provide:
- Order details and preparation time.
- Weather and traffic conditions.
- Vehicle type and rider experience.
- Road distance and number of signals.

The application generates an estimated delivery time based on the trained model.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming |
| Pandas & NumPy | Data manipulation |
| Matplotlib & Seaborn | Visualization |
| Scikit-learn | Machine Learning |
| Joblib | Model saving |
| Gradio | Application deployment |
| Jupyter Notebook / Google Colab | Development environment |
| Git & GitHub | Version control |

## 📂 Project Structure

```text
food-delivery-time-prediction-ml/
│
├── Machine_Learning_Project(Food_Delivery_Prediction).ipynb
├── Food_Delivery_Time_Prediction.csv
├── food_delivery_model.pkl
└── README.md
```

## 🚀 How to Run the Project

**1. Clone the repository**

```bash
git clone https://github.com/YOUR-USERNAME/food-delivery-time-prediction-ml.git
```

**2. Navigate to the project folder**

```bash
cd food-delivery-time-prediction-ml
```

**3. Install the required libraries**

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib gradio jupyter
```

**4. Open Jupyter Notebook**

```bash
jupyter notebook
```

Open the project notebook and execute the cells sequentially to perform preprocessing, model training, evaluation, and Gradio deployment.

## 💡 Key Learnings & Future Enhancements

**Key Learnings:**
- Understanding real-world regression problems.
- Performing EDA and data preprocessing.
- Implementing and comparing multiple ML algorithms.
- Evaluating models and performing hyperparameter tuning.
- Saving trained models and developing interactive applications.

**Future Enhancements:**
- Integrate real-time traffic and weather APIs.
- Implement GPS-based delivery tracking.
- Explore advanced boosting algorithms.
- Deploy the application as a cloud-based service.


## 👩‍💻 Author

**Sharanya Vemula**

Machine Learning | Data Science | Python

GitHub: https://github.com/Sharanya-Vemula

---

⭐ If you find this project useful, consider giving the repository a star!

Learning by building. Growing through experimentation. Turning data into meaningful solutions.
