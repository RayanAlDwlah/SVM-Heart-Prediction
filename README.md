# SVM-Heart-Prediction

This project uses Support Vector Machine (SVM) to classify and predict heart disease based on various health metrics. The model is trained and evaluated using a dataset containing information about patients' health.

## Project Structure

- `model.ipynb`: The main Jupyter Notebook containing the code for data preprocessing, model training, evaluation, and visualization.

## Requirements

- Python 3.8 or later
- Jupyter Notebook
- Libraries:
  - numpy
  - pandas
  - matplotlib
  - seaborn
  - scikit-learn

## Installation

To run this project locally, follow these steps:

```bash
# Clone the repository
git clone https://github.com/RayanAlDwlah/SVM-Heart-Prediction.git

# Navigate to the project directory
cd SVM-Heart-Prediction

# Install the required libraries
pip install -r requirements.txt
```

## Usage

Open the Jupyter Notebook `model.ipynb` to explore the code and run the cells to train and evaluate the SVM model.

```bash
# Open Jupyter Notebook
jupyter notebook model.ipynb
```

## Data

The dataset used in this project contains various health metrics such as age, sex, chest pain type, resting blood pressure, cholesterol level, fasting blood sugar, resting ECG results, maximum heart rate, exercise-induced angina, ST depression, ST slope, and heart disease presence.

## Model Training and Evaluation

The SVM model is trained using the scikit-learn library. The notebook includes steps for:

- Data Preprocessing
- Splitting the data into training and testing sets
- Scaling the features
- Training the SVM model
- Evaluating the model using metrics such as accuracy, confusion matrix, classification report, and ROC curve.

## Results

The model achieved an accuracy score of 89.13% on the test set with the following evaluation metrics:

- Precision, Recall, and F1-score for each class
- Confusion Matrix
- ROC AUC Score

## Contributing

Contributions are welcome! Follow these steps to contribute:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Create a new Pull Request

## License

This project is licensed under the MIT License.

## Contact

For any questions or issues, please contact:

- Email: rayanaldwlah@gmail.com
- GitHub: [RayanAlDwlah](https://github.com/RayanAlDwlah)
```

Feel free to modify any part of the README to better suit your project. If you need further assistance, let me know!
