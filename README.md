📊 Automated Exploratory Data Analysis (EDA) with YData-Profiling
🧩 About the Project

This project demonstrates fully automated Exploratory Data Analysis (EDA) using YData-Profiling, the official successor to pandas-profiling.

With just a few lines of code, it generates an interactive HTML report containing statistical summaries, variable distributions, correlation matrices, and missing-value visualizations — all crucial for the initial understanding of any dataset before applying machine learning or predictive modeling.

🚀 Project Overview

The Jupyter Notebook Pandas Profiling.ipynb performs the following key operations:

Step	Description
1. Installation	Installs ydata-profiling (formerly pandas-profiling) and required dependencies.
2. Data Loading	Loads a sample dataset — airbus_crash_passengers.csv — for demonstration.
3. Report Generation	Creates a comprehensive HTML EDA report using a single command.
🧠 Purpose of the Notebook

The goal of this notebook is to automate the EDA process, helping data scientists quickly gain insights into:

🧾 Data Structure & Schema – Number of rows, columns, and data types.

🧮 Descriptive Statistics – Mean, median, mode, skewness, kurtosis, etc.

🧱 Correlations – Pearson’s r, Spearman’s ρ, and Cramér’s V for mixed-type data.

⚠️ Missing Values – Matrix, bar chart, and heatmap visualization.

🔍 Variable Distributions – Histograms and frequency plots for every column.

🔄 Duplicate Detection – Identify and flag redundant rows.

🛠️ Installation

You’ll only need pandas and ydata-profiling. Install both directly inside your notebook or terminal:

!pip install pandas ydata-profiling


💡 Note: The notebook also includes installation for pandas_profiling for compatibility during transition to the newer ydata-profiling library.

📁 Dataset

The dataset used here — airbus_crash_passengers.csv — serves as a demonstration dataset for the profiling process.
It contains varied data types and missing values, making it ideal for showcasing EDA capabilities.

File Name	Purpose	Type
airbus_crash_passengers.csv	Demo dataset for profiling	CSV
output.html	Generated interactive EDA report	HTML
🧮 Implementation

Once the dataset is loaded into a DataFrame (df), the entire EDA process is triggered in two lines of Python:

from ydata_profiling import ProfileReport

# 1. Create the profiling report
profile = ProfileReport(df)

# 2. Export the interactive HTML report
profile.to_file(output_file='output.html')


✅ Result:
A complete interactive HTML report (output.html) summarizing:

Overview of data structure and memory usage

Distribution plots for all variables

Pairwise correlations and scatter plots

Missing value matrix and bar visualizations

Warnings and data quality flags

🧾 Output Summary
Report Section	Description
Overview	Dataset summary, memory usage, missing values, and duplicates
Variables	Univariate distributions, descriptive stats, and warning flags
Interactions	Scatter plots and pairwise comparisons between variables
Correlations	Pearson, Spearman, Kendall, and Cramér’s V correlations
Missing Values	Visual patterns via matrix, bar, and heatmap views
💡 Why Use YData-Profiling?

Traditional EDA requires writing dozens of manual plotting and statistical commands.
With YData-Profiling, you can:

Generate full EDA reports instantly

Reduce manual effort by 90%

Get interactive insights for data quality and model readiness

Export results in HTML or JSON for easy sharing

🧰 Output Example

Once executed, you’ll find the following files generated in your working directory:

📁 project/
 ├── airbus_crash_passengers.csv
 ├── Pandas Profiling.ipynb
 └── output.html   ← Interactive EDA Report

📈 Quick Preview of the Workflow
Step	Command	Output
1️⃣	!pip install ydata-profiling	Installs the library
2️⃣	df = pd.read_csv('airbus_crash_passengers.csv')	Loads dataset
3️⃣	ProfileReport(df)	Generates profile object
4️⃣	profile.to_file('output.html')	Creates HTML report
