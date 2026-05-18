# Global Terrorism Exploratory Data Analysis (1970–2017)

## Project Overview

This project performs an in-depth Exploratory Data Analysis (EDA) on the Global Terrorism Database (GTD), which contains information on over 181,000 terrorist incidents worldwide from 1970 to 2017.

The objective of this analysis is to uncover long-term terrorism trends, identify the most affected countries and regions, study attack methods and casualty patterns, and generate data-driven security and policy recommendations.

The project goes beyond simple chart creation by focusing on:
- analytical storytelling,
- quantified insights,
- derived feature engineering,
- temporal trend analysis,
- geographic visualization,
- and business/policy impact.

---

## Dataset Information

- Dataset: Global Terrorism Database (GTD)
- Source: START Consortium / Kaggle
- Time Period: 1970–2017
- Total Incidents: 181,691
- Original Features: 135 columns
- Final Analytical Features Used: 14 core columns + 9 derived features

---

## Project Objectives

- Analyze how terrorism trends changed over time
- Identify the countries and cities with highest casualties
- Study how attack methods evolved across decades
- Explore relationships between attack success and casualties
- Understand regional concentration of terrorism
- Detect high-lethality countries and attack types
- Generate actionable counter-terrorism recommendations

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Folium
- Jupyter Notebook
- Tableau

---

## Data Cleaning & Wrangling

The project includes extensive preprocessing and analytical wrangling:

- Reduced dataset from 135 columns to the most relevant analytical features
- Group-based imputation:
  - Missing cities filled using country-wise mode
  - Missing latitude/longitude filled using country-wise mean
- Preserved original casualty columns before imputation
- Created data-quality flags:
  - `casualty_unknown`
  - `casualty_suspect`
- Handled missing casualty values conservatively using `fillna(0)`
- Created proper datetime columns
- Built missing-value analysis tables
- Performed distribution analysis before imputation

---

## Derived Features

The following analytical features were engineered:

- `total_casualties`
- `kill_ratio`
- `decade`
- `yoy_change`
- `casualty_severity`
- `high_fatality`
- `casualty_unknown`
- `casualty_suspect`
- `casualties_per_attack`

These features enabled deeper multi-dimensional analysis beyond the raw dataset.

---

## Key Insights

### 1. Iraq experienced the highest terrorism impact
- Iraq recorded **213,279 casualties**
- This accounts for approximately **22% of all casualties**
- Iraq alone had casualties comparable to the next 4 countries combined

### 2. Baghdad was the most affected city
- Baghdad recorded **80,363 casualties**
- Nearly **38% of Iraq’s total casualties** occurred in Baghdad

### 3. Terrorism is highly region-concentrated
The top 3 regions:
- Middle East & North Africa
- South Asia
- Sub-Saharan Africa

accounted for approximately:

- **77.5% of all casualties**

### 4. Bombings caused the highest casualties despite low lethality
- Bombing/Explosion attacks caused:
  - **530,007 total casualties**
- But had a relatively low:
  - **0.18 kill ratio**

This revealed an important insight:

> volume beats lethality.

### 5. Assassination attacks were the deadliest attack type
- Assassinations had the highest kill ratio:
  - **0.71**
- Meaning 71% of casualties in assassination attacks resulted in deaths.

### 6. Syria had the highest casualties per attack
- Syria recorded:
  - **13.33 casualties per attack**
- Despite not ranking highest in total casualties.

This revealed that:
- some countries experience fewer,
- but significantly deadlier incidents.

### 7. Terrorism increased dramatically over time
- Incidents increased from:
  - **651 attacks in 1970**
  - to **16,903 attacks in 2014**

Major spikes aligned with:
- Iranian Revolution (1979)
- 9/11 (2001)
- Arab Spring (2011)
- ISIS peak activity (2014)

---

## Visualizations Included

This project contains 17 visualizations including:

- Attacks over time
- YoY trend analysis
- Regional comparisons
- Country casualty analysis
- Attack type evolution by decade
- Pair plots
- Correlation heatmaps
- Severity distributions
- Geographic Folium map
- Casualties-per-attack analysis
- Target and weapon analysis

---

## Geographic Analysis

An interactive Folium map was created using 5,000 sampled incidents to visualize the global geographic spread of terrorism.

The map visually confirmed the concentration of attacks in:
- the Middle East,
- South Asia,
- and parts of Africa.

---

## Business & Policy Recommendations

### 1. Prioritize High-Risk Regions
Since 77.5% of casualties are concentrated in 3 regions, counter-terrorism resources should heavily prioritize:
- Middle East & North Africa
- South Asia
- Sub-Saharan Africa

### 2. Focus on Counter-IED Technologies
Bombings account for the highest casualties globally. Investments in:
- bomb detection,
- explosive tracing,
- surveillance,
- and counter-IED systems
should receive highest priority.

### 3. Prevention Is More Effective Than Reaction
Even failed attacks produced casualties on average.

This suggests:
- early detection,
- financial monitoring,
- intelligence gathering,
- and surveillance
are more effective than post-incident response alone.

### 4. Improve Emergency Medical Response
Countries with high kill ratios may benefit from:
- improved trauma care,
- emergency response systems,
- and faster medical intervention.

---

## Data Limitations

- Missing casualty data may underestimate older incidents
- Some attacks remain unattributed to known groups
- Dataset ends in 2017
- Geographic imputations may slightly distort city-level patterns

These limitations were explicitly acknowledged to maintain analytical transparency.


---

## Conclusion

This project evolved from a basic visualization exercise into a full analytical EDA focused on:
- data storytelling,
- feature engineering,
- business interpretation,
- and interview-ready analysis.

The analysis demonstrates that effective EDA is not about creating charts alone, but about:
- uncovering meaningful patterns,
- questioning assumptions,
- connecting findings,
- and translating data into actionable insight.
