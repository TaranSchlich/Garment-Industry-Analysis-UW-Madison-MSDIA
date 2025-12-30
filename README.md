# Garment Industry Productivity Analysis  
**Author:** Taran Schlichtmann  
**Date:** 09/14/2025  

*Data cleaning, transformation, and visualization of garment manufacturing productivity using Python.* 

[[Open In Colab](https://colab.research.google.com/github/TaranSchlich/garment-productivity-analysis/blob/main/notebooks/garment_analysis.ip

---

## Overview
This project analyzes garment manufacturing productivity data from January and February. It demonstrates:
- **Data Integration**: Combining multiple CSV datasets
- **Data Cleaning**: Removing duplicates, fixing typos, handling null values
- **Feature Engineering**: Creating new metrics like `productivity_difference`
- **Visualization**: Exploring relationships between incentive pay and productivity

---

## Features
- Merge and clean raw datasets
- Rename and standardize columns for clarity
- Replace inconsistent values and handle missing data
- Generate descriptive statistics and visualizations
- Create derived metrics for deeper insights

---

## Project Structure
```
garment-productivity-analysis/
├─ notebooks/
│  └─ garment_analysis.ipynb    # Colab notebook
├─ src/
│  └─ garment_analysis/
│     ├─ data_cleaning.py       # Data cleaning logic
│     ├─ visualization.py       # Visualization logic
├─ data/
│  ├─ garment_jan.csv
│  ├─ garment_feb.csv
├─ requirements.txt             # Python dependencies
├─ README.md                    # Project documentation
```

---

## Quickstart
Clone the repo and install dependencies:
```bash
git clone https://github.com/TaranSchlich/garment-productivity-analysis.git
cd garment-productivity-analysis
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
```

---

## Usage Example
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load combined dataset
df = pd.read_csv('data/combined_garment.csv')

# Scatterplot: Incentive vs Actual Productivity
sns.scatterplot(x='incentive', y='productivity_actual', data=df)
plt.title('Incentive vs Actual Productivity')
plt.xlabel('Incentive Pay')
plt.ylabel('Actual Productivity')
plt.show()
```

---

## Requirements
- **Python Version:** 3.9+
- **Dependencies:**
  - `pandas` – for data manipulation
  - `seaborn` – for visualization
  - `matplotlib` – for plotting
- Works in **local environment** or **Google Colab**

Example `requirements.txt`:
```txt
pandas>=1.3
seaborn>=0.11
matplotlib>=3.4
```

---

## Notes
- Data sourced from garment productivity datasets (January & February)
- Column renaming and cleaning ensure consistency for analysis

---

## Disclaimer
This project is for **educational purposes only** and should **not** be used for operational decision-making without further validation.

---

## License
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
