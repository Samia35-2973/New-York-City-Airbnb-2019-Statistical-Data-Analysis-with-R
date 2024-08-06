**Analysis Covered in the Repository:**

- **Understanding Data**
- **Handling Missing Data**
- **Summary Statistics of Numerical Values**
- **Summary Statistics of Categorical Values**
- **Total Listings Per Neighbourhood Group**
- **Total Listings Per Room Type**
- **Distribution of Price**
- **Outlier Detection**
- **Distribution of Longitude & Latitude**
- **Correlation Heatmap**
- **Insights on Popularity**
- **Distribution of Listings Across Neighborhood Groups**
- **Insights on Most Popular Area in Manhattan**
- **Factors Influencing Popularity in Manhattan**
- **Insights on Least Popular Area in Manhattan**
- **Factors Influencing Least Popularity in Manhattan**
- **Insights on Most Popular Area in Staten Island**

---

# Usage Details
It is advised to load the `Rmd` file in VSCode with an extension to preview the `Rmd` file or in R studio as this is an R notebook. Make sure to put the csv file in the same directory. 

1. You can clone the repository by following the command
   ```bash
   git clone https://github.com/Samia35-2973/New-York-City-Airbnb-2019-Statistical-Data-Analysis-with-R.git
   ```
2. Then open the directory on VSCode with R Markdown or Just open the `Rmd` file in R Studio.

# Airbnb NYC 2019 Data Analysis

## Overview

This repository contains an in-depth analysis of the Airbnb listings in New York City for the year 2019. The analysis leverages R for statistical data analysis to understand patterns, trends, and insights from the dataset.

## Understanding Data

### Head of the Data

The first five rows of the dataset showcase essential details about each listing, including ID, name, host information, location, room type, price, and availability.

### Dimensions

The dataset contains 48,895 entries and 16 columns, offering a comprehensive snapshot of Airbnb listings in New York City for the year 2019.

### Numerical & Categorical Columns

The numerical and categorical columns are extracted from the dataset and further divided based on knowledge:

- **Discrete Numerical Variables**:
  - `id`: Listing ID
  - `host_id`: Host ID
  - `price`: Price in Dollars
  - `minimum_nights`: Amount of nights minimum
  - `number_of_reviews`: Number of reviews given
  - `calculated_host_listings_count`: Amount of listing per host
  - `availability_365`: Number of days when listing is available for booking

- **Continuous Numerical Variables**:
  - `latitude`: Latitude coordinates
  - `longitude`: Longitude coordinates
  - `reviews_per_month`: Number of reviews per month

- **Nominal Categorical Variables**:
  - `name`: Name of the listing
  - `host_name`: Name of the host
  - `neighbourhood_group`: Location
  - `neighbourhood`: Area
  - `room_type`: Listing space type

- **Ordinal Categorical Variables**:
  - `last_review`: Latest Review

- **Useless Variables**:
  - `id`
  - `host_id`
  - `name`
  - `host_name`
  - `last_review`

## Data Preprocessing

### Handling Missing Data

In the dataset, two variables were identified with missing values:

- **reviews_per_month**:
  - 10,052 missing values were replaced with the mean value of the column.

- **last_review**:
  - 10,100 missing values were replaced with the median date after converting the dates to the "Date" type.

These imputation strategies aim to maintain the quality and completeness of the dataset, allowing for a more robust analysis.

## Summary Statistics

### Summary Statistics of Numerical Values

- **Mean**: Represents the arithmetic average.
- **Median**: Middle value of the dataset.
- **Mode**: Most frequently occurring value.
- **Variance**: Degree of spread or dispersion.
- **Standard Deviation**: Average distance of each data point from the mean.
- **25% and 75% Quantiles**: First and third quartile.
- **Minimum and Maximum**: Smallest and largest values.
- **Range**: Difference between the maximum and minimum values.
- **Interquartile Range (IQR)**: Range between the first quartile (Q1) and the third quartile (Q3).

### Summary Statistics of Categorical Values

- **Mode**: Most frequently occurring category.

## Total Listings

### Total Listings Per Neighbourhood Group
- The number of listings in each neighborhood group.

### Total Listings Per Room Type
- The number of listings for each room type.

## Data Visualization of Summary Statistics

### Distribution of Price

- **Figure**: Histogram of Price and Density Plot of Price
- **Initial Observations**: High positive skewness, suggesting a few listings with significantly higher prices.
- **Log Transformation**: Applied to address the skewness and create a more symmetric distribution.
- **Post-Transformation Observation**: More balanced and interpretable distribution of prices.

### Outlier Detection

- **Box Plot for Numerical Features**: Identification of extreme outliers in features like `price`, `reviews_per_month`, and `number_of_reviews`.
- **Bar Plots for Categorical Features**: Potential imbalances in features like `neighbourhood_group` and `room_type`.

### Distribution of Longitude & Latitude

- **Figure**: Scatter Plot of Longitude and Latitude
- **Observations**: No significant linear correlation between longitude and latitude (correlation: 0.0848).

## Correlation Heatmap

### Key Correlations

- **Number of Reviews and Reviews per Month (0.55)**: Moderate positive correlation.
- **Availability_365 and Number of Reviews (0.19)**: Weak positive relationship.
- **Availability_365 and Reviews per Month (0.19)**: Weak positive relationship.
- **Availability_365 and Calculated Host Listings Count (0.18)**: Weak positive relationship.

## Insights on Popularity

### Distribution of Listings Across Neighborhood Groups

- **Figure**: Bar Chart of Neighborhood Group
- **Observations**: 'Manhattan' has the highest number of listings, while 'Staten Island' has the lowest.

### Insights on Most Popular Area in Manhattan

- **Financial District**: Highest total listings per host.
- **Harlem**: Most popular based on the number of reviews.
- **Factors Influencing Popularity**: Right-skewed distribution for "Entire home/apt" room type, normal distribution for "Private room," and flatter distribution for "Shared room."

### Insights on Least Popular Area in Manhattan

- **Marble Hill**: Least popular area based on total listings per host and number of reviews.
- **Factors Influencing Least Popularity**: Right-skewed distribution for "Entire home/apt" and less distinct distribution for "Private room."

### Insights on Most Popular Area in Staten Island

- **Concord**: Most popular area based on total listings per host.
- **Tompkinsville**: Most popular based on the number of reviews and combined reviews and listings score.

## Conclusion

This repository provides a comprehensive analysis of Airbnb listings in New York City for 2019, highlighting key insights, trends, and patterns. The analysis aims to help hosts, guests, and researchers understand the dynamics of the Airbnb market in NYC, providing valuable information for strategic decision-making.
