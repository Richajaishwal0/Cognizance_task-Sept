# Code
```python
# Import necessary libraries
from sklearn.datasets import load_iris
import pandas as pd
iris = load_iris()# Load the Iris dataset
# Create a DataFrame from the dataset
# The data contains the features, and the target holds the species information
iris_df = pd.DataFrame(data=iris.data, columns=iris.feature_names)
# Add the target variable (species) to the DataFrame
iris_df['species'] = iris.target
# Display the first 5 rows of the dataset
print(iris_df.head())
```
# Output
![image](https://github.com/user-attachments/assets/c2d39fbb-f32d-4bc6-8c29-b73c877d3655)
#Overall Code
![image](https://github.com/user-attachments/assets/47f87f6e-4012-4870-a3c3-da1f0bc50849)
