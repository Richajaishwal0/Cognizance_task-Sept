## Label Encoding of Categorical Target Variable

To encode the categorical target variable `species` into numeric values, we use `LabelEncoder` from `scikit-learn`.

### Code Example

```python
# Import necessary libraries
import pandas as pd
from sklearn.preprocessing import LabelEncoder
from sklearn.datasets import load_iris

# Load the Iris dataset
iris = load_iris()
df = pd.DataFrame(data=iris.data, columns=iris.feature_names)
df['species'] = iris.target

# Map integer target values to species names for better readability
df['species'] = df['species'].map({0: 'setosa', 1: 'versicolor', 2: 'virginica'})

# Initialize the LabelEncoder
label_encoder = LabelEncoder()

# Fit and transform the 'species' column to numeric values
df['species_encoded'] = label_encoder.fit_transform(df['species'])

# Display the first few rows of the DataFrame with encoded species
print("DataFrame with Encoded Species:")
print(df.head())
```
# Output
 ![image](https://github.com/user-attachments/assets/ed30f241-b5bc-45a6-8f96-fc7e442c83c2)
