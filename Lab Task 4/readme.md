# Linear Regression Model on Programming Languages Dataset

This project demonstrates how to perform a linear regression on a dataset that tracks the worldwide popularity of different programming languages over time.

## Dataset

The dataset (`data.csv`) contains the worldwide popularity percentages of various programming languages and frameworks. It includes columns such as:

- `Month`: The date (starting from 2004).
- `Python Worldwide(%)`, `JavaScript Worldwide(%)`, `Java Worldwide(%)`, etc.: Popularity percentages of programming languages.

## Project Steps

### 1. Data Loading

The dataset is loaded into a pandas DataFrame:

```python
import pandas as pd
df = pd.read_csv('data.csv')
```

### 2. Data Preprocessing

The feature matrix `X` and target vector `y` are extracted from the dataset:

```python
X = df[['Python Worldwide(%)', 'JavaScript Worldwide(%)']]  # Example features
y = df['Java Worldwide(%)']  # Target variable
```

### 3. Train-Test Split

The data is split into training and testing sets:

```python
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=0)
```

### 4. Model Training

A linear regression model is initialized and trained on the training data:

```python
from sklearn.linear_model import LinearRegression
model = LinearRegression()
model.fit(X_train, y_train)
```

### 5. Model Prediction and Plotting

Predictions are made using the test data, and the results are plotted:

```python
import matplotlib.pyplot as plt

# Make predictions
y_pred = model.predict(X_test)

# Select a single feature for plotting (e.g., the first feature)
X_test_single_feature = X_test.iloc[:, 0]

# Plot the actual data and the regression line
scatter_plot = plt.scatter(X_test_single_feature, y_test, color='b')
line_plot, = plt.plot(X_test_single_feature, y_pred, color='r')

# Add labels, title, and legend
plt.xlabel('First feature from X_test')
plt.ylabel('y-axis')
plt.title('Linear Regression')
plt.legend([scatter_plot, line_plot], ['Actual Data', 'Regression Line'])

# Show the plot
plt.show()
```

## Requirements

- Python 3.x
- Pandas
- Scikit-learn
- Matplotlib

You can install the required libraries using:

```bash
pip install pandas scikit-learn matplotlib
```

## How to Run

1. Clone the repository:
    ```bash
    git clone <repository-url>
    ```
   
2. Ensure you have the dataset `data.csv` in the project directory.

3. Run the Jupyter notebook or Python script containing the linear regression code.

## Output

The project will display a scatter plot showing the actual data points and a line representing the regression model's predictions.

## License

This project is licensed under the MIT License.
```

You can customize the sections based on your specific project details. This structure will give an overview of the steps involved in your linear regression project, including code snippets, requirements, and instructions on how to run it.
