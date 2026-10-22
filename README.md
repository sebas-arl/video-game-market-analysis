# Video Game Market Analysis

[Español](README_ES.md)

## Project Overview

This project analyzes historical video game sales data to identify patterns associated with commercial success and support product and advertising decisions for an international video game retailer.

The analysis was developed as an end-to-end data analysis project using Python, covering data preparation, exploratory analysis, regional market differences, correlation analysis, and statistical hypothesis testing.

The business scenario assumes that historical data through 2016 is available and that the company is preparing its commercial strategy for 2017.

## Business Objective

The main objective is to identify which characteristics are associated with stronger video game sales and determine how these patterns vary across markets.

The analysis addresses questions such as:

- Which platforms have performed best in recent years?
- Which genres generate the highest sales?
- How do consumer preferences differ across North America, Europe, and Japan?
- Are critic and user scores associated with higher sales?
- Do Xbox One and PC users have different average ratings?
- Are user ratings for Action and Sports games statistically different?

## Dataset

The dataset contains **16,715 video game records** and includes:

- Game title
- Platform
- Year of release
- Genre
- Sales in North America
- Sales in Europe
- Sales in Japan
- Sales in other regions
- Critic scores
- User scores
- ESRB ratings

Sales are expressed in millions of units.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- SciPy
- Jupyter Notebook

## Analysis Process

### 1. Data Exploration

The dataset was reviewed using methods such as `head()`, `sample()`, `info()`, `isna()` and `duplicated()` to understand its structure and identify data quality issues.

### 2. Data Cleaning

The preparation process included:

- Standardizing column names.
- Converting user scores to numerical values.
- Treating `tbd` values as missing data.
- Reviewing missing values in release year, scores, and ESRB ratings.
- Removing records without essential information such as game name or genre.
- Creating a `total_sales` variable by combining regional sales.

### 3. Historical and Recent Market Analysis

Historical data was used to understand platform life cycles.

For business decisions related to 2017, the analysis focused on the **2012–2016 period**, which contains **2,886 games** and better represents the recent market environment.

## Key Findings

### Platform Performance

During 2012–2016, the platforms with the highest total sales were:

1. PS4 — 314.14 million
2. PS3 — 288.79 million
3. Xbox 360 — 236.54 million
4. Nintendo 3DS — 194.61 million
5. Xbox One — 159.32 million

Platform sales show clear life cycles, which means recent performance is more useful for short-term commercial planning than historical totals alone.

### Genre Performance

Action generated the highest total recent sales, followed by Shooter, Role-Playing, and Sports.

Genre preferences also vary significantly by region.

### Regional Differences

**North America**

Xbox 360 was the strongest platform during the analyzed period, followed by PS4, PS3, Xbox One, and Nintendo 3DS.

Action and Shooter were the leading genres.

**Europe**

PS4 had the highest sales, followed by PS3 and Xbox 360.

Action and Shooter were also the strongest genres.

**Japan**

Japan showed a very different market profile.

Nintendo 3DS was the strongest platform, while **Role-Playing** was the leading genre.

These results indicate that a global commercial strategy should be adapted to regional consumer preferences.

## Reviews and Sales

For PS4 games:

- Critic score correlation with sales: **0.407**
- User score correlation with sales: **-0.032**

Critic scores show a moderate positive association with sales, while user scores show almost no linear relationship with sales.

These relationships represent correlation and should not be interpreted as proof of causation.

## Statistical Hypothesis Testing

### Xbox One vs PC

**Null hypothesis:** Average user ratings for Xbox One and PC are equal.

**Alternative hypothesis:** Average user ratings are different.

Using a significance level of 5%:

**p-value = 0.549**

The null hypothesis could not be rejected.

The available data do not provide sufficient statistical evidence to conclude that average user ratings differ between Xbox One and PC.

### Action vs Sports

**Null hypothesis:** Average user ratings for Action and Sports games are equal.

**Alternative hypothesis:** Average user ratings are different.

**p-value ≈ 4.24 × 10⁻²⁰**

The null hypothesis was rejected.

The data provide strong statistical evidence that the average user ratings for Action and Sports games are different.

## Business Conclusions

For a 2017 commercial strategy:

- PS4 deserves strong attention due to its recent sales performance.
- Action and Shooter are attractive genres for broad campaigns.
- Regional differences should influence product selection and advertising.
- Japan should be treated as a distinct market, with stronger emphasis on Nintendo platforms and Role-Playing games.
- Commercial potential should not be evaluated using a single variable. Platform, genre, region, reviews, and ESRB information should be analyzed together.

## Repository Structure

```text
video-game-market-analysis/
│
├── data/
│   └── games.csv
│
├── notebooks/
│   └── video_game_market_analysis.ipynb
│
├── images/
│
├── .gitignore
├── README.md
├── README_ES.md
└── requirements.txt
```

## How to Run the Project

Clone the repository:

```bash
git clone https://github.com/sebas-arl/video-game-market-analysis.git
```

Move into the project directory:

```bash
cd video-game-market-analysis
```

Create a virtual environment:

```bash
python -m venv .venv
```

Install the dependencies:

```bash
python -m pip install -r requirements.txt
```

Open the notebook:

```text
notebooks/video_game_market_analysis.ipynb
```

## Skills Demonstrated

- Data cleaning and preprocessing
- Exploratory Data Analysis
- Data visualization
- Data aggregation
- Market segmentation
- Correlation analysis
- Statistical hypothesis testing
- Business-oriented data interpretation
- Python and Pandas workflows

## Author

**Sebastián Arcos**

Junior Data Scientist

GitHub: [sebas-arl](https://github.com/sebas-arl)