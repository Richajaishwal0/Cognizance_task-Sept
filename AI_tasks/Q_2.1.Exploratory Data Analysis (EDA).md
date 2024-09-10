# Code 
```python
# Import necessary libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.datasets import load_iris

# Load the Iris dataset
iris = load_iris()
df = pd.DataFrame(data=iris.data, columns=iris.feature_names)
df['species'] = iris.target

# Map integer target values to species names
df['species'] = df['species'].map({0: 'setosa', 1: 'versicolor', 2: 'virginica'})

# Display the first few rows of the dataset
print(df.head())
# Print summary statistics of the numeric features
print("Summary Statistics:")
print(df.describe())

# Calculate the mode for each numeric column
print("\nMode of each numeric feature:")
print(df.select_dtypes(include=[np.number]).mode().iloc[0])

# Check standard deviation of numeric features
print("\nStandard Deviation of each numeric feature:")
print(df.select_dtypes(include=[np.number]).std())
# Check for missing values
print("\nMissing Values in the Dataset:")
print(df.isnull().sum())

# Since the Iris dataset has no missing values, handling is not required
# If there were missing values, you could handle them like this:
# df.fillna(df.mean(), inplace=True)  # Example: Fill missing numeric values with the mean
# Plot histograms for each numeric feature
df.iloc[:, :-1].hist(figsize=(10, 8), bins=20, color='skyblue', edgecolor='black')
plt.suptitle("Feature Distributions", fontsize=16)
plt.show()
# Pair plot to visualize the relationships between features, colored by species
sns.pairplot(df, hue='species', palette='Set2')
plt.suptitle("Pairwise Relationships Between Features", y=1.02, fontsize=16)
plt.show()
``` 
# Output
![image](https://github.com/user-attachments/assets/5f15e539-e3ca-434a-9758-fed1d1d7de2f)
![image](https://github.com/user-attachments/assets/6e459a9e-881b-44c2-9adb-7ed4e2291eed)
![image](https://github.com/user-attachments/assets/d82cf58a-fe35-4ebb-877f-07adecb2ea89)
![image](https://github.com/user-attachments/assets/ef54ea34-8f8a-47f8-81e1-791a83e75183)
![image](https://github.com/user-attachments/assets/2d4557b3-c908-4bbc-8071-f62b1b7417a5)
![image](https://github.com/user-attachments/assets/ca4e5f2e-aa66-438c-823f-966d81e3a190)
