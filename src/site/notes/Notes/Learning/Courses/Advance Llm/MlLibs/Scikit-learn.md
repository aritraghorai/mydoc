---
{"dg-publish":true,"permalink":"/notes/learning/courses/advance-llm/ml-libs/scikit-learn/","title":" Scikit-learn"}
---

Here’s a detailed guide for starting with ***Scikit-learn*** as a Machine Learning Engineer:

## 1. **Summary of Scikit-learn**

Scikit-learn is an open-source Python library for machine learning. It provides simple and efficient tools for data analysis and modeling. It is built on top of SciPy and NumPy, which makes it fast and efficient for handling numerical operations.

Key features include:
- **Supervised Learning** (classification, regression)
- **Unsupervised Learning** (clustering, dimensionality reduction)
- **Model Selection** (cross-validation, hyperparameter tuning)
- **Preprocessing** (standardization, scaling, encoding)

Scikit-learn is widely used because it integrates well with other scientific libraries and provides simple APIs for complex tasks.

## 2. **Advantages and Disadvantages**

### **Advantages**
- **Easy to Use:** Offers a consistent API and a wide range of algorithms, making it beginner-friendly.
- **Efficient:** Built on top of NumPy and optimized for performance.
- **Documentation:** Extensive and well-structured documentation.
- **Integration:** Works well with other libraries like Pandas, NumPy, and Matplotlib.
- **Community Support:** Large community with a lot of tutorials and pre-built models.

### **Disadvantages**
- **Not for Deep Learning:** Scikit-learn is not suited for deep learning tasks. For that, you would use TensorFlow or PyTorch.
- **Limited Parallelism:** Not optimized for distributed computing.
- **Scalability:** It is not suitable for very large datasets (big data) unless integrated with libraries like Dask or Spark.

## 3. **Important APIs and Functions to Learn**

### **Supervised Learning APIs**
- **`fit()`**: Trains a model on the provided data.
- **`predict()`**: Makes predictions on new data.
- **`score()`**: Evaluates the model's performance.
- **`cross_val_score()`**: Cross-validation to assess model generalization.
  
### **Unsupervised Learning APIs**
- **`fit()`**: Fits the model on the data without supervision (labels).
- **`transform()`**: Transforms the data based on the model.
- **`fit_transform()`**: Fits the model and then transforms the data.
  
### **Preprocessing APIs**
- **`StandardScaler()`**: Standardizes features by removing the mean and scaling to unit variance.
- **`MinMaxScaler()`**: Transforms features by scaling each feature to a given range.
- **`OneHotEncoder()`**: Converts categorical data into a format suitable for ML models.
- **`PCA()`**: Reduces the dimensionality of the data using Principal Component Analysis.

### **Model Selection APIs**
- **`train_test_split()`**: Splits data into training and testing sets.
- **`GridSearchCV()`**: Performs an exhaustive search over parameter values for model tuning.
- **`RandomizedSearchCV()`**: Similar to `GridSearchCV`, but with random sampling of parameters.

## 4. **Important Topics to Learn**

1. **Data Preprocessing**: Learning how to clean, transform, and encode data before feeding it into machine learning algorithms.
2. **Classification Algorithms**: E.g., Logistic Regression, Decision Trees, Random Forests.
3. **Regression Algorithms**: E.g., Linear Regression, Ridge, Lasso.
4. **Clustering Techniques**: K-Means, DBSCAN.
5. **Dimensionality Reduction**: PCA, t-SNE.
6. **Model Evaluation and Validation**: Cross-validation, confusion matrix, accuracy, precision, recall.
7. **Hyperparameter Tuning**: GridSearchCV, RandomizedSearchCV.
8. **Pipeline Construction**: Building pipelines to streamline the process of applying transformations and training models.
9. **Ensemble Methods**: Bagging, boosting, stacking.

## 5. **Explanation of Functions with Examples**

### **1. `fit()` and `predict()`**

- **Usage**: To train a model and make predictions.

```python
from sklearn.linear_model import LogisticRegression

# Sample data
X_train = [[1, 2], [2, 3], [3, 4], [4, 5]]
y_train = [0, 0, 1, 1]

# Initialize the model
model = LogisticRegression()

# Train the model
model.fit(X_train, y_train)

# Predict using the model
X_test = [[2, 3], [3, 4]]
predictions = model.predict(X_test)

print(predictions)
```

### **2. `train_test_split()`**

- **Usage**: Split data into training and testing sets.

```python
from sklearn.model_selection import train_test_split

# Sample data
X = [[1, 2], [2, 3], [3, 4], [4, 5]]
y = [0, 0, 1, 1]

# Split the data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.25)

print(X_train, X_test)
```

### **3. `StandardScaler()`**

- **Usage**: Standardizes features by removing the mean and scaling to unit variance.

```python
from sklearn.preprocessing import StandardScaler

# Sample data
X = [[1, 2], [2, 3], [3, 4], [4, 5]]

# Initialize the scaler
scaler = StandardScaler()

# Fit and transform the data
X_scaled = scaler.fit_transform(X)

print(X_scaled)
```

### **4. `GridSearchCV()`**

- **Usage**: Perform hyperparameter tuning using exhaustive search.

```python
from sklearn.model_selection import GridSearchCV
from sklearn.svm import SVC

# Sample data
X_train = [[1, 2], [2, 3], [3, 4], [4, 5]]
y_train = [0, 0, 1, 1]

# Define the model and parameters
model = SVC()
parameters = {'kernel': ('linear', 'rbf'), 'C': [1, 10]}

# Perform grid search
grid_search = GridSearchCV(model, parameters)
grid_search.fit(X_train, y_train)

print(grid_search.best_params_)
```

### **5. `PCA()`**

- **Usage**: Perform dimensionality reduction.

```python
from sklearn.decomposition import PCA

# Sample data
X = [[1, 2], [2, 3], [3, 4], [4, 5]]

# Initialize PCA
pca = PCA(n_components=1)

# Fit and transform the data
X_pca = pca.fit_transform(X)

print(X_pca)
```

---

This guide provides an overview to start your journey with Scikit-learn. You can explore further by practicing these functions on real datasets and building projects!


## Train Test Split
