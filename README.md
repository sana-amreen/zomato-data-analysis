# Zomato Bangalore Restaurant Analysis
Analysis of Zomato restaurant data using Python and Power BI to uncover insights on cuisine performance, location trends, pricing, and what makes a restaurant successful.

## Overview
This project performs an exploratory data analysis of 50,000+ restaurants listed on Zomato in Bangalore. Using Python for data cleaning and analysis and Power BI for an interactive dashboard, I investigated key factors that influence restaurant ratings — including cuisine type, location, pricing, online ordering, and restaurant format.

## Dataset
- **Source:** [Zomato Bangalore Dataset — Kaggle](https://www.kaggle.com/datasets/rajeshrampure/zomato-dataset)
- **Size:** 51,717 rows, 17 columns
- **Coverage:** Restaurants across Bangalore listed on Zomato
- **Columns:** url, address, name, online_order, book_table, rate, votes, phone, location, rest_type, dish_liked, cuisines, approx_cost(for two people), reviews_list, menu_item, listed_in(type), listed_in(city)

## Tools & Technologies
- **Python** — Pandas, Numpy, Matplotlib, Seaborn
- **Dashboard** — Power BI
- **Environment** — Jupyter Notebook

## Data Cleaning
- Removed `/5` suffix from rating column and converted to float
- Removed commas from cost column and converted to integer
- Filled missing `rest_type` values using `listed_in(type)` as a proxy
- Exploded multi-value cuisine column so each cuisine could be analysed individually
- Dropped rows with missing ratings as they could not be analysed
- Stripped whitespace and standardised capitalisation across all text columns

## Business Questions Answered

### Cuisine Analysis
1. Which cuisines have the highest average ratings on Zomato?
2. Which cuisines have the lowest average ratings?

### Location Analysis
3. Which areas in Bangalore have the highest rated restaurants?
4. What is the top rated restaurant in each area?

### Pricing Analysis
5. Does spending more guarantee a better rated restaurant?
6. Which price bracket — budget, mid, premium or luxury — performs best?

### Online Ordering
7. Do restaurants that accept online orders rate higher than those that don't?
8. How many restaurants offer online ordering vs those that don't?

### Restaurant Type
9. Which restaurant format — casual dining, quick bites, café — has the highest average rating?

### Popularity vs Quality
10. Is there a correlation between number of votes and restaurant rating?

## Key Insights
1. **Cuisine** — Cantonese cuisine has the highest average rating of 4.60
2. **Location** — Restaurants in Lavelle Road consistently outperformed other areas with an average rating of 4.1
3. **Price** — Luxury restaurants (₹1000 for two) rated higher than other restaurants on average
4. **Online Ordering** — Restaurants accepting online orders rated slightly higher than those that don't. The difference in average rating was only 0.06
5. **Restaurant Type** — Microbrewery, Pub  outperformed other types of restaurants withg the average rating of 4.45
6. **Popularity vs Quality** — Votes and ratings show a moderate positive correlation of 0.46, suggesting popularity and quality do not always align
## Dashboard
View the interactive Power BI dashboard here:
[Zomato Restaurant Analysis — Power BI Dashboard]()

## What I Learned
- Handling and cleaning real-world messy data including multi-value columns, mixed format strings and inconsistent text
- Using pandas `.explode()` to analyse multi-value columns like cuisines
- Making data-driven decisions on null value handling rather than defaulting to dropping all missing rows
- Building an interactive Power BI dashboard with slicers and cross-filtering
- Translating a business question into a structured end-to-end analysis
