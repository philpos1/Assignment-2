# Assignment 2

Python notebooks for Assignment 2 (pandas, numpy, matplotlib). Outputs and charts are saved in the notebooks.

```
Assignment-2/
├── README.md
├── Q1_Used_Cars/
│   ├── data/train.csv
│   └── notebooks/Q1_Used_Cars_Data_Prep.ipynb
└── Q2_Diabetes/
    ├── data/diabetes.csv
    └── notebooks/Q2_Diabetes_Sampling_Bootstrap.ipynb
```

Q1 (used cars): missing values, removing units, one-hot encoding, a new Car_Age feature, and select/filter/rename/mutate/arrange/group by.

Q2 (diabetes): a sample of 25 for Glucose, the 98th percentile of BMI, and a bootstrap (500 samples of 150) for BloodPressure, with charts and findings.

To run, open a notebook from its `notebooks/` folder and run all cells. The data paths are relative (`../data/...`).
