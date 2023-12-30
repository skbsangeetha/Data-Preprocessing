# Data-Preprocessing
## Imputation with SimpleImputer:
The SimpleImputer class from sklearn.impute module provides a way to handle missing data within a dataset. It allows for strategies like mean, median, most_frequent, or constant to fill in missing values. The usage involves:

### Importing: from sklearn.impute import SimpleImputer
### Initialization: imputer = SimpleImputer(missing_values=np.nan, strategy='mean') initializes the imputer with parameters to define missing values and the strategy to handle them.
### Fitting and Transforming: imputer.fit() computes the strategy on the dataset, and imputer.transform() applies the imputation to fill the missing values in specific columns.
## Encoding Categorical Variables:
### OneHotEncoder: This class from sklearn.preprocessing is used to convert categorical variables into a one-hot encoded format, creating binary columns for each category present in the categorical feature.
It is typically used within ColumnTransformer to specify which columns need one-hot encoding.
### LabelEncoder: This class from sklearn.preprocessing encodes categorical integer features into numeric labels.
It is used to transform the dependent variable into numerical labels.
### ColumnTransformer: This class from sklearn.compose is used to selectively apply different transformations to different columns in a dataset.
It is used in conjunction with OneHotEncoder to specify the columns requiring one-hot encoding.
## Data Splitting using train_test_split:
train_test_split from sklearn.model_selection allows splitting a dataset into training and test sets. It shuffles the data and splits it into two portions based on the specified test size or train size. Key points:

### Usage: from sklearn.model_selection import train_test_split
Parameters: It takes the dataset and test size as inputs, along with other optional parameters like random_state for reproducibility.
Output: It returns four sets of data: X_train, X_test, y_train, y_test (features and labels for both training and test sets).
Feature Scaling with StandardScaler:
StandardScaler from sklearn.preprocessing is used to standardize numerical features by removing the mean and scaling to unit variance.

### Usage: from sklearn.preprocessing import StandardScaler
Fit and Transform: sc.fit_transform() is applied to the training set to compute mean and standard deviation for scaling, and sc.transform() is used to apply the same transformation to the test set.
Normalization: It ensures that each feature has a mean of 0 and a standard deviation of 1, making different features comparable and preventing certain features from dominating due to their scale.
