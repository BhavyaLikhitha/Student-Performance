# 🎯 Student Performance Analysis using Machine Learning

## 📌 Project Overview
This project is designed to predict student performance based on various factors such as gender, ethnicity, parental education, lunch type, test preparation course, and previous scores. The system uses machine learning models to provide an estimated **Math Score** based on input features.

## 🎯 Objectives
- Perform **Exploratory Data Analysis (EDA)** to understand student performance trends.
- **Preprocess the data** using feature engineering and transformation techniques.
- Train multiple **machine learning models** and evaluate their performance.
- Deploy the model as a **Flask web application**.
- Containerize the application using **Docker**.
- Deploy the project on **AWS (ECR & EC2)**.

## 🛠 Tech Stack Used
- **Programming Language:** Python  
- **Web Framework:** Flask  
- **Containerization:** Docker  
- **Cloud Deployment:** AWS (ECR & EC2)  
- **Version Control:** Git & GitHub  
- **Orchestration:** GitHub Actions (CI/CD)  
- **📊 Data Processing:** Pandas, NumPy  

💡 **Why is this useful?**  
- Helps **educators** identify students who may need additional support.  
- Aids in **policy-making** for improving student outcomes.  
- Provides **insights** into factors affecting student performance.  

---

## 🤖 Machine Learning Models Used  
The following **regression models** were trained and evaluated for predicting student performance:  

1️⃣ **Random Forest Regressor** 🌳  
2️⃣ **Decision Tree Regressor** 🌲  
3️⃣ **Gradient Boosting Regressor** 🚀  
4️⃣ **Linear Regression** 📈  
5️⃣ **XGBoost Regressor** ⚡  
6️⃣ **AdaBoost Regressor** 🎯  

## 🏆 Best Performing Model  
🎉 **Best Model:** **Linear Regression**  
✅ **R² Score (Accuracy):** **0.8778 (87.78%)**  
📊 The **Linear Regression model** outperformed others based on evaluation metrics on both **training** and **testing datasets**.  

## 🔬 Machine Learning Workflow  

🛠 The project follows a structured **ML pipeline**, ensuring modularity and maintainability:  

### 1️⃣ Data Ingestion 📥  
- Reads the dataset (`stud.csv`).  
- Splits data into **train (80%)** and **test (20%)** sets.  
- Stores the processed data in `artifacts/`.  

### 2️⃣ Data Transformation 🔄  
- Handles **missing values** using imputation.  
- Encodes **categorical variables** (Gender, Ethnicity, etc.).  
- Scales **numerical features** (Reading & Writing scores).  
- Saves the preprocessor as a **pickle file (`preprocessor.pkl`)**.  

### 3️⃣ Model Training & Selection 🎯  
- Trains multiple **regression models**:  
  - **Random Forest** 🌳  
  - **Decision Tree** 🌲  
  - **Gradient Boosting** 🚀  
  - **Linear Regression** 📈  
  - **XGBoost** ⚡  
  - **AdaBoost** 🎯  
- **Hyperparameter tuning** using `GridSearchCV`.  
- Selects the **best-performing model** based on `R² score`.  
- Saves the **best model** as a pickle file (`model.pkl`).  

### 4️⃣ Prediction Pipeline 📊  
- Loads the **pre-trained model**.  
- Takes **new input values** from the web app.  
- Predicts **Math Score** dynamically.  


## 📦 Deployment Details  
The project is deployed on **AWS** using containerization for scalability.  

### 🚀 **Docker Containerization**  
- The Flask app is **dockerized** using a `Dockerfile`.  
- The container runs the **ML model and web application**.  

### ☁ **AWS Cloud Deployment**  
✅ **Amazon ECR (Elastic Container Registry)** - Stores the Docker images.  
✅ **Amazon EC2 (Elastic Compute Cloud)** - Hosts the containerized app.  
✅ **CI/CD Automation with GitHub Actions** - Ensures smooth deployment.  

---

## 🌐 Web Application Interface  
The Flask web app allows users to **input student details** and get a **predicted Math Score**.  

### 🖥️ **Frontend UI (home.html)**
- **User-friendly form** to collect input data.  
- **Dynamic prediction display** for real-time results.  

📌 **File:** `templates/home.html`  

### 🔧 **Backend (Flask App)**
- Loads the trained model.  
- Preprocesses the input data.  
- Returns the **predicted Math Score**.  

📌 **File:** `app.py`  

---

## 🎯 Key Takeaways  
✅ **Automated Data Ingestion & Transformation**  
✅ **Hyperparameter Tuned ML Models**  
✅ **Dockerized Flask Application**  
✅ **Cloud Deployment on AWS**  
✅ **87.78% Prediction Accuracy**  

---

🔗 **Developed with ❤️ by Bhavyalikhitha**  
