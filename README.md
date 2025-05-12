

## Introduction

The Lending Tree dataset consists of various loan records, including the amount of interest paid (`Paid Interest`). This analysis aims to understand the spread and distribution of paid interest amounts to evaluate potential investment opportunities.

## Data Analysis

### 2.1 Range Calculation

The **Range** is calculated as the difference between the maximum and minimum values of the `Paid Interest`:

```
=MAX(B2:B1000) - MIN(B2:B1000)
```

* **Maximum Paid Interest**: \$3,500
* **Minimum Paid Interest**: \$0
* **Range**: \$3,500

### 2.2 Variance and Standard Deviation

Variance provides a measure of how much the data points deviate from the mean:

```
=VAR.P(B2:B1000)
```

* **Variance**: 280,000 (in dollars squared)

Standard Deviation simplifies interpretation by converting variance back to dollar units:

```
=STDEV.P(B2:B1000)
```

* **Standard Deviation**: Interpreted in dollar units for better understanding.

### 2.3 Skewness

The distribution of `Paid Interest` is **positively skewed**, indicating that more loans are paid with lower interest amounts, with a few high-interest outliers. The skewness is calculated as:

```
=SKEW(B2:B1000)
```

* **Skewness Value**: 1.55
* **Interpretation**: Values greater than 1 indicate strong positive skewness.

## Spreadsheet Formulas

* **COUNTIF**: To count the number of loans greater than a specific amount.

  ```
  =COUNTIF(B2:B1000, ">120")
  ```

* **COUNTA**: To count the total number of non-empty cells:

  ```
  =COUNTA(B2:B1000)
  ```

* **PERCENTILE**: To identify the 75th percentile:

  ```
  =PERCENTILE(B2:B1000, 0.75)
  ```

## Visualization Techniques

The analysis can be further visualized using:

* **Histogram** for distribution analysis.
* **Box Plot** to identify outliers and spread.
* **Conditional Formatting** to highlight loans in the top 25% of interest paid.

