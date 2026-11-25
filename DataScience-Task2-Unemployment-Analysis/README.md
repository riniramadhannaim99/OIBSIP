# Task 2: Unemployment Analysis with Python

**Oasis Infobyte Internship Program, Data Science track**
Author: Rini Ramadhan Naim

## Objective
Explore unemployment data from India to find regional and monthly trends, and measure the impact of the COVID-19 lockdown on unemployment, employment and labour participation. This is an exploratory analysis (no prediction model): every chart is followed by a written observation.

## Demo video
[Watch the demo video](https://lnkd.in/p/gbA7j_35)

## Dataset
`Unemployment in India.csv` (CMIE data, May 2019 to June 2020): 768 raw rows, 740 after cleaning, 28 states, Rural and Urban areas.

| Column | Meaning |
|---|---|
| Region | Indian state |
| Date | Month (last day of the month) |
| Frequency | How often the data is measured (monthly) |
| Estimated Unemployment Rate (%) | Share of the labour force without a job |
| Estimated Employed | Estimated number of employed people |
| Estimated Labour Participation Rate (%) | Share of people who are working or looking for work |
| Area | Rural or Urban |

## Approach
1. Load and clean the data: remove 28 empty rows, trim extra spaces, convert `Date` to a real date type
2. Exploratory analysis: region-wise, Rural vs Urban and month-wise trends
3. Time series of unemployment for five major states (Maharashtra, Tamil Nadu, Uttar Pradesh, Delhi, West Bengal)
4. Top 10 states by average unemployment
5. Correlation heatmap (all rows vs monthly averages)
6. Pre-COVID (May 2019 to Feb 2020) vs COVID period (April to June 2020)

## Key findings
- Before the lockdown, unemployment was steady at about 9% to 10%. It jumped to about 24% in April and May 2020 and fell back to about 12% in June 2020.
- Labour participation fell from about 44% to about 35% in April 2020, so many people stopped looking for work, not only lost their jobs.
- Pre-COVID vs COVID period: unemployment 9.5% to 20.2%, participation 43.9% to 38.1%, employed people down about 17%.
- Urban areas had higher unemployment than rural areas, but both rose by about 10 to 11 points.
- Highest average unemployment: Tripura, Haryana, Jharkhand, Bihar and Himachal Pradesh. Biggest COVID rise: Puducherry, Jharkhand, Tamil Nadu and Bihar.
- Averages can hide differences: the correlations look weak across all rows but very strong across monthly averages.

## Limitations
- Only 14 months of data, ending in June 2020, so long-term effects cannot be judged.
- Simple averages of rows, not weighted by population or labour force size.
- States have different numbers of rows, and some values come from small samples.
- CMIE noted that survey work was disrupted during the lockdown, so some numbers (especially March 2020) are less certain.
- The analysis shows association over time, not proof that the lockdown alone caused every change.

## Files
- `UnemploymentAnalysis.ipynb`: the full notebook
- `Unemployment in India.csv`: the dataset

## How to run
```bash
pip install numpy pandas matplotlib seaborn jupyter
jupyter notebook UnemploymentAnalysis.ipynb
```
Keep the CSV file in the same folder as the notebook.

## Source
Centre for Monitoring Indian Economy (CMIE), Unemployment in India (Kaggle dataset).
