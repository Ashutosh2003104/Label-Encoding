# Label Encoding Example

This Jupyter Notebook demonstrates how to perform label encoding on categorical data using the `OrdinalEncoder` and `LabelEncoder` from the `sklearn.preprocessing` module. The dataset used in this example is a customer dataset containing categorical features such as `review`, `education`, and `purchased`.

## Table of Contents
- Introduction
- Dependencies
- Dataset Overview
- Data Preprocessing
- Label Encoding
- Conclusion

## Introduction
Label encoding is a technique used to convert categorical data into numerical format, which is necessary for many machine learning algorithms that require numerical input. This notebook demonstrates how to use `OrdinalEncoder` for encoding multiple categorical features and `LabelEncoder` for encoding the target variable.

## Dependencies
The following Python libraries are used in this notebook:

- `numpy`
- `pandas`
- `sklearn`

You can install these libraries using pip if you don't have them installed:

```bash
pip install numpy pandas scikit-learn
```

## Dataset Overview
The dataset used in this notebook is stored in a CSV file named `customer.csv`. It contains the following columns:

- `age`: The age of the customer.
- `gender`: The gender of the customer.
- `review`: The review rating given by the customer (`Poor`, `Average`, `Good`).
- `education`: The education level of the customer (`School`, `UG`, `PG`).
- `purchased`: Whether the customer made a purchase (`Yes`, `No`).

The dataset is loaded into a Pandas DataFrame, and a sample of the data is displayed.

## Data Preprocessing

### Loading the Dataset
The dataset is loaded using `pandas.read_csv()`.

### Selecting Relevant Columns
Only the `review`, `education`, and `purchased` columns are selected for further processing.

### Splitting the Data
The dataset is split into training and testing sets using `train_test_split()` from `sklearn.model_selection`.

## Label Encoding

### Ordinal Encoding
The `OrdinalEncoder` is used to encode the categorical features (`review` and `education`) into numerical values. The categories are specified as:

```python
[['Poor', 'Average', 'Good'], ['School', 'UG', 'PG']]
```

### Label Encoding
The `LabelEncoder` is used to encode the target variable (`purchased`) into numerical values:

- `0` for `No`
- `1` for `Yes`

## Conclusion
This notebook provides a step-by-step guide on how to perform label encoding on categorical data using `OrdinalEncoder` and `LabelEncoder`. The encoded data is now ready to be used in machine learning models that require numerical input.

## Usage
To run this notebook, ensure you have the required dependencies installed and the `customer.csv` file in the same directory. You can then execute each cell sequentially to see the results.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

