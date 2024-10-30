---

# End-To-End Deployment of Zomato Restaurant Ratings Prediction

## Project Overview

This project aims to build and deploy a machine learning model to predict restaurant ratings based on various features in the Zomato dataset. By conducting Exploratory Data Analysis (EDA) and building an effective predictive model, the project enables Zomato restaurants to estimate their ratings. The model is deployed via Flask, allowing live predictions through a web application.

## Main Objectives

1. Conduct extensive Exploratory Data Analysis (EDA) on the Zomato dataset.
2. Build a machine learning model that predicts restaurant ratings based on specific features.
3. Deploy the model using Flask for live predictions of restaurant ratings.

## Project Steps

### A. EDA and Model Building
1. Load the dataset and perform necessary EDA in Jupyter Notebook or Google Colab.
2. Develop a machine learning algorithm to predict restaurant ratings.
3. Save the trained model using `pickle` for later use.

### B. Deployment
1. Use an IDE of your choice, such as PyCharm or Sublime Text, for deploying the model.
2. Set up the development environment by installing [PyCharm](https://www.jetbrains.com/pycharm/download/) or another preferred IDE.

#### Virtual Environment Setup (Optional but Recommended)
To prevent library dependency conflicts, it’s recommended to create a virtual environment. Use the following resources for guidance:
- [Creating Virtual Environments](https://bit.ly/2CwnTfo)
- [Virtual Environment Setup in PyCharm](https://bit.ly/32pe8uL)

3. Install Flask:
   ```bash
   pip install flask
   ```

4. File Structure:
   - **Model.py**: Code for training and saving the prediction model.
   - **Data.csv**: Cleaned dataset for analysis and model training.
   - **Template Folder**: Contains the HTML and CSS files for the web application interface.
   - **App.py**: Flask API to receive restaurant details and return predicted ratings.

## Project Files and Descriptions

- **Model.py**: Contains code for building and saving the model to predict restaurant ratings.
- **Data.csv**: Pre-processed dataset saved for model training.
- **Template Folder**: Holds HTML and CSS files for the web application's front end.
- **App.py**: Flask API file that handles incoming data, processes it through the model, and returns the predicted rating.

## Setting Up Your Project

1. **Create the required project files**:
   - **app.py**: Main application file to handle API requests.
   - **Template Folder**: Create a `templates` directory to hold HTML files.
   - **Static Folder**: Create a `static` directory for CSS files.

2. **Adding Project Files**:
   - In `templates` directory, add your HTML file for the web app.
   - In `static` directory, add the CSS file to style the application.

3. **Running the Project**:
   - Run `app.py` to start the Flask server.
   - Use the web interface to input restaurant details and receive predicted ratings.

---
