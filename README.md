# Zomato Restaurant Rating Prediction (Bangalore)

This project focuses on **analyzing restaurant data from Bangalore**, performing **Exploratory Data Analysis (EDA)**, building a **Machine Learning model**, and **deploying it using Flask** to predict restaurant ratings.
---
![Project Overview Diagram](https://github.com/LearnCode801/zomato-rating-prediction/blob/main/img.png)  
*Web App Image.*

## 📌 Project Objective

* Analyze the Zomato dataset to identify factors that influence restaurant ratings.
* Build a regression model to predict ratings using features like cost, location, and cuisine.
* Deploy the trained model using Flask to make live predictions.

---

## 🧾 Dataset Description

* **Source**: Zomato, scraped from Kaggle
* **City**: Bangalore
* **Records**: \~51,000
* **Features**:

  * `name`: Restaurant name
  * `location`: Neighborhood
  * `online_order`: Online delivery available
  * `book_table`: Table booking available
  * `rate`: Customer rating (target)
  * `votes`: Number of votes
  * `cuisines`, `cost`, `dish_liked`, etc.

---

## 🔍 Exploratory Data Analysis (EDA)

The following steps were done during EDA:

* Cleaned missing and inconsistent data
* Converted rating and cost to numeric types
* Removed "NEW" and "nan" ratings
* Identified:

  * Most common cuisines
  * Most liked dishes (e.g., Pasta, Pizza)
  * Distribution of ratings (3.5–4.5 is most common)
  * Popular service types: Delivery, Dine-out

---

## 🤖 Machine Learning Models

After preprocessing (label encoding, null handling, numeric conversion), three models were trained:

| Model                     | R² Score   |
| ------------------------- | ---------- |
| Linear Regression         | 0.22       |
| Random Forest             | 0.88       |
| **Extra Trees Regressor** | **0.93** ✅ |

➡️ **Extra Trees Regressor** was selected as the best model.

---

## 💾 Model Saving (Pickle)

The model is saved using `pickle`:

```python
import pickle

pickle.dump(model, open('model.pkl', 'wb'))
model = pickle.load(open('model.pkl', 'rb'))
```

---

## 🚀 Flask Deployment

A minimal Flask app allows live predictions:

```bash
# To run the app locally
cd app/
python app.py
```

* User enters inputs like online order, location, cuisine, etc.
* App returns the **predicted rating** for a restaurant.

---

## 📈 Sample Prediction Flow

1. User selects:

   * Online order: Yes
   * Cuisine: Indian
   * Cost: 600
   * Location: Koramangala
2. Model processes the input features
3. Outputs predicted rating: `4.1`

---

## 📽️ Demo & Resources

* 📹 [Video Walkthrough](https://lnkd.in/p/dTykrzdh)

---

## 👨‍💻 Tech Stack

* Python (Pandas, NumPy, Seaborn, Scikit-learn)
* Jupyter Notebook
* Flask (for deployment)
* Plotly (for interactive graphs)

---
