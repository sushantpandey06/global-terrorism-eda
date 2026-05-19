# Global Terrorism EDA

Analysis of 181,691 terrorist incidents from 1970 to 2017.

Dataset: Global Terrorism Database (GTD) from Kaggle. 135 columns originally, reduced to 14.

Dataset link: https://drive.google.com/file/d/1Y6oCRo-uYEE7163J1flnUzL7wXGQZZ3w/view?usp=sharing

## What I did

- Dropped 77 columns that had over 100K missing values, then picked 14 columns that actually matter for analysis
- Missing cities: filled using the most common city per country (groupby mode), not a global fill
- Missing casualties: used fillna(0) but kept the original values in separate columns (nkill_raw, nwound_raw) so I can track what was imputed. Also made a casualty_unknown flag for rows where data was originally missing, and a casualty_suspect flag for pre-1990 incidents where zero might mean "not recorded" rather than "no one died"
- Created 9 features: total_casualties, kill_ratio, decade, yoy_change, casualty_severity, high_fatality, casualty_unknown, casualty_suspect, casualties_per_attack
- Made 17 charts covering countries, cities, regions, attack types, time trends, severity, groups, and a folium map

## Main findings

Iraq has 213,279 casualties — 22% of the global total and more than the next 4 countries combined. Baghdad alone has 80,363.

Bombing causes the most casualties (530,007) but has the lowest kill ratio (0.18). Assassination has the highest kill ratio (0.71) but far fewer total casualties. Volume beats lethality.

77.5% of all casualties happen in 3 regions: Middle East, South Asia, Sub-Saharan Africa.

Syria has 13.33 casualties per attack — the highest of any country — but ranks only 7th in total. So total counts miss per-incident severity.

Attack counts went from 651 in 1970 to 16,903 in 2014. The spikes line up with the Iranian Revolution (1979), 9/11 (2001), Arab Spring (2011), and ISIS (2014).

90% of attacks have zero or low casualties. The devastating ones get media coverage, which creates a perception that most attacks are catastrophic. They're not.

## Tools

Python, pandas, matplotlib, seaborn, folium

## How to run

Open the notebook in Colab or Jupyter. Use `encoding='latin1'` when loading the CSV.

## What I'd improve

- Normalize by country population to get per-capita rates
- Build a Tableau dashboard for the main findings
- Look at post-2017 data if it becomes available
