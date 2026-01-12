# Executive Summary - NYC TLC EDA (Course 3)

## Overview
Completed exploratory data analysis (EDA) on the NYC TLC taxi dataset and created visualizations to summarize ridership patterns and data quality. The current file contains 22,699 trips from 2017 (appears to be a sample of the full TLC data).

## Work completed
- Loaded and structured the dataset, including ID cleanup and datetime parsing.
- Created derived features: trip duration (minutes), pickup month/quarter/hour, and estimated speed.
- Produced EDA plots: trip duration box plot, trip distance distribution, monthly and quarterly time series, payment type and passenger count distributions, and top pickup locations.
- Documented Tableau visualization plan with accessibility considerations.

## Key findings
- Trip duration: median 11.18 minutes (IQR 6.65 to 18.38), mean 17.01 minutes, with extreme outliers up to 1,439.55 minutes.
- Trip distance: median 1.61 miles, mean 2.91 miles, with a long right tail (max 33.96 miles).
- Fare amount: median $9.50, mean $13.03; outliers include negative fares (-$120) and very high values ($999.99).
- Payment type: credit card is dominant (67.2%), cash is 32.0%; other types are less than 1% combined.
- Passenger count: single-passenger trips dominate (71.0%), followed by two passengers (14.6%).
- Time series: trips are relatively stable across months (about 1.7k to 2.0k per month in this file).

## Data quality notes
- 14 trips with negative fare amounts (0.1%), 1 trip with negative duration, and 148 trips with zero distance (0.7%). These should be filtered or reviewed.
- Store-and-forward is rare (0.4%), suggesting most trips are transmitted live.

## Recommended next steps
- Confirm whether this file is a sample and request the full 2017 dataset if needed.
- Define cleaning rules: remove negative/zero durations, handle zero distance and negative fares, and cap extreme outliers for modeling.
- Join TLC zone lookup data to convert pickup/dropoff IDs into readable locations.
- Build modeling-ready features (time-of-day, day-of-week, holiday flags, trip speed) and proceed to train baseline predictive models.
