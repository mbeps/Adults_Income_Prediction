# **Adult Income Prediction**

Welcome to the **Adult Income Prediction Project**. This endeavor focuses on predicting an individual's income bracket based on various demographic and personal details. Utilizing the renowned [Adult Income dataset from the UCI Machine Learning Repository](http://www.cs.toronto.edu/~delve/data/adult/desc.html), our primary goal is to determine if a person earns `<=50K` or `>50K` annually.

In this project, we employ the `RandomForestClassifier`, a robust ensemble learning method, to capture the intricate relationships within the data. Through meticulous hyperparameter tuning, our best model achieves an accuracy of approximately `85.6%` on the test set. Key features like `age`, `educational-num`, and `capital-gain` surfaced as significant determinants of an individual's income.

This repository provides insights into our methodology, results, and the importance of each feature in influencing the prediction. It serves as a foundational example of data preprocessing, machine learning practices, and model interpretation.

Dive in to explore the nuances of income prediction and the factors that influence it!

## **Data Preprocessing: One-Hot Encoding**

**One-Hot Encoding** is a technique used to convert categorical variables into a format that can be provided to machine learning algorithms to do a better job in prediction. Instead of having a single column with n categories, one-hot encoding creates n columns, each representing a category and marked as `0` or `1` depending on the value for that instance.

In this project, one-hot encoding was employed because machine learning algorithms, especially the ones based on mathematical equations like linear regression, require numerical input features. Using this technique ensured that the categorical values in our dataset were transformed into a suitable format without introducing ordinal relationships that might not exist.

## **Model Choice: Random Forest Classifier**

The **Random Forest classifier** is an ensemble learning method that builds multiple decision trees during training and outputs the class that is the mode of the classes output by individual trees for classification tasks. It brings randomness into the model, which makes it robust against overfitting.

Random Forests inherently work well with one-hot encoded data. When features are one-hot encoded, a tree in the Random Forest can make a split on a specific category by using just one of these binary features. This allows the model to consider each category independently, accommodating well for the nature of the encoded features.

## **Hyperparameter Tuning**

**Hyperparameter tuning** is the process of searching for the best set of hyperparameters that produce the most optimal model for a given dataset. Instead of accepting the default values or using educated guesses to fill in hyperparameters, we systematically search for the best combination to enhance the model's performance.

In this project, **Grid Search** was employed for hyperparameter tuning. Grid Search works by defining a grid of hyperparameters and then exploring a model's performance for each point in the grid. This ensures we don't miss out on any potential combinations that might enhance our model's predictive capability.

# **Running Notebook Locally**
These are simple steps to run the notebook locally. 
Jupyter is required.

## 1. **Clone the Project Locally**
```sh
git clone https://github.com/mbeps/House_Price_Prediction.git
```

## 2. **Set Up Environment**

### Using Anaconda (Preferred)
If you have Anaconda installed, create a new environment and activate it. Once active, install the required packages.

### Using Poetry (Alternative for non-Anaconda users)
1. Ensure you have Python 3.10 installed.
2. If you are using Poetry and do not have Anaconda, install the dependencies:
```sh
poetry install
```

## 3. **Run the Project**
After setting up the environment and installing all dependencies, navigate to the project's root directory and run the main notebook. 

> Note: Adjust the specific steps, commands, or any other requirements based on the nature of your project or any additional configurations that might be needed.
