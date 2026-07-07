# Big Mart Sales - Data Analysis & Visualization

DevRise Internship Program - Batch 1 (2026) | Domain: AI & ML | Task 1

## Project Overview
This project performs data cleaning, descriptive statistical analysis, and
visualization on the Big Mart Sales dataset to uncover trends behind item
and outlet sales performance.

## Objective
- Clean a raw public dataset (missing values, duplicates, inconsistent categories, anomalies)
- Compute descriptive statistics using Pandas and NumPy
- Generate visualizations (histogram, bar chart, scatter plot, correlation heatmap) using Matplotlib and Seaborn
- Communicate business insights from the trends observed

## Project Structure
DevRise-Task1/
- Task1_Analysis.ipynb (Main Jupyter Notebook)
- Train.csv (Dataset)
- plots/ (Exported high-resolution plots)
- README.md (This file)

## Setup Instructions
1. Clone the repository
   git clone <your-repo-url>
   cd DevRise-Task1

2. Install dependencies
   pip install pandas numpy matplotlib seaborn jupyter

3. Launch Jupyter Notebook
   jupyter notebook Task1_Analysis.ipynb

4. Run all cells (Kernel > Restart & Run All) to reproduce the analysis.

## Dataset
The Big Mart Sales dataset (Train.csv) contains 8523 rows and 12 columns,
including item attributes (weight, fat content, visibility, type, MRP) and
outlet attributes (size, location type, establishment year, type), with
Item_Outlet_Sales as the target variable.

## Data Cleaning Steps
- Missing Item_Weight: Filled with median
- Missing Outlet_Size: Filled with mode
- Duplicate rows: Checked and removed
- Item_Fat_Content inconsistency: Standardized (LF/low fat -> Low Fat, reg -> Regular)
- Item_Visibility = 0 anomaly: Replaced with mean visibility per Item_Type
- Data types: Converted categorical columns to category dtype

## Key Insights
- Item MRP is the strongest driver of sales (correlation 0.57)
- Outlet Type matters more than Outlet Size - Supermarket Type3 outlets average ~3694 in sales vs. Grocery Stores at ~340
- Sales distribution is right-skewed, with most items selling in the 0-4000 range
- Multiple data quality issues were identified and corrected during cleaning

## Tech Stack
- Python 3
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Author
Ahana Singh - DevRise Internship, Batch 1 (2026)