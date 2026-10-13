# Airbnb NYC Market, Location, and Customer Insight Dashboard

An interactive Tableau dashboard exploring Airbnb listing locations, prices, room types, and review activity in New York City. Data preparation was carried out in Excel Power Query before building the visualisations in Tableau.

**Tools:** Microsoft Excel, Power Query, and Tableau Public.

## Project Overview

This project explores how Airbnb listings are distributed across New York Citys`` five boroughs and how prices vary by location and room type. It also examines the relationship between listing prices and review counts, alongside the year of each listing's most recent review.

The dashboard is designed for analysts and hosts who want to explore these patterns through maps, charts, filters, and listing-level tooltips.

## Dataset and Data Preparation

The project uses **Airbnb Open Data** from Kaggle. Each row represents a listing, with fields covering its location, property characteristics, price, reviews, and availability.

| Stage | Records |
| --- | ---: |
| Original dataset | 103,006 |
| After data cleaning | 81,830 |
| Random sample used in Tableau | 40,000 |

The data preparation process in Excel Power Query included:

- Renaming columns to make their meaning clearer.
- Removing duplicate records using `Listing ID`.
- Filtering missing values in selected analytical fields and replacing missing host names with `Unknown Host`.
- Setting appropriate data types for categories, numbers, geographic coordinates, and dates.
- Adding a `Random Number` column with `Number.Random()`, sorting the records by that column, and keeping 40,000 rows for analysis.

The final sample was used to keep the Tableau workbook lighter while supporting exploratory analysis.

## Dashboard Features

| Visualisation | Purpose |
| --- | --- |
| **Geospatial density map** | Shows where listings are concentrated across NYC. |
| **Average price heat map** | Compares average listing prices across boroughs and room types. |
| **Price vs. number of reviews scatter plot** | Explores price variation among listings with different review counts, coloured by room type. |
| **Listings by last review year** | Groups listings by the year of their most recent review. |

The exploratory analysis also includes a **price histogram with $100 bins** to examine the distribution of listing prices.

### Interactive Controls

- **Neighbourhood Group:** Select a borough, such as Manhattan or Brooklyn.
- **Room Type:** Explore entire homes/apartments, private rooms, shared rooms, or hotel rooms.
- **Number of Reviews:** Adjust the review-count range for the scatter plot.
- **Tooltips:** View additional information such as listing name, location, price, and review rating.

The scatter plot shown in the report focuses on listings with at least **100 reviews**.

## Dashboard Preview

<img width="1751" height="934" alt="Screenshot 2026-10-13 163201" src="https://github.com/user-attachments/assets/bbb7ee56-76a4-4631-8581-5a2c62520442" />


## Key Findings

| Finding | Interpretation |
| --- | --- |
| Listings are more concentrated around **Manhattan and Brooklyn** in the density map. | These boroughs contain prominent clusters of listings in the sample. |
| **Hotel rooms in Brooklyn** have an average listing price of about **$730**, compared with about **$515 in Queens**. | Average prices differ across borough–room type combinations. The number of listings in each group matters when comparing these averages. |
| Listings with high review counts appear at different price levels. | Among the listings shown, more reviews do not consistently correspond to higher prices. |
| **9,539 Manhattan listings** have their most recent review in **2019**. | This describes the last-review year of those listings, rather than the number of reviews submitted during 2019. |
| Listing counts are broadly similar across the **$100 to $1,100 price bins**. | The histogram shows a relatively even distribution across these bins in the sample. |

## Interpretation Notes

- The findings describe a **40,000-row sample** of the cleaned dataset. Removing records with missing values can affect which listings remain in the analysis.
- `Last Review Date` records each listing's latest review. It does not establish annual review totals or growth in the number of listings.
- Review counts provide context about review activity. They do not establish listing quality, occupancy, or revenue.
- Prices are values recorded in the dataset and do not establish actual transaction prices or current market conditions.

## Project Links

- [Interactive dashboard on Tableau Public](https://public.tableau.com/views/AirbnbNYCMarketLocationandCustomerInsightDashboard/Dashboard1)
- [Source dataset on Kaggle](https://www.kaggle.com/datasets/arianazmoudeh/airbnbopendata)

## Author

Nacito Florisen Astari
