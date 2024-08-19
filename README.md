# Alzheimer's Disease Staging Prediction

## Project Overview
This project develops a machine learning system to predict Alzheimer's disease stages using brain imaging data, demographic information, and cognitive test results. The system classifies patients into six categories:

1. Cognitive Normal
2. Significant Memory Concern
3. Early Mild Cognitive Impairment
4. Mild Cognitive Impairment
5. Late Mild Cognitive Impairment
6. Alzheimer's Disease

## Methodology

### Data
The dataset includes:
- Brain imaging data
- Demographic information
- Cognitive test results

### Models Implemented
1. Logistic Regression
2. Random Forest
3. Gradient Boosting Machine (GBM)
4. K-Nearest Neighbors (K-NN)

### Model Evaluation
Models were evaluated using precision, recall, and F1-score metrics. Hyperparameter tuning was performed using GridSearchCV.

## Results

### Initial Model Performance

#### Logistic Regression
- Accuracy: 44%
- Macro Avg F1-score: 0.31

#### Random Forest
- Accuracy: 73%
- Macro Avg F1-score: 0.61

#### Gradient Boosting Machine (GBM)
- Accuracy: 71%
- Macro Avg F1-score: 0.61

#### K-Nearest Neighbors (K-NN)
- Accuracy: 28%
- Macro Avg F1-score: 0.21

### Tuned Model Performance

#### Logistic Regression (Tuned)
- Best parameters: C=1, solver='liblinear'
- Accuracy: 51%
- Macro Avg F1-score: 0.42

#### Random Forest (Tuned)
- Best parameters: max_depth=20, n_estimators=200
- Accuracy: 74%
- Macro Avg F1-score: 0.61

#### Gradient Boosting Machine (Tuned)
- Best parameters: learning_rate=0.01, n_estimators=200
- Accuracy: 71%
- Macro Avg F1-score: 0.59

#### K-Nearest Neighbors (Tuned)
- Best parameters: n_neighbors=5
- Accuracy: 28%
- Macro Avg F1-score: 0.21

## Key Findings
1. Random Forest performed best, achieving 74% accuracy after tuning.
2. GBM showed consistent performance with 71% accuracy.
3. Logistic Regression improved significantly with tuning but still underperformed compared to ensemble methods.
4. K-NN performed poorly, suggesting it may not be suitable for this complex classification task.
5. All models struggled with the "Late Mild Cognitive Impairment" category, possibly due to class imbalance or feature overlap with other categories.

## Future Work
1. Address class imbalance, particularly for the underrepresented categories.
2. Explore feature engineering to improve model performance.
3. Investigate deep learning approaches, such as neural networks, which may capture complex patterns in brain imaging data more effectively.
4. Collect more data for underrepresented categories to improve classification accuracy.

## Technologies Used
- Python
- Scikit-learn for machine learning models
- Pandas for data manipulation
- Matplotlib/Seaborn for data visualization

