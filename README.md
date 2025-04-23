# CrimesLosAngeles

![Los Angeles Crime Map](https://cdn.pixabay.com/photo/2016/08/05/08/36/los-angeles-1571740_1280.jpg)

## Overview

This repository contains a Jupyter Notebook that analyzes crime data from the Los Angeles Police Department (LAPD). By exploring temporal, geographic, and demographic patterns, the analysis provides insights that can help law enforcement allocate resources more effectively.

## Contents

- **`Los_Angeles_Crime_Analysis.ipynb`**  
  The primary notebook that walks through:
  1. Data loading & initial exploration  
  2. Data cleaning & preprocessing  
  3. Exploratory data analysis (visualizations of crime frequency by hour, crime types, night crimes by area, victim demographics)  
  4. Answers to specific analytical questions (peak crime hour, area with most night crimes, crime counts by victim age group)  
  5. Conclusion and key findings  

- **`crimes.csv`**  
  Raw LAPD crime dataset (CSV format).  

## Key Findings

1. **Peak Crime Hour**: The highest number of reported crimes occurs in the late afternoon/early evening hours.  
2. **Night Crime Hotspots**: Specific neighborhoods show significantly higher night-time crime rates (10 PM–3:59 AM).  
3. **Victim Age Vulnerability**: Certain age groups (e.g., 18–25 and 26–34) experience higher crime victimization rates.


## Usage

1. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
2. Open **`Los_Angeles_Crime_Analysis.ipynb`**.
3. Step through each cell to reproduce the analysis and visualizations.

## Data Preprocessing Steps

- **Duplicate Removal**: Ensures unique records.  
- **Datetime Parsing**: Converts report and occurrence dates to `datetime` objects.  
- **Time Extraction**: Derives `Hour`, `Minute`, and categorizes into `Morning`, `Afternoon`, `Evening`, `Night`.  
- **Missing Values**:  
  - Weapons: fill with “No Weapon”  
  - Victim sex/descent: fill with “Unknown”  
- **Outlier Handling**: Victim ages clipped between 0 and 100, then binned into age groups.

## Exploratory Visualizations

- **Hourly Crime Frequency**: Bar plot of crime counts for each hour (0–23).  
- **Top Crime Types**: Horizontal bar chart of the 15 most common offenses.  
- **Night Crimes by Area**: Top 10 neighborhoods for crimes occurring between 10 PM and 3:59 AM.  
- **Victim Demographics**:  
  - Age group distribution  
  - Sex breakdown (Male, Female, Unknown)  
  - Top descent (ethnicity) categories  

## Questions Answered

1. **Which hour has the highest frequency of crimes?**  
2. **Which area has the greatest number of night crimes (10 PM–3:59 AM)?**  
3. **How many crimes were committed against victims in each age group?**

Variables in the notebook:
- `peak_crime_hour` (integer)  
- `peak_night_crime_location` (string)  
- `victim_ages` (Pandas Series indexed by age group)  

## Contributing

1. Fork the repository.  
2. Create a feature branch: `git checkout -b feature/YourFeature`.  
3. Commit changes: `git commit -am 'Add new analysis'`.  
4. Push to branch: `git push origin feature/YourFeature`.  
5. Open a Pull Request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
