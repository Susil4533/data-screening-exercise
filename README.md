# ICE Detention Facilities Data Screening Exercise

## Project Overview

This repository contains the complete data screening and analysis workflow for the ICE Detention Facilities dataset.  
The objective of this exercise is to demonstrate **data cleaning, analysis, visualization, and reproducibility** while handling messy real-world data.

Tasks completed include:

1. Cleaning inconsistent or malformed data (special characters, missing values, mixed types)  
2. Converting numeric Excel serial numbers and string dates into proper datetime format  
3. Summarizing facility-level population using Level A–D columns  
4. Identifying the top 10 facilities by total population  
5. Visualizing the top 10 facilities in a professional horizontal bar chart  

---

## Data Cleaning

1. **Name column**  
   - Removed unnecessary special characters (e.g., `@`, `#`, `$`)  
   - Filled blank facility names by reconciling with the official source webpage  
   - Standardized capitalization and removed leading/trailing spaces  

2. **Last Inspection End Date**  
   - Converted numeric Excel serial numbers to datetime format (`origin='1899-12-30'`)  
   - Converted valid string dates to datetime  
   - Removed the time portion (`00:00:00`) to keep only the date  
   - Preserved missing/invalid values as `NaT`  

3. **Level columns (Level A–D)**  
   - Converted to numeric values, including scientific notation  
   - Verified no negative values  
   - Missing or invalid entries were preserved as `NaN`  

4. **City and State columns**  
   - Stripped leading/trailing spaces   

All cleaning steps were documented and performed programmatically to ensure reproducibility.  

---

## Analysis

- **Total Population** was calculated per facility as the sum of `Level A + B + C + D`  
- **Top 10 facilities** by Total Population were identified for further analysis  

---

## Visualization

- A **horizontal bar chart** displays the top 10 facilities by total population  
- Used **Seaborn** with a professional color palette (`rocket`)  
- Saved as a **PNG image** in the `outputs` folder for reporting/submission  

---

## Limitations

1. **Missing or Irrecoverable Data**  
   - Some values in `Last Inspection End Date` were malformed or missing; these were preserved as `NaT`  
   - Certain facility names and addresses required manual reconciliation from external sources  

2. **Assumptions in Total Population**  
   - The Total Population calculation assumes Level A–D columns represent mutually exclusive population groups  
   - Any misreported or missing data may slightly affect rankings  

3. **Static Snapshot**  
   - Dataset represents a single point in time and may not reflect real-time facility populations  

4. **Visualization Choices**  
   - Horizontal bar chart chosen for clarity; other visualizations could provide alternative insights  

---

## Tools and Libraries

- Python 3.12.1  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Jupyter Notebook  

---

## How to Reproduce

1. Clone the repository:

      git clone https://github.com/Susil4533/data-screening-exercise.git

2. Navigate to notebook folder:
cd data-screening-exercise/notebook
3. Open and run the analysis.ipynb notebook in Jupyter or VS Code

4. All outputs (cleaned data, top 10 subset, and plot) will be saved automatically in the outputs folder

