  ## Feature Scaling

### Standardizing Features with `StandardScaler`

```python
# Import necessary libraries
import pandas as pd
from sklearn.preprocessing import StandardScaler
from sklearn.datasets import load_iris

# Load the Iris dataset
iris = load_iris()
df = pd.DataFrame(data=iris.data, columns=iris.feature_names)
df['species'] = iris.target

# Map integer target values to species names
df['species'] = df['species'].map({0: 'setosa', 1: 'versicolor', 2: 'virginica'})

# Define features (excluding the target variable 'species')
features = df.iloc[:, :-1]

# Initialize the StandardScaler
scaler = StandardScaler()

# Fit and transform the features
scaled_features = scaler.fit_transform(features)

# Create a new DataFrame with standardized features
df_standardized = pd.DataFrame(scaled_features, columns=features.columns)
df_standardized['species'] = df['species']

# Print the first few rows of the standardized DataFrame
print("Standardized DataFrame:")
print(df_standardized.head())
```

![image](https://github.com/user-attachments/assets/0fb69481-2158-4f87-ac85-654eed6ba689)
