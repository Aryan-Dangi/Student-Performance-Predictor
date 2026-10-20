# Student Performance Prediction Using Machine Learning

## 1. Project Overview

This project predicts a student's final mathematics grade using
Machine Learning.

It uses academic information such as:
- Weekly study time
- Previous class failures
- Number of absences
- First period grade
- Second period grade

The project uses Linear Regression to estimate the final grade
on a scale of 0 to 20.

## 2. Problem Statement

Students' academic performance can be affected by their study
habits, attendance, and previous academic results.

This project develops a simple Machine Learning model to
estimate final student grades using these factors.

## 3. Objectives

- Apply supervised Machine Learning.
- Understand regression algorithms.
- Train and test a model using real-world data.
- Evaluate predictions using MAE and R² Score.
- Predict grades for new student inputs.

## 4. Dataset

Dataset: Student Performance Dataset

Source:
https://archive.ics.uci.edu/dataset/320/student+performance

The project uses the mathematics dataset, student-mat.csv.

Selected features:
- studytime: Weekly study time category (1-4)
- failures: Previous class failures
- absences: Number of school absences
- G1: First period grade
- G2: Second period grade

Target:
- G3: Final mathematics grade (0-20)

The dataset is downloaded automatically by train.py.

## 5. Algorithm Used

Linear Regression is a supervised Machine Learning algorithm
used to predict continuous numerical values.

It learns the relationship between input features and the
target grade from the training data.

## 6. Project Workflow

1. Download the dataset.
2. Select relevant features.
3. Divide the dataset into training and testing sets.
4. Train the Linear Regression model.
5. Predict grades for the test dataset.
6. Evaluate the model using MAE and R² Score.
7. Save the trained model.
8. Accept user input and predict a student's final grade.

## 7. Technologies Used

- Python
- Pandas
- Scikit-learn
- Pickle
- UCI Machine Learning Repository

## 8. Installation

Install Python 3.10 or newer.

Install the required libraries:

pip install pandas scikit-learn

An internet connection is required when downloading the dataset.

## 9. How to Run

Step 1: Open the project directory in VS Code.

Step 2: Train the model:

python train.py

Step 3: Run the prediction program:

python main.py

Step 4: Enter the requested academic information.

Step 5: View the predicted final grade and its estimated
pass/fail category.

Running train.py generates student_model.pkl automatically.

## 10. Model Evaluation

Mean Absolute Error (MAE):
Measures the average absolute difference between actual
and predicted grades. Lower values are better.

R² Score:
Measures how well the model explains the variation in
the target grades. A score closer to 1 generally indicates
better performance on the evaluated dataset.

Actual results are printed when train.py executes.

## 11. Limitations

- Predictions are estimates, not guaranteed grades.
- The dataset represents students from two Portuguese schools.
- Results may not generalize to every educational institution.
- Previous grades are strong predictors of final grades, so
  performance may be lower when previous grades are unavailable.
- The model does not establish that study time or attendance
  directly causes a particular grade.

## 12. Future Improvements

- Compare Linear Regression with Decision Tree Regression.
- Add visualizations of student performance.
- Develop a web interface for predictions.
- Explore additional features that may help explain performance.

## 13. Conclusion

This project demonstrates a complete basic Machine Learning
workflow, including dataset loading, model training, testing,
evaluation, and prediction.

It shows how regression can be applied to an educational
problem using real-world data.
## Web Interface

The project includes a simple web interface developed using Flask.
Users can enter academic details through a form and view the
predicted final grade in their browser.

### Run the Application

1. Install dependencies:

   pip install flask pandas scikit-learn

2. Train the model:

   python train.py

3. Start the Flask server:

   python main.py

4. Open http://127.0.0.1:5000 in your browser.

The model is trained separately and saved as student_model.pkl.
The Flask application loads the saved model to make predictions.
