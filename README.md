# Sort Dataset using Pandas

**Internship:** Veda Technology, AI & ML Track
**Intern:** J Sanjay (AI & Data Science)

## Description
In this project, a dataset is sorted using numerical and categorical columns in ascending and descending order. It is a practical example of how sorting helps organize data and makes analysis easier.

## Objective
Understand how sorting helps organize and analyze datasets.

## Tools Used
- Python
- Pandas
- Jupyter Notebook / Google Colab

## Dataset
Employee Dataset (Name, Department, Age, Salary). File: `employee.csv`

## Approach
1. Imported Pandas and loaded the dataset into a DataFrame.
2. **Ascending sort:** `df.sort_values(by="Salary")`
3. **Descending sort:** `df.sort_values(by="Salary", ascending=False)`
4. **Categorical sort:** `df.sort_values(by="Department")` (A to Z)
5. **Multiple columns sort:** `df.sort_values(by=["Department", "Salary"], ascending=[True, False])`
6. Used `reset_index(drop=True)` to clean the index.

## Sample Code
```python
import pandas as pd

df = pd.read_csv("employee.csv")

asc = df.sort_values(by="Salary")
desc = df.sort_values(by="Salary", ascending=False)
multi = df.sort_values(by=["Department", "Salary"], ascending=[True, False])
```

## Outcome
- Numerical column (Salary) sorted in ascending and descending order.
- Categorical column (Department) sorted alphabetically.
- With multiple columns, records are grouped by the first column, and the second column's order applies within each group (Department A-Z, then Salary high to low).

## Output Screenshots
![Ascending](screenshots/ascending.png)
![Descending](screenshots/descending.png)
![Multi-column](screenshots/multi_column.png)

## Key Learnings
- `sort_values()` is the main function for sorting a DataFrame.
- `ascending=False` gives descending order.
- Multiple columns can be passed as a list, and `ascending` can also be a list.

## How to Run
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
pip install pandas jupyter
jupyter notebook sort_dataset.ipynb
```

## Repository Structure
```
├── sort_dataset.ipynb
├── employee.csv
├── screenshots/
└── README.md
```
