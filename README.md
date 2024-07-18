# A Comprehensive Analysis of Airbnb Pricing Strategies

This repository contains the final project from the IST 652 Scripting for Data Analysis course. The project applies data mining techniques to analyze and model Airbnb pricing strategies, providing insights for hosts to optimize their rental prices and for guests to find the perfect rental. The study draws parallels with real-world economic principles and offers actionable recommendations based on historical data.

## Table of Contents
- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Skills Demonstrated](#skills-demonstrated)
- [Dataset](#dataset)
  - [Calendar Data](#calendar-data)
  - [Listings Data](#listings-data)
  - [Reviews Data](#reviews-data)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
  - [Calendar Data Cleaning](#calendar-data-cleaning)
  - [Listings Data Cleaning](#listings-data-cleaning)
  - [Reviews Data Cleaning](#reviews-data-cleaning)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
  - [Methods of Analysis](#methods-of-analysis)
- [Key Findings](#key-findings)
- [Repository Structure](#repository-structure)

## Project Overview

The tourism industry is a significant economic driver worldwide, with Airbnb emerging as a major player in the market. This project aims to leverage historical Airbnb data to develop a comprehensive tool that helps hosts optimize their rental pricing strategies and assists guests in finding the ideal rental property. Through data exploration, linear regression analysis, correlation matrices, decision trees, and random forest models, this project seeks to uncover trends and provide actionable insights for both hosts and guests.

## Objectives

- **Analyze** the economic behavior in Airbnb’s rental market.
- **Model** the fluctuating rental prices using machine learning techniques.
- **Predict** optimal rental prices to provide strategic insights for hosts.
- **Visualize** key trends and patterns in the rental market.

## Skills Demonstrated

- **Data Preprocessing**: Cleaning and preparing data for analysis.
- **Machine Learning**: Implementing algorithms such as Linear Regression, Decision Trees, and Random Forest.
- **Data Visualization**: Creating insightful visualizations to highlight trends.
- **Statistical Analysis**: Conducting correlation and regression analyses.

## Dataset
![image](https://github.com/user-attachments/assets/99e9840a-270c-48a2-b043-d689e847aee0)

The dataset, sourced from Kaggle, includes detailed information about Airbnb listings in Seattle, with key variables:

### Calendar Data

- **listing_id**: Unique identifier for the listing.
- **date**: Date of the listing.
- **available**: Availability status (True/False).
- **price**: Price of the listing.

### Listings Data

- **id**: Unique identifier for each listing.
- **listing_url**: URL of the listing.
- **name**: Name of the listing.
- **summary**: Summary description of the listing.
- **space**: Detailed description of the listing space.
- **description**: Full description of the listing.
- **neighborhood_overview**: Description of the neighborhood.
- **notes**: Additional notes about the listing.
- **transit**: Information about nearby transit options.
- **picture_url**: URL for the listing's pictures.
- **host_id**: Unique identifier for the host.
- **host_name**: Name of the host.
- **host_since**: Date since the host joined Airbnb.
- **host_response_time**: Average response time of the host.
- **host_response_rate**: Response rate of the host.
- **host_is_superhost**: Whether the host is a superhost (True/False).
- **host_listings_count**: Number of listings the host has.
- **host_verifications**: Verification details of the host.
- **street**: Street address of the listing.
- **neighborhood**: Neighborhood of the listing.
- **city**: City of the listing.
- **state**: State of the listing.
- **zipcode**: Zip code of the listing.
- **latitude**: Latitude coordinates of the listing.
- **longitude**: Longitude coordinates of the listing.
- **property_type**: Type of property.
- **room_type**: Type of room.
- **accommodates**: Number of guests the listing can accommodate.
- **bathrooms**: Number of bathrooms.
- **bedrooms**: Number of bedrooms.
- **beds**: Number of beds.
- **amenities**: List of amenities available.
- **price**: Price per night.
- **weekly_price**: Weekly price.
- **monthly_price**: Monthly price.
- **security_deposit**: Security deposit amount.
- **cleaning_fee**: Cleaning fee.
- **guests_included**: Number of guests included in the price.
- **extra_people**: Additional charge for extra guests.
- **minimum_nights**: Minimum number of nights for booking.
- **maximum_nights**: Maximum number of nights for booking.
- **number_of_reviews**: Number of reviews the listing has received.
- **first_review**: Date of the first review.
- **last_review**: Date of the last review.
- **review_scores_rating**: Overall rating score.
- **review_scores_accuracy**: Accuracy rating score.
- **review_scores_cleanliness**: Cleanliness rating score.
- **review_scores_checkin**: Check-in rating score.
- **review_scores_communication**: Communication rating score.
- **review_scores_location**: Location rating score.
- **review_scores_value**: Value rating score.

### Reviews Data

- **listing_id**: Unique identifier for the listing.
- **id**: Unique identifier for the review.
- **date**: Date of the review.
- **reviewer_id**: Unique identifier for the reviewer.
- **reviewer_name**: Name of the reviewer.
- **comments**: Review comments.

## Data Cleaning and Preparation

In data science, clean data is essential for accurate analysis. This project involved extensive data cleaning and preparation to ensure the datasets were ready for analysis.
![image](https://github.com/user-attachments/assets/57b23ce3-55be-485c-8450-4e6af6fff19b)

### Calendar Data Cleaning

- Removed dollar signs from the price column and converted it to numeric.
- Converted the date column to datetime format.
- Converted the availability column to Boolean (True/False).
- Removed rows with missing or null values.

### Listings Data Cleaning

- Removed irrelevant columns such as URLs and host details not needed for analysis.
- Converted price-related columns to numeric.
- Converted date columns to datetime format.
- Filled missing values in text columns with empty strings.
- Created new variables: price per bedroom and price per guest.

### Reviews Data Cleaning

- Converted date columns to datetime format.
- Filled missing values in the comments column with empty strings.

## Exploratory Data Analysis (EDA)
![image](https://github.com/user-attachments/assets/e2fef151-e802-44c0-9405-ae4988808653)

EDA helps to understand the data better, identify patterns, and detect anomalies. The following questions were explored during the EDA:

- **What is the most common price range for Airbnb listings in Seattle?**
- **How can hosts price their properties competitively within these ranges?**

### Methods of Analysis

1. **Average Listing Prices by Neighborhood**
    - Calculated the average price and grouped them by neighborhood.
    - Found that Delridge neighborhood was the cheapest at $83, while Magnolia was the most expensive at $177.
![image](https://github.com/user-attachments/assets/d86617ff-e138-4fc6-b7d6-9fd77e413819)

2. **Predicting Host Listing Prices**
    - Developed a program to predict listing prices based on features like bedrooms, bathrooms, and zip code.
![image](https://github.com/user-attachments/assets/d1d98006-20df-474b-b3ae-e07c385d072e)
![image](https://github.com/user-attachments/assets/00191826-8608-4e05-8a26-ea8182c5a5e7)
![image](https://github.com/user-attachments/assets/7de8f0e3-d448-49f8-933b-5897aec389a6)

3. **Keyword Search on Amenities**
    - Created a function to perform keyword searches on amenities within a listing and return core features.
![image](https://github.com/user-attachments/assets/028adfcb-0ec9-4bc5-aa1e-6cb04a01eb28)

4. **Correlation Analysis**
    - Analyzed the correlation between host response rate and review categories.
![image](https://github.com/user-attachments/assets/8814ec40-cca2-4def-8e47-5383fc3d864a)

5. **Top 10 Airbnb Listings in Seattle**
    - Sorted review scores to find the top-rated listings.
![image](https://github.com/user-attachments/assets/585ef30d-41ae-4f5e-91d1-2d518081adf6)

6. **Impact of Reviews and Review Scores on Price**
    - Used random forest models to analyze the impact of reviews and review scores on listing prices.
    - MSE: 8369.73, RMSE: 91.48 and R^2: 0.38%
![image](https://github.com/user-attachments/assets/1482dabe-0f14-4d4b-bfc4-c3b61281ef20)

7. **Predicting Future Prices**
    - Developed a model to predict future listing prices based on historical data.
    - MSE: 4312.98, RMSE: 65.67 and R^2: 0.48%
![image](https://github.com/user-attachments/assets/dde9054f-12f8-40a8-8851-424fafd363a2)

## Key Findings

- **Market Dynamics**: Identified pricing trends and competitive ranges.
- **Host Insights**: Provided hosts with tools to optimize their pricing strategies.
- **Guest Insights**: Helped guests find the best rentals based on specific criteria.
- **Predictive Insights**: Achieved high accuracy in predicting listing prices, offering strategic insights for both hosts and guests.

## Repository Structure
```plaintext
Airbnb-Price-Analysis-Seattle/
├── data/
│   ├── raw/
│   │   ├── calendar.csv
│   │   ├── listings.csv
│   │   └── reviews.csv
│   ├── processed/
│   │   ├── cleaned_calendar.csv
│   │   ├── cleaned_listings.csv
│   │   └── cleaned_reviews.csv
├── Airbnb_Price_Analysis_Seattle.ipynb
├── Airbnb_Price_Analysis_Seattle_Report.docx
├── README.md
└── LICENSE
