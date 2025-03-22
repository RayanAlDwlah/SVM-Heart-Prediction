# SVM Heart Disease Prediction

## Project Overview
This project focuses on analyzing and predicting heart disease using a Support Vector Machine (SVM) classifier. The dataset includes detailed patient information such as age, sex, chest pain type, and other relevant features. The goal is to provide insights into the factors contributing to heart disease and build a predictive model for estimating the likelihood of heart disease.

## Dataset Description
The dataset `heart.csv` contains the following features:
- **Age**: Age of the patient.
- **Sex**: Sex of the patient (M/F).
- **ChestPainType**: Type of chest pain (e.g., ATA, NAP, ASY).
- **RestingBP**: Resting blood pressure (in mm Hg).
- **Cholesterol**: Serum cholesterol in mg/dl.
- **FastingBS**: Fasting blood sugar (1 if > 120 mg/dl, 0 otherwise).
- **RestingECG**: Resting electrocardiographic results (e.g., Normal, ST, LVH).
- **MaxHR**: Maximum heart rate achieved.
- **ExerciseAngina**: Exercise induced angina (Y/N).
- **Oldpeak**: ST depression induced by exercise relative to rest.
- **ST_Slope**: Slope of the peak exercise ST segment (e.g., Up, Flat, Down).
- **HeartDisease**: Diagnosis of heart disease (1 = yes, 0 = no).

## Key Steps in the Project

### Data Preprocessing
- Loaded the dataset using Pandas and performed initial exploration.
- Checked for missing values and handled them appropriately.
- Converted categorical variables into numerical format using one-hot encoding.

### Exploratory Data Analysis (EDA)
- Conducted a detailed analysis of the dataset using descriptive statistics.
- Visualized the distribution of heart disease using histograms and count plots.
- Analyzed categorical features and their relationships with heart disease.

### Feature Engineering
- Created new features from existing ones, such as extracting unique values in the `Age` feature.
- Encoded categorical variables using techniques like one-hot encoding.
- Scaled numerical features using standard scaling.

### Model Building and Evaluation
- Split the dataset into training and testing sets.
- Trained a Support Vector Machine (SVM) classifier.
- Evaluated model performance using metrics such as accuracy, precision, recall, and F1-score.
- The SVM model demonstrated high accuracy and robustness in predicting heart disease.

### Visualization
- Plotted histograms and box plots to analyze numerical features.
- Visualized outliers and distributions of key features.
- Created count plots to explore categorical data.

## Results
The **SVM model** demonstrated high accuracy in predicting heart disease, achieving an accuracy score of 89.13%. The model effectively utilized the provided features to estimate the likelihood of heart disease.

## Future Enhancements
- Perform hyperparameter tuning to further improve model accuracy.
- Explore additional machine learning models and ensemble techniques.
- Deploy the model as a web application for real-time heart disease prediction.

## Repository
The complete project, including the dataset and code, is available in the [GitHub repository](https://github.com/RayanAlDwlah/SVM-Heart-Prediction).

## Author
- **Email**: rayanaldwlah@gmail.com
- **GitHub**: [RayanAlDwlah](https://github.com/RayanAlDwlah)
- **LinkedIn**: [Rayan Saleh](https://www.linkedin.com/in/rayan-saleh-b12a3132a)

Feel free to explore the repository, review the code, and contribute to the project!
