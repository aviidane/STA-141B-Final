# STA-141B-Final
#  Motivation, Background, and Problem Statement
One of the most pressing issues of the past few decades in the United States of America has been housing affordability. Today, research shows that more than 75% of homes nationwide are unaffordable for the typical household (Cerullo, 2025). In addition to this gap between housing costs and household income, the United States of America experiences a dramatic divergence in housing prices depending on the location (Cerullo, 2025). To understand the housing price market behavior over time, this project will investigate whether some metropolitan areas have become more expensive since 2000, and what socioeconomic factors are associated with these changes.

Dataset Source, Variables, Size, and Relevance
For this project, we will use two different datasets. The first dataset, called Zillow Home Value Index (ZHVI), was acquired through Zillow, an American tech real estate marketplace company. This dataset consists of the monthly estimates of home prices from January 2000 through January 2026. In this project, we will also use such variables from the ZHVI dataset as region identifiers, monthly home value estimates, and geographic classification to analyze how housing prices changed over time and across different metropolitan areas.

The second dataset is an American Community Survey (ACS) that provides data from 2009 to 2024 on metropolitan socioeconomic factors. This dataset was acquired through the U.S. Census Bureau API. The key variables used in this dataset are median household income, education level, poverty rate, unemployment rate, and total population. These variables will let us understand economic and demographic conditions that may relate to housing affordability.

### Expected Approach, Hypotheses, and Assumptions
In this project, our approach will consist of three data analysis stages. First, using the ZHVI dataset, we will study the changes in housing prices across different metropolitan areas from 2000 to 2026. To achieve this, we will use pandas to reshape the ZHVI dataset from wide to long format, to get one row per metropolitan area per month. After this, for each metropolitan area, we will compute housing prices and how those prices have changed over time, with the focus on the 2009 through 2024 timeline.

In the second stage, we integrate the ACS dataset. By using the Census API, we will download the ACS data for the 5-year estimates for 2009 through 2024, clean the data, format the responses into pandas DataFrames, and merge the ACS dataset with the ZHVI dataset from the first stage. As a result, this combined dataset will contain the changes in housing prices and the changes in socioeconomic factors for each metropolitan area.

The third stage of the project will consist of developing visualizations. Using matplotlib/seaborn, we will visualize and analyze the relationships between housing prices and such socioeconomic factors as income and population size.

In this project, we developed two hypotheses. 

Hypothesis 1: The housing market in the metropolitan areas of the United States of America started experiencing a rapid increase over time in housing prices in the 2000s, up to 2026.

Hypothesis 2: Between 2009 and 2024, the United States of America housing market is associated with a greater growth in housing prices in the metropolitan areas with strong socioeconomic characteristics, such as high income, high education level, and faster population growth.

We also want to acknowledge that, for this project, we will assume that the ZHVI dataset, consisting of monthly estimates of the typical home sale prices and not observed transaction prices, accurately reflects the typical home prices and would allow us to consistently compare housing prices across different metropolitan areas. We will also acknowledge a few limitations. For example, it is important to note that the ACS dataset averages data across five consecutive years of surveys. Therefore, the data provides estimates that reflect an average across five years, which prevents us from analyzing socioeconomic factors at a specific year. Finally, it is important to note that the matching between two datasets may not be exactly aligned, which may restrict our metropolitan analysis.
