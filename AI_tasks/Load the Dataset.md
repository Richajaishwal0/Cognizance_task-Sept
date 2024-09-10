# Code
```python
from sklearn.datasets import load_iris
import pandas as pd
iris = load_iris()
iris_df = pd.DataFrame(data=iris.data, columns=iris.feature_names)
iris_df['species'] = iris.target
print(iris_df.head())
```
# Output
![image](https://github.com/user-attachments/assets/c2d39fbb-f32d-4bc6-8c29-b73c877d3655)
