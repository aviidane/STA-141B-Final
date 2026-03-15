# STA-141B-Final

## Motivation, Background, and Problem Statement
One of the most pressing issues of the past few decades in the United States has been housing affordability. Today, research shows that more than 75% of homes nationwide are unaffordable for the typical household (Cerullo, 2025). In addition to this gap between housing costs and household income, the U.S. experiences a dramatic divergence in housing prices depending on the location (Cerullo, 2025). To understand the housing price market behavior over time, this project will investigate whether some metropolitan areas have become more expensive since 2000, and what socioeconomic factors are associated with these changes.

## Dataset Source, Variables, Size, and Relevance
For this project, we will use two different datasets:

* **Zillow Home Value Index (ZHVI):** Acquired through Zillow, an American tech real estate marketplace company. This dataset consists of the monthly estimates of home prices from January 2000 through January 2026. Key variables used include region identifiers, monthly home value estimates, and geographic classification to analyze how housing prices changed over time and across different metropolitan areas.
* **American Community Survey (ACS):** Provides data from 2009 to 2024 on metropolitan socioeconomic factors, acquired through the U.S. Census Bureau API. Key variables used include median household income, education level, poverty rate, unemployment rate, and total population. These variables will let us understand economic and demographic conditions that may relate to housing affordability.

## Expected Approach, Hypotheses, and Assumptions

### Approach
Our data analysis approach consists of three stages:
1. **Stage 1 (ZHVI Analysis):** Using `pandas`, we will reshape the ZHVI dataset from wide to long format to get one row per metropolitan area per month. We will compute housing prices and how those prices have changed over time, focusing on the 2009 through 2024 timeline.
2. **Stage 2 (ACS Integration):** Using the Census API, we will download 5-year ACS estimates for 2009 through 2024, clean and format the responses into `pandas` DataFrames, and merge them with the ZHVI dataset. This combined dataset maps changes in housing prices to changes in socioeconomic factors.
3. **Stage 3 (Visualization):** Using `matplotlib` and `seaborn`, we will visualize and analyze the relationships between housing prices and socioeconomic factors like income, education, and population size.

### Hypotheses
1. **Hypothesis 1:** The housing market in U.S. metropolitan areas started experiencing a rapid and sustained increase in prices in the 2000s, continuing up to 2026.
2. **Hypothesis 2:** Between 2009 and 2024, greater growth in housing prices is strongly associated with metropolitan areas exhibiting strong socioeconomic characteristics, such as high income, high education levels, and faster population growth.

### Assumptions and Limitations
* **Assumptions:** We assume that the ZHVI dataset—which consists of monthly estimates of typical home sale prices rather than observed transaction prices—accurately reflects typical home prices and allows for consistent comparison across different metropolitan areas.
* **Limitations:** The ACS dataset averages data across five consecutive years of surveys. This provides rolling estimates rather than point-in-time data, preventing us from analyzing socioeconomic factors for a single, specific year. Additionally, geographical matching between the Zillow and Census datasets may not align perfectly, which may slightly restrict our metropolitan analysis.

## How to Run
* **Prerequisites:** Python 3.x with `pandas`, `matplotlib`, `seaborn`, and `requests` (to query the Census API).
* **Execution:** Clone this repository and run all cells in `STA141B_Housing_Project_Final.ipynb`.
