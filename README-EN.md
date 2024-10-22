## README of the Hackathon Notebook
In the Data Science repository, you will find the file hackathon.ipynb where the project is developed.

## Project Objective
The main objective of this project is to develop a Business Intelligence tool that allows entrepreneurs or companies looking to establish themselves in different neighborhoods of Barcelona to access strategic information about commercial activity in each area. Through this tool, users will be able to evaluate key aspects such as commercial density, business category diversity, the average age of establishments, and more. This will facilitate decision-making for the opening of new businesses, maximizing opportunities for success by identifying neighborhoods with high commercial potential.

## Step-by-Step Process Description
Library Import:
In the first part, the necessary libraries such as pandas for data manipulation and matplotlib for visualizing graphs are imported.

### Loading the Datasets:
The data for businesses in different neighborhoods is loaded from previously cleaned JSON files. The data contains key information such as the location of businesses, their age, activity category, and other details.

### Dataset Concatenation:
The two datasets are combined into a single DataFrame to perform a structured, joint analysis of the businesses in Barcelona's neighborhoods.

### Feature Engineering:
Multiple key features are generated to analyze the businesses by neighborhood, including:

Number of businesses per neighborhood: Calculates how many businesses there are in each neighborhood.
Diversity of categories: Measures how many different business categories exist per neighborhood.
Proportion of prominent businesses: Determines the percentage of prominent (high-value) businesses in each neighborhood.
Average business age: Calculates the average age of businesses based on their last review.
Average last modification: Extracts the average year of the last modification of businesses.
Average business value: Measures the average value of businesses in each neighborhood based on their activity group.
Geographical density: Measures the concentration of businesses based on their geographical location.
Average distance between businesses: Calculates the proximity between businesses using the standard deviation of geographic coordinates.
Businesses older than 10 years: Measures how many businesses in each neighborhood are over 10 years old.
Business growth in the last 5 years: Determines how many new businesses have been created in the last 5 years.
Business size: Classifies businesses as small, medium, or large depending on their predominant commercial activity.
Feature Combination:
All the generated features are combined into a new DataFrame, merging the information for each neighborhood to have a comprehensive view of the commercial landscape of Barcelona.

### Saving Results:
The final DataFrame containing all the business characteristics in the neighborhoods is saved in a CSV file and a JSON file. These files serve as the database for generating Business Intelligence reports.

### Business Intelligence Reports
Based on the features created during the feature engineering process, detailed reports were generated for each neighborhood in Barcelona, including:

Poblenou: With a total of 1,512 businesses, an average age of 2.64 years, and a high concentration of medium and large businesses. It is suggested to leverage the existing infrastructure for new strategic partnerships and commercial expansion.

El Clot: With 861 businesses and an average age of 2.76 years, there is a predominance of medium and small businesses. It is recommended to diversify the commercial offering to attract new investments.
