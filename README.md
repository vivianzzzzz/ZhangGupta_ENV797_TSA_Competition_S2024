# README
## TSA: Forecasting Competition

## Overview
This repository is part of the TSA: Forecasting Competition, aimed at predicting daily demand for January 2011 using historical data on hourly demand, temperature, and relative humidity from January 2005 to December 2010. This project is managed by Luana Lima as of 03/20/2024.

## Repository Setup
To clone this repository and work with it locally using RStudio, follow these steps:

1. Copy the repository's HTTPS clone URL from GitHub.
2. Open RStudio and select "New Project" from the File menu.
3. Choose "Version Control", then "Git", and paste the repository URL.
4. Set your preferred directory and project name.

## Data
The `/Competition/Data` directory contains three datasets:
- Hourly demand
- Hourly temperature
- Relative humidity

## Data Wrangling
Hourly data is transformed into daily averages using the method outlined in the R markdown file from Lesson 11, utilizing pipes for efficient data aggregation.

## Time Series Object Creation
The processed dataset is converted into a time series object using the `msts()` function from the `forecast` package in R, which allows handling multiple seasonal components.

## Collaboration
Group members are invited to collaborate on this repository to contribute to the forecasting model development.

## License
This project is open source and available under the GNU General Public License v3.0. See the LICENSE file for more information.

