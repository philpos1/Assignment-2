# Assignment 2: Data Preparation, Sampling and Bootstrap

All source code is in Jupyter notebooks (Python: pandas, NumPy, matplotlib). The notebooks are saved with their outputs and charts, so they display directly on GitHub.

```
Assignment-2/
├── README.md
├── Q1_Used_Cars/
│   ├── data/
│   │   ├── train.csv                 # used-car listings provided for the assignment
│   │   └── used_cars_clean.csv       # output of the Q1 notebook
│   └── notebooks/
│       └── Q1_Used_Cars_Data_Prep.ipynb
└── Q2_Diabetes/
    ├── data/
    │   └── diabetes.csv              # 768 patients, treated as the population
    └── notebooks/
        └── Q2_Diabetes_Sampling_Bootstrap.ipynb
```

## Q1: Used cars (`Q1_Used_Cars_Data_Prep.ipynb`)
- **(a) Missing values:** found hidden missing values (`0.0 kmpl`, and 3 Mileage values in `km/kg`, a CNG unit that can't be converted to kmpl). Engine, Power, Mileage, and Seats were imputed with the mode of the same car model. The remaining Seats gaps got the overall mode (5). The 63 rows (1.1%) with no same-model reference were dropped, including the 2 Electric cars. `New_Price` (86% missing) was dropped.
- **(b) Units removed:** `kmpl`, `CC`, `bhp`, and `Lakh`/`Cr` (crore converted to lakh).
- **(c) One-hot encoding** of `Fuel_Type` and `Transmission`.
- **(d) New features:** `Car_Age` (current year − Year) and `Brand`.
- **(e)** select, filter, rename, mutate, arrange, and group-by summarize, done step by step.

## Q2: Diabetes (`Q2_Diabetes_Sampling_Bootstrap.ipynb`)
- **(a)** Seeded sample of 25: mean and max Glucose vs population.
- **(b)** 98th percentile BMI: sample vs population.
- **(c)** 500 bootstrap samples of 150 (`replace=True`): average mean, SD, and 98th percentile of BloodPressure vs population, with charts and findings.

## How to run
```bash
pip install pandas numpy matplotlib jupyter
jupyter notebook
```
Open a notebook from its `notebooks/` folder and choose **Run All**. Data paths are relative (`../data/...`).
