# Santander-Value-prediction


## Dataset Overview

The dataset consists of train and test sets with the following dimensions:

- **Train Set**: (4459, 4993)
- **Test Set**: (49342, 4992)

### Key Characteristics:

- **Sparse Tabular Dataset**: The dataset is primarily sparse, meaning many values are zero or missing.
- **High Range with No Visible Outliers**: The data range is quite extensive but without any apparent outliers.
- **Skewed Distribution**: Most data points have low values, indicating a skewed distribution.
- **Columns with Constant Values**: Some columns might have constant values across the training set, which should be checked and potentially removed.

## Correlation Analysis: Pearson vs. Spearman

### Pearson Correlation:

- **How it Works**: Measures the strength and direction of a linear relationship between two variables. It looks at how changes in one variable are associated with changes in another variable, assuming they move in a straight line.
- **When to Use**: Best used when you expect the relationship between the two variables to be linear, meaning if you plotted them on a graph, they would form a straight line.

### Spearman Correlation:

- **How it Works**: Measures the strength and direction of a monotonic relationship between two variables. It looks at how one variable changes in relation to the rank order of another variable. Instead of using the actual values, it uses the ranks (positions in order) of the values.
- **When to Use**: Best used when the relationship might not be linear but is still consistent in some way. For example, if one variable increases, the other generally increases as well, but not necessarily in a straight line.

## Correlation Heat Map

To identify the most significant features, we analyze the variables with an absolute correlation value with the target greater than 0.11. This step helps in reducing the number of features and focusing on the most relevant ones.

### Steps:

1. **Select Significant Features**: Choose variables whose absolute value of correlation with the target is greater than 0.11.
2. **Generate Heat Map**: Create a correlation heat map to identify any strong monotonic relationships between these important features.
3. **Feature Selection**: If high correlation values are found between some features, consider keeping only one of those variables for the model building process to avoid redundancy.


## Models Used

- **LightGBM**
- **ExtraTreesRegressor**

These models are used to build predictive models based on the selected features from the correlation analysis.

---

