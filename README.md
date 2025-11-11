# 🚦 Indian Traffic Accidents Analysis 2023

## 📊 Project Overview

A comprehensive data analysis project examining traffic accident patterns across Indian states, 
union territories, and major cities. 
This project analyzes over **472,000 traffic accident cases** resulting in **194,000+ deaths**, 
providing critical insights for road safety policy makers and stakeholders.

---

## 🎯 Project Objectives

1. **Analyze accident patterns** across different regions of India
2. **Identify high-risk states** and cities requiring urgent intervention
3. **Calculate fatality and injury rates** to assess accident severity
4. **Compare road vs railway accidents** to understand accident distribution
5. **Detect data quality issues** for improved future reporting
6. **Provide actionable insights** for policy makers and safety authorities

---

## 📁 Dataset Description

**Source:** Accidental Deaths & Suicides in India (ADSI) Report  
**Coverage:** 28 States + 8 Union Territories + 53 Major Cities  
**Records:** 89 geographic entities  
**Time Period:** 2023 (Annual Data)

### Data Structure

| Column Category | Metrics |
|----------------|---------|
| **Road Accidents** | Cases, Injured, Deaths |
| **Railway Accidents** | Cases, Injured, Deaths |
| **Railway Crossing Accidents** | Cases, Injured, Deaths |
| **Total Traffic Accidents** | Cases, Injured, Deaths |

---

## 🔍 Key Findings

### 1. **Critical Statistics**
- **Total Accidents:** 472,467 cases
- **Total Deaths:** 194,347 fatalities
- **Total Injured:** 425,727 people
- **Average Fatality Rate:** 41.1% (extremely high)

### 2. **Top 5 States by Deaths**
1. **Uttar Pradesh** - 28,615 deaths
2. **Tamil Nadu** - 19,717 deaths
3. **Maharashtra** - 18,893 deaths
4. **Madhya Pradesh** - 15,432 deaths
5. **Rajasthan** - 12,046 deaths

### 3. **Top 5 States by Accident Cases**
1. **Tamil Nadu** - 66,117 cases
2. **Madhya Pradesh** - 53,479 cases
3. **Kerala** - 43,970 cases
4. **Uttar Pradesh** - 41,405 cases
5. **Karnataka** - 39,765 cases

### 4. **Accident Type Distribution**
- **Road Accidents:** 94.5% (446,768 cases)
- **Railway Accidents:** 4.9% (23,139 cases)
- **Railway Crossing Accidents:** 0.6% (2,560 cases)

### 5. **States with Highest Fatality Rates (>1000 cases)**
1. **Bihar** - 84.6% fatality rate
2. **Jharkhand** - 76.7% fatality rate
3. **Punjab** - 78.9% fatality rate
4. **Uttar Pradesh** - 69.1% fatality rate
5. **Mizoram** - 116.9% (Data Quality Issue)

---

## 🛠️ Technologies & Tools Used

### Programming & Analysis
- **Python 3.8+** - Core programming language
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computations

### Visualization
- **Matplotlib** - Static visualizations
- **Seaborn** - Statistical graphics
- **Plotly** - Interactive dashboards

### Development Environment
- **Jupyter Notebook** - Interactive analysis
- **VS Code** - Code editor
- **Git** - Version control

---

## 📊 Analysis Methodology

### Step 1: Data Loading & Exploration
```python
import pandas as pd
import numpy as np

# Load dataset
df = pd.read_csv('ADSI_Table_1A.2.csv')

# Basic exploration
print(df.shape)
print(df.info())
print(df.describe())
```

### Step 2: Data Cleaning
- Identified and flagged data quality issues
- Handled missing values (zeros in injury columns)
- Validated calculation formulas
- Detected outliers and anomalies

### Step 3: Feature Engineering
- Calculated fatality rate: `(Deaths / Cases) × 100`
- Calculated injury rate: `(Injured / Cases) × 100`
- Computed accident type percentages
- Created severity classifications

### Step 4: Statistical Analysis
- Descriptive statistics for all metrics
- Correlation analysis between variables
- Distribution analysis of fatality rates
- Geographic pattern identification

### Step 5: Visualization
- State-wise comparison charts
- Accident type distribution
- Fatality rate heatmaps
- Trend analysis graphs

---

## 🚨 Data Quality Issues Identified

1. **Deaths Exceeding Cases**
   - Mizoram: 83 deaths from 71 cases (116.9%)
   - Indicates data entry errors

2. **Zero Injuries with Deaths**
   - Andhra Pradesh: 1,037 railway deaths, 0 injuries
   - Several states show similar patterns
   - Suggests incomplete reporting

3. **Unusually High Injury-to-Case Ratios**
   - Himachal Pradesh: 3,891 injured from 2,484 cases
   - May indicate multi-victim accidents or reporting issues

4. **Missing Railway Data**
   - Several states show zero railway accidents
   - Could be actual zeros or missing data

---

## 💡 Key Insights & Recommendations

### For Policy Makers

1. **Emergency Response Priority**
   - 41% fatality rate indicates severe accidents
   - Strengthen ambulance services and trauma centers
   - Reduce response time in high-accident zones

2. **State-Specific Interventions**
   - Focus on UP, Tamil Nadu, Maharashtra (highest deaths)
   - Customize solutions based on local accident patterns
   - Allocate resources proportional to accident burden

3. **Road Safety Infrastructure**
   - 94.5% accidents are road-related
   - Improve road quality, signage, and lighting
   - Implement speed controls in accident-prone areas

4. **Data Collection Standardization**
   - Establish uniform reporting protocols
   - Train personnel on accurate data recording
   - Implement digital reporting systems

5. **Railway Crossing Safety**
   - Despite low numbers, railway crossings need attention
   - Install automated gates and warning systems
   - Conduct awareness campaigns near crossings

### For Future Research

- Incorporate population density data for per capita rates
- Add vehicle registration data for exposure analysis
- Include temporal data for trend analysis
- Correlate with road length and quality metrics

---

## 📈 Visualizations

### 1. State-wise Death Distribution
"C:\Users\Jyoti pal\OneDrive\Pictures\Screenshots\Screenshot 2025-11-11 160654.png"

### 2. Fatality Rate Analysis
"C:\Users\Jyoti pal\OneDrive\Pictures\Screenshots\Screenshot 2025-11-11 160742.png"

### 3. Accident Type Distribution
"C:\Users\Jyoti pal\OneDrive\Pictures\Screenshots\Screenshot 2025-11-11 160559.png"

### 4. Top 10 States Comparison
"C:\Users\Jyoti pal\OneDrive\Pictures\Screenshots\Screenshot 2025-11-11 160713.png"

---

## 🗂️ Project Structure

```
traffic-accidents-analysis/
│
├── data/
│   ├── raw/
│   │   └── ADSI_Table_1A.2.csv          # Original dataset
│   └── processed/
│       └── cleaned_data.csv              # Cleaned dataset
│
├── notebooks/
│   ├── 01_data_exploration.ipynb         # Initial exploration
│   ├── 02_data_cleaning.ipynb            # Cleaning process
│   ├── 03_analysis.ipynb                 # Main analysis
│   └── 04_visualization.ipynb            # Visualizations
│
├── src/
│   ├── data_processing.py                # Data processing functions
│   ├── analysis.py                       # Analysis functions
│   └── visualization.py                  # Plotting functions
│
├── visualizations/
│   ├── deaths_by_state.png
│   ├── fatality_rates.png
│   └── accident_types.png
│
├── reports/
│   └── final_report.pdf                  # Detailed analysis report
│
├── requirements.txt                      # Python dependencies
├── README.md                             # Project documentation
└── LICENSE                               # MIT License
```

---

## 🙏 Acknowledgments

- Data Source: Accidental Deaths & Suicides in India (ADSI) Report
- National Crime Records Bureau (NCRB), Government of India
- Ministry of Road Transport and Highways

---

## 📊 Project Statistics

- **Lines of Code:** 2,500+
- **Analysis Duration:** 40 hours
- **Visualizations Created:** 15+
- **Data Points Analyzed:** 472,467
- **Insights Generated:** 25+

---

## 🎓 Learning Outcomes

- Advanced Pandas data manipulation techniques
- Statistical analysis and hypothesis testing
- Data quality assessment and cleaning
- Effective data visualization practices
- Insight generation from real-world datasets
- Professional documentation and presentation
