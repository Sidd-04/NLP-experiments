# Employee Data Analysis Experiments

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on an employee dataset using **Python, Pandas, Matplotlib, and Seaborn**.

The notebook analyzes employee information such as:

- Department
- Salary
- Gender
- Age
- Years of Experience
- Employee Name

It uses statistical operations and visualizations to better understand the dataset.

## 🛠️ Technologies Used

- **Python**
- **Pandas** — Data manipulation and analysis
- **Matplotlib** — Data visualization
- **Seaborn** — Statistical data visualization
- **Jupyter Notebook / Google Colab**

## 📂 Dataset

The project uses the following CSV dataset:

```text
employee_information_100.csv
```

The dataset is loaded using:

```python
df = pd.read_csv(file_path)
```

The data is stored in a Pandas DataFrame called `df`.

## 📊 Experiments Performed

### 1. Average Salary by Department

Calculates the average salary of employees in each department using:

```python
df.groupby('Department')['Salary'].mean()
```

A horizontal bar chart is used to visualize the results.

### 2. Number of Employees per Department

Counts the number of employees in each department using:

```python
df['Department'].value_counts()
```

A Seaborn count plot is used for visualization.

### 3. Gender Distribution

Analyzes the distribution of employees based on gender:

```python
df['Gender'].value_counts()
```

The result is displayed using a pie chart with percentage values.

### 4. Salary Distribution

A histogram is created to understand how employee salaries are distributed:

```python
sns.histplot(df['Salary'], bins=15, kde=True)
```

The KDE curve helps show the overall salary distribution pattern.

### 5. Experience vs Salary

A scatter plot is used to analyze the relationship between:

- Years of Experience
- Salary
- Department
- Gender

```python
sns.scatterplot(
    data=df,
    x='Experience_Years',
    y='Salary',
    hue='Department',
    style='Gender'
)
```

### 6. Top 10 Highest-Paid Employees

Finds the 10 employees with the highest salaries:

```python
df.nlargest(10, 'Salary')
```

The following information is displayed:

- Name
- Department
- Salary
- Years of Experience

### 7. Highest Salary in Each Department

Finds the maximum salary for every department:

```python
df.groupby('Department')['Salary'].max()
```

### 8. Employees Earning Above Average Salary

First, the overall average salary is calculated:

```python
overall_avg = df['Salary'].mean()
```

Then, employees earning more than the average are selected:

```python
high_earners = df[df['Salary'] > overall_avg]
```

### 9. Average Experience by Department

Calculates the average number of years of experience for employees in each department:

```python
df.groupby('Department')['Experience_Years'].mean()
```

### 10. Age Distribution

A histogram is created to analyze the age distribution of employees:

```python
sns.histplot(df['Age'], bins=15, kde=True)
```

This helps identify the distribution of employee ages.

## 📈 Visualizations Used

The project includes:

- Horizontal Bar Chart
- Count Plot
- Pie Chart
- Histogram
- KDE Curve
- Scatter Plot

## ▶️ How to Run the Project

1. Install the required libraries:

```bash
pip install pandas matplotlib seaborn
```

2. Place the dataset in the appropriate location.

3. Update the file path if necessary:

```python
file_path = 'path/to/employee_information_100.csv'
```

4. Open the Jupyter Notebook or Google Colab.

5. Run all cells sequentially.

## 📁 Project Structure

```text
Employee-Data-Analysis/
│
├── Experiment1.ipynb
├── employee_information_100.csv
└── README.md
```

## 🎯 Learning Objectives

This project demonstrates:

- Loading CSV files using Pandas
- Exploring datasets with `head()` and `info()`
- Grouping data using `groupby()`
- Calculating mean and maximum values
- Counting categorical data using `value_counts()`
- Filtering data based on conditions
- Finding top values using `nlargest()`
- Creating different types of data visualizations
- Performing basic Exploratory Data Analysis

## ✅ Conclusion

This project provides a basic analysis of employee data using Python data analysis libraries. It demonstrates how to extract useful insights from a dataset and present those insights through tables and visualizations.
