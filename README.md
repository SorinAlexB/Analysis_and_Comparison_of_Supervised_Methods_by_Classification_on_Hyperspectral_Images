# Analysis and Comparison of Supervised Methods by Classification on Hyperspectral Images

This project explores the use of Support Vector Machines (SVM) and Random Forest (RF) for classifying hyperspectral images. Hyperspectral imaging provides detailed information about the composition and characteristics of objects and surfaces, useful in various fields such as agriculture, mineral exploration, environmental monitoring, and military surveillance.

Used Methods

1. Support Vector Machines (SVM)

SVMs are powerful supervised learning methods for classification, regression, and outlier detection.

Advantages:
- Effective in high-dimensional spaces.
- Suitable when the number of dimensions exceeds the number of samples.
- Uses a subset of training points (support vectors), making it memory efficient.

Disadvantages:
- Choosing appropriate kernel functions and regularization terms is crucial to avoid overfitting.
- Does not directly provide probability estimates, requiring expensive cross-validation for estimation.

2. Random Forest (RF)

Random Forest is an ensemble learning method that constructs multiple decision trees and combines them to improve accuracy and control overfitting.

Advantages:
- High accuracy.
- Robust to noise, missing data, and outliers.
- Handles non-linear relationships effectively.

Disadvantages:
- Computational complexity and memory usage increase with the number of trees.
- Prediction time can be longer compared to simpler models.
- Susceptible to overfitting if not properly tuned.

Installation

Install necessary modules using pip:
```
pip install numpy pandas matplotlib kagglehub seaborn
```
Dataset

Download the dataset using KaggleHub:
```
import kagglehub

# Download dataset
path = kagglehub.dataset_download("billbasener/hyperspectral-library-of-agricultural-crops-usgs")
print("Path to dataset files:", path)
```
Usage

1. Load Dataset:
- Load and preprocess the hyperspectral data, including creating additional columns and normalizing the data.

2. Train/Test Split:
- Split the dataset into training and testing sets.

3. Support Vector Machines (SVM):
- Train SVM model and evaluate its accuracy.
- Display results including precision, recall, and F-score.

4. Random Forest (RF):
- Train RF model and evaluate its accuracy.
- Compare results with SVM and analyze precision, recall, and F-score.

5. Conclusion:
- Compare the performance of SVM and RF.
- Discuss which method performs better for your dataset and why.

Conclusion

Based on the evaluation, SVM performs better for this dataset due to its ability to handle linear boundaries between classes effectively. RF, while powerful, struggled to achieve comparable accuracy possibly due to the nature of the dataset's feature relationships.
