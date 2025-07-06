# 🦠 COVID-19 India Trend Analysis

This project analyzes the spread and impact of COVID-19 across different Indian states using a synthetic uncleaned dataset. It focuses on uncovering trends in daily cases, recovery and death rates, regional comparisons, and curve flattening over time.

## 📌 Project Goals

- Understand how COVID-19 progressed state-wise in India
- Detect trends in confirmed, recovered, and deceased cases
- Visualize daily spikes and rolling averages
- Analyze and compare recovery and death rates
- Communicate insights through clear plots and summary metrics

---

## 📁 Dataset

- **Source**: Synthetic dataset generated manually (based on real trends)
- **Columns**:  
  - `Date` – daily dates from Mar 2020 to Jun 2021  
  - `State` – name of Indian state  
  - `Confirmed` – cumulative confirmed cases  
  - `Recovered` – cumulative recoveries  
  - `Deceased` – cumulative deaths  

- **Cleaning Challenges**:
  - Invalid dates (`'N/A'`)
  - Missing state names
  - Non-numeric or negative values
  - Sudden spikes in some fields

---

## 📊 Exploratory Data Analysis

### ✅ Data Cleaning Steps
- Converted date strings into datetime format
- Removed invalid rows and filled missing values
- Handled `'unknown'` and negative values

### 📈 Key Features Created
- `Active` = Confirmed - Recovered - Deceased
- `Daily New Cases` using `.diff()`
- `7-day Rolling Averages` for smoother trends
- `Recovery Rate` and `Death Rate` for each state

---

## 📉 Visualizations

- **Daily New Cases vs 7-Day Avg** for individual states
- **Top 10 States by Confirmed Cases**
- **Bar plots** for regional comparisons
- **Scatterplot** of Recovery Rate vs Death Rate

---

## 📌 Insights

- Maharashtra consistently showed high case counts, followed by Kerala and Delhi.
- 7-day rolling averages helped smooth out daily reporting noise.
- Some states showed excellent recovery rates (>90%) with very low death rates (<2%).
- Visual evidence of curve flattening in some states post second wave.

---

## 🧠 What I Learned

- Handling real-world uncleaned time-series data
- Engineering rolling averages and day-wise trends
- Creating reusable visualizations for any state
- Communicating data insights with clear plots

---

## 🛠️ Tech Stack

- Python (Jupyter Notebook)
- pandas, numpy
- matplotlib, seaborn

---

## 📁 Output Files

- `covid_india_cleaned.csv` – Cleaned dataset after preprocessing
- `.ipynb` – Notebook with full code, cleaning, EDA, and plots

---

## 📌 How to Use

```bash
# Clone this repo and open the notebook:
jupyter notebook covid_trend_analysis.ipynb
