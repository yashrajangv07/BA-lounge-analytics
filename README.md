# BA-lounge-analytics
# British Airways Customer Booking – Random Forest Classifier

📌 Project Overview

This project uses a **Random Forest Classifier** to predict whether a **British Airways customer completes a booking** based on customer, flight, and service-related features. The model is trained on historical booking data and evaluated using both a **hold-out test set** and **cross-validation**.

The project demonstrates a complete **end-to-end machine learning workflow**, from preprocessing to model interpretation.



 🎯 Objectives

* Predict `booking_complete` using customer booking data
* Apply a **Random Forest Classifier** for robust performance
* Evaluate accuracy using test data and cross-validation
* Identify the **most important features** influencing booking completion



🧠 Model Details

* **Algorithm:** Random Forest Classifier (`sklearn.ensemble`)
* **Number of Trees:** 200
* **Max Depth:** None (fully grown trees)
* **Why Random Forest?**

  * Handles mixed feature types well
  * Reduces overfitting compared to single decision trees
  * Provides feature importance for interpretability


 📂 Project Structure


├── data/
│   └── customer_booking.csv
├── notebook/
│   └── ba_random_forest.ipynb
├── README.md
└── requirements.txt




📊 Dataset

* **File:** `customer_booking.csv`
* **Encoding:** ISO-8859-1
* **Target Variable:**

  * `booking_complete` (1 = booking completed, 0 = not completed)

Preprocessing Steps

* Missing values filled with `0`
* Categorical variables encoded using **one-hot encoding** (`pd.get_dummies`)
* First category dropped to avoid multicollinearity



⚙️ Machine Learning Pipeline

1. Load dataset using Pandas
2. Handle missing values
3. One-hot encode categorical features
4. Split data into training (80%) and testing (20%) sets
5. Train Random Forest Classifier
6. Evaluate model accuracy
7. Perform 5-fold cross-validation
8. Analyze feature importance



## 📈 Model Evaluation

* **Test Set Accuracy:** Calculated using `accuracy_score`
* **Cross-Validation:** 5-fold cross-validation using `cross_val_score`

Cross-validation provides a more reliable estimate of model performance and confirms model stability.


## 🔍 Feature Importance

The Random Forest model provides feature importance scores, allowing us to identify which variables most strongly influence booking completion.

Top features are extracted and sorted to understand customer behavior and booking patterns.


🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Jupyter Notebook

🚀 How to Run

Install dependencies:

bash
pip install -r requirements.txt


Run the notebook:


Or open the Jupyter notebook for step-by-step execution.


📄 License

This project is intended for **educational and portfolio purposes only**.

🙌 Acknowledgements

Project inspired by real-world airline customer booking behavior and applied machine learning techniques.
