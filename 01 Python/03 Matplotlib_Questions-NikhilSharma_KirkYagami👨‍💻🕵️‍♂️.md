## Matplotlib
### Question 1: Line Plot Visualization (Monthly Sales)
**Problem Statement:**
Using the publicly available "Monthly Beer Production in Australia" dataset from the `pandas` library, create a line plot showing the trend of beer production over the months. Label the x-axis as "Months" and the y-axis as "Beer Production (ML)" and add a title "Monthly Beer Production Trend".

**Function Signature:**
```python
def plot_beer_production() -> None:
```

**Dataset:**
You can use the dataset from `pandas`:
```python
import pandas as pd
df = pd.read_csv('https://people.sc.fsu.edu/~jburkardt/data/csv/hw_200.csv')
```

---

### Question 2: Bar Chart for Category Comparison (Iris Dataset)
**Problem Statement:**
Using the Iris dataset from the UCI Machine Learning Repository, create a bar chart to compare the average sepal lengths of the three different species of iris flowers. Ensure that the bars are color-coded and the chart includes appropriate labels and a title.

**Function Signature:**
```python
def plot_iris_sepal_length() -> None:
```

**Dataset:**
You can load it directly from `seaborn`:
```python
import seaborn as sns
df = sns.load_dataset('iris')
```

---

### Question 3: Scatter Plot with Regression Line (Diamonds Dataset)
**Problem Statement:**
Using the Diamonds dataset from the `ggplot2` package, create a scatter plot of carat vs. price. Fit a linear regression line to the data points and display it on the scatter plot. Include labels for the axes and a title.

**Function Signature:**
```python
def plot_diamond_price_vs_carat() -> None:
```

**Dataset:**
You can load it from `seaborn`:
```python
df = sns.load_dataset('diamonds')
```

---

### Question 4: Histogram of Data Distribution (Titanic Dataset)
**Problem Statement:**
Using the Titanic dataset from the `seaborn` library, create a histogram to visualize the age distribution of passengers. Customize the histogram to have 10 bins and add labels and a title.

**Function Signature:**
```python
def plot_titanic_age_distribution() -> None:
```

**Dataset:**
Load it from `seaborn`:
```python
df = sns.load_dataset('titanic')
```

---

### Question 5: Heatmap Visualization (Correlation Matrix of Titanic Dataset)
**Problem Statement:**
Using the Titanic dataset, generate a heatmap to visualize the correlation matrix of numeric features. Make sure to include a color bar and appropriate labels for the axes.

**Function Signature:**
```python
def plot_titanic_correlation_heatmap() -> None:
```

**Dataset:**
Use the same Titanic dataset as above:
```python
df = sns.load_dataset('titanic')
```

---
### Question 6: Subplots for Multiple Visualizations (Iris Dataset)
**Problem Statement:**
Using the Iris dataset, create a figure with subplots to visualize the following:
1. A scatter plot of sepal length vs. sepal width.
2. A scatter plot of petal length vs. petal width.
Ensure that both plots are in a single figure, appropriately titled, and labeled.

**Function Signature:**
```python
def plot_iris_subplots() -> None:
```

**Dataset:**
Load from `seaborn`:
```python
df = sns.load_dataset('iris')
```

---

### Question 7: Box Plot for Feature Distribution (Titanic Dataset)
**Problem Statement:**
Using the Titanic dataset, create a box plot to visualize the distribution of ages across different passenger classes (Pclass). Include labels for the axes and a title.

**Function Signature:**
```python
def plot_titanic_age_boxplot() -> None:
```

**Dataset:**
Load from `seaborn`:
```python
df = sns.load_dataset('titanic')
```

---

### Question 8: Pie Chart for Categorical Data (Tips Dataset)
**Problem Statement:**
Using the Tips dataset from `seaborn`, create a pie chart showing the distribution of total bill amounts across different days of the week. Include a title and ensure the pie chart is visually appealing.

**Function Signature:**
```python
def plot_tips_pie_chart() -> None:
```

**Dataset:**
Load from `seaborn`:
```python
df = sns.load_dataset('tips')
```

---

### Question 9: Area Plot for Cumulative Data (Global Temperature Dataset)
**Problem Statement:**
Using a publicly available dataset of global temperatures over time, create an area plot to visualize the cumulative increase in temperature over the years. Ensure that the plot is well-labeled and includes a title.

**Function Signature:**
```python
def plot_global_temperature_area() -> None:
```

**Dataset:**
You can find relevant datasets at [Kaggle](https://www.kaggle.com/datasets) or from NOAA (National Oceanic and Atmospheric Administration).

---

### Question 10: Facet Grid for Comparison (Penguins Dataset)
**Problem Statement:**
Using the Penguins dataset from `seaborn`, create a facet grid of scatter plots comparing flipper length vs. body mass across different species. Each subplot should represent a different species, and the plots should include appropriate titles and labels.

**Function Signature:**
```python
def plot_penguins_facet_grid() -> None:
```

**Dataset:**
Load from `seaborn`:
```python
df = sns.load_dataset('penguins')
```
