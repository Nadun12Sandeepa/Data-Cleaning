# Data Cleaning and Visualization Pipeline

A **Python pipeline** to load, clean, summarize, and visualize **any dataset** (CSV, Excel, JSON, TXT, Parquet) with **automatic handling of missing values, duplicates, and numeric conversion**. Includes **static and interactive visualizations** using **Matplotlib, Seaborn, and Plotly**.

---

## Table of Contents

* [Features](#features)
* [Requirements](#requirements)
* [Installation](#installation)
* [Usage](#usage)
* [Function Documentation](#function-documentation)
* [Example](#example)
* [Tips & Notes](#tips--notes)

---

## Features

| Feature            | Description                                                          |
| ------------------ | -------------------------------------------------------------------- |
| Multi-file support | CSV, Excel (`.xls`, `.xlsx`), JSON, TXT, Parquet                     |
| Data Cleaning      | Drop duplicates, handle missing values, convert numeric-like columns |
| Data Summarization | Column info, missing value count, statistics, duplicates             |
| Visualization      | Histograms, boxplots, correlation heatmap, countplots, pairplots     |
| Interactive Plots  | Plotly histograms and bar charts for numeric & categorical columns   |

---

## Requirements

* Python ≥ 3.8
* Libraries:

```bash
pip install pandas numpy matplotlib seaborn plotly openpyxl
```

---

## Installation

1. Clone or download this repository.
2. Save your Python script as `data_pipeline.py`.
3. Prepare your dataset (CSV, Excel, JSON, TXT, Parquet).

---

## Usage

Run the script in the terminal:

```bash
python data_pipeline.py
```

Enter the path to your dataset when prompted:

```text
Enter the path of your dataset: data/dirty_cafe_sales.csv
```

The pipeline will:

1. Load the dataset.
2. Summarize it (info, missing values, statistics, duplicates).
3. Clean it automatically.
4. Display **static** and **interactive** visualizations.

---

## Function Documentation

| Function               | Input              | Output            | Description                                                                                                |
| ---------------------- | ------------------ | ----------------- | ---------------------------------------------------------------------------------------------------------- |
| `load_data(file_path)` | String (file path) | `DataFrame`       | Loads dataset based on file type (`.csv`, `.xls`, `.xlsx`, `.json`, `.txt`, `.parquet`).                   |
| `clean_data(df)`       | `DataFrame`        | `DataFrame`       | Cleans data by removing duplicates, filling missing values (median/mode), converting numeric-like objects. |
| `summarize_data(df)`   | `DataFrame`        | Prints            | Shows dataset info, missing values, statistics, duplicates.                                                |
| `plot_graphs(df)`      | `DataFrame`        | Plots             | Generates static plots (Seaborn) and interactive plots (Plotly) for numeric and categorical columns.       |
| `main()`               | None               | Executes pipeline | Orchestrates dataset loading, cleaning, summarization, and visualization.                                  |

---

## Example Graphs

**1. Histogram (Numeric Column)**
*Visualizes the distribution of numeric data.*

**2. Boxplot (Numeric Column)**
*Shows distribution and outliers for numeric data.*

**3. Correlation Heatmap**
*Shows correlation between numeric columns.*

**4. Countplot (Categorical Column)**
*Visualizes counts of categories.*

**5. Pairplot (Numeric Columns)**
*Shows pairwise relationships between numeric columns.*

**6. Interactive Plotly Histogram**
*Allows zooming, panning, and hovering in the browser.*

---

## Tips & Notes

* **Large Datasets**: Use `chunksize` in `pd.read_csv()` if your CSV is very large.
* **Custom Cleaning**: Extend `clean_data()` for outlier removal, string standardization, or date parsing.
* **Adding File Types**: Update `load_data()` to support more formats.
* **Interactive Plots**: Plotly allows interactive exploration in the browser.

---

This README is ready to include in your GitHub repository or project folder.
