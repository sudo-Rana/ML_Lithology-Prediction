# ML-Driven Lithology Prediction from Well Logs

This project analyzes well log data for lithology (facies) classification using machine learning models including KNN, Decision Trees, and Random Forest. It includes data preprocessing, visualization, hyperparameter tuning, model training, and evaluation on FORCE 2020 challenge datasets.

## Features
- Loads and preprocesses LAS well log data (GR, SP, RHOB, DTC, NPHI, etc.).
- Handles missing values with interpolation and mean filling.
- Visualizes logs and lithology labels using matplotlib.
- Implements KNN with GridSearchCV (best: n_neighbors=15).
- Trains DecisionTreeClassifier with hyperparameter tuning (max_depth=2, min_samples_leaf=5).
- Uses RandomForestClassifier with RandomizedSearchCV (200 estimators, max_depth=4).
- Achieves ~89.7% accuracy on test set with Random Forest.
- Predicts lithofacies on unseen test data (e.g., WELL 159-14).

## Dataset
- **Train**: ~17k samples from multiple wells (FORCE 2020), 13 features + FACIES labels (0-11).
- **Test**: ~20k samples (testfeatures.csv.txt + testtarget.csv.txt).
- Lithofacies: Sandstone, Shale, Marl, Dolomite, Limestone, etc.

## Installation
1. Clone repo: `git clone<>`
2. Install dependencies: 
   ```bash
   pip install numpy pandas matplotlib scikit-learn lasio missingno petroeval seaborn
3. Place train.csv, testfeatures.csv.txt, testtarget.csv.txt in root.

## Usage
Run the notebook:
jupyter notebook Well-Data_Visualization_and_Lithology_Prediction.ipynb

