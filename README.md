# Netflix Catalogue Analysis

Exploratory data analysis of **7,787 Netflix movies and TV shows** using Python, pandas, matplotlib and seaborn. The project cleans a messy real world dataset, answers business questions about Netflix's content strategy, and presents findings with clear visualisations.

![image alt](https://github.com/karanmagar921/NetflixDataAnalysis/blob/main/images/03_titles_added_per_year.png?raw=true)
## Business Questions

1. How much of the catalogue is movies versus TV shows?
2. How fast did Netflix add content, and when did growth peak?
3. Which countries, genres and directors dominate the catalogue?
4. What audience ratings does Netflix target?
5. How long are typical movies, and how many seasons do TV shows run?

## Key Findings

| Area | Finding |
|---|---|
| Content mix | Movies are about **69%** of the catalogue |
| Growth | Additions peaked in **2019** with **2,153** titles |
| Countries | The **US** leads; **India** is second and mostly movies; **Japan** and **South Korea** lean towards TV |
| Audience | **TV-MA** is the most common rating; kids content is only about **10%** |
| Duration | Median movie is **98 minutes**; **67%** of TV shows have one season |
| Timing | **December, October and January** are the busiest months for new titles |

## Visual Highlights

| | |
|---|---|
| ![image alt](https://github.com/karanmagar921/NetflixDataAnalysis/edit/main/README.md#:~:text=02_movies_vs_tv.png) | ![image alt](https://github.com/karanmagar921/NetflixDataAnalysis/edit/main/README.md#:~:text=06_country_content_mix.png) |
| ![image alt](https://github.com/karanmagar921/NetflixDataAnalysis/edit/main/README.md#:~:text=08_ratings.png) | ![image alt](https://github.com/karanmagar921/NetflixDataAnalysis/edit/main/README.md#:~:text=09_duration.png) |

## Data Cleaning Steps

- Removed 2 exact duplicate rows
- Standardised column names to snake_case
- Stripped stray whitespace that broke date parsing
- Converted the date column to datetime and renamed it `date_added` (it records when a title was added to Netflix, not its original release)
- Filled missing `director`, `cast` and `country` with "Unknown" instead of dropping 30% of rows
- Split `duration` into a numeric value and a unit (minutes or seasons)
- Split multi value `country`, `genres` and `director` fields so each entity is counted correctly
- Added assertion checks to confirm cleaning worked

## Project Structure

```
netflix-project/
├── netflix_eda.ipynb      # Main analysis notebook
├── netflix_titles.csv     # Raw dataset
├── netflix_cleaned.csv    # Cleaned output
├── 01 to 10 *.png         # Exported charts
├── requirements.txt
└── README.md
```

## How to Run

```bash
git clone <your-repo-url>
cd NetflixDataAnalysis
pip install -r requirements.txt
jupyter notebook netflix_eda.ipynb
```

## Limitations

- The data ends in early 2021, so 2021 is a partial year.
- There is no viewership data, so popularity cannot be measured.

## Next Steps

- Join IMDb ratings to analyse content quality
- Build a content based recommender using TF-IDF on descriptions and genres
- Create an interactive Streamlit or Power BI dashboard

## Dataset

Netflix titles dataset sourced from Flixable via Kaggle.

## Author

**Karan Thapa**, Bachelor of Computer Science, Charles Darwin University
