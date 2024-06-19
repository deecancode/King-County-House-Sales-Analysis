# King-County-House-Sales-Analysis

This repository contains a Jupyter Notebook that analyzes and predicts housing prices in King County, USA, using various features of the houses. The dataset includes homes sold between May 2014 and May 2015.

## Dataset Description

The dataset contains the following columns:

| Variable      | Description                                                                                                 |
| ------------- | ----------------------------------------------------------------------------------------------------------- |
| id            | A notation for a house                                                                                      |
| date          | Date house was sold                                                                                         |
| price         | Price is prediction target                                                                                  |
| bedrooms      | Number of bedrooms                                                                                          |
| bathrooms     | Number of bathrooms                                                                                         |
| sqft_living   | Square footage of the home                                                                                  |
| sqft_lot      | Square footage of the lot                                                                                   |
| floors        | Total floors (levels) in house                                                                              |
| waterfront    | House which has a view to a waterfront                                                                      |
| view          | Has been viewed                                                                                             |
| condition     | How good the condition is overall                                                                           |
| grade         | Overall grade given to the housing unit, based on King County grading system                                |
| sqft_above    | Square footage of house apart from basement                                                                 |
| sqft_basement | Square footage of the basement                                                                              |
| yr_built      | Built Year                                                                                                  |
| yr_renovated  | Year when house was renovated                                                                               |
| zipcode       | Zip code                                                                                                    |
| lat           | Latitude coordinate                                                                                         |
| long          | Longitude coordinate                                                                                        |
| sqft_living15 | Living room area in 2015 (implies some renovations)                                                         |
| sqft_lot15    | Lot size area in 2015 (implies some renovations)                                                            |

## Notebook Structure

The notebook is divided into several modules:

1. **Importing Data**: Load the dataset and display the first few rows.
2. **Data Wrangling**: Clean the data by handling missing values and dropping unnecessary columns.
3. **Exploratory Data Analysis**: Analyze the data to find patterns and relationships between features.
4. **Model Development**: Develop machine learning models to predict house prices.
5. **Model Evaluation and Refinement**: Evaluate and refine the models to improve their performance.

## Key Steps and Outputs

1. **Data Import and Initial Exploration**:
    - Load the dataset from a CSV file.
    - Display the first few rows and data types of each column.

2. **Data Cleaning**:
    - Drop columns `id` and `Unnamed: 0`.
    - Replace missing values in `bedrooms` and `bathrooms` with their respective means.

3. **Exploratory Data Analysis**:
    - Count the number of houses with unique floor values.
    - Use boxplots to analyze price outliers for houses with and without waterfront views.
    - Use regression plots to determine the correlation between `sqft_above` and `price`.

4. **Model Development**:
    - Fit a linear regression model using `sqft_living` to predict `price` and calculate R².
    - Fit a linear regression model using multiple features and calculate R².
    - Create a pipeline with scaling, polynomial features, and linear regression to predict `price`.

5. **Model Evaluation**:
    - Split the data into training and testing sets.
    - Fit a Ridge regression model and calculate R² on the test data.
    - Perform a second-order polynomial transform and fit a Ridge regression model to calculate R².

## Authors

- **Joseph Santarcangelo**: PhD in Electrical Engineering, IBM.
- **Michelle Carey**: Contributor.
- **Mavis Zhou**: Contributor.
- **Nabelou Ouologuem**: Implemented the code and analysis for this project.

## License

© IBM Corporation 2020. All rights reserved.
