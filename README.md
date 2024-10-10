# nosql-challenge

This project involves using MongoDB to analyze fictional food hygiene ratings across various fictional establishments in the UK. The goal is to help the fictional 'Eat Safe, Love' magazine gain insights into the hygiene standards of different locations and assist their editorial team in focusing on specific areas and establishments for future stories.

## Project Overview
The analysis is structured into two main parts:

### 1. Database Setup & Data Cleaning: 
Initial setup of the MongoDB database, adding new records, updating existing entries, and removing irrelevant data.

### 2. Exploratory Analysis: 
Using queries and aggregation techniques to extract meaningful insights, such as identifying high-risk establishments and finding top-rated venues near a specific location.

## Code Highlights

### Part 1: Database Setup and Modifications

#### Data Import: 
Data from establishments.json is imported into a MongoDB collection named establishments in the uk_food database. This is achieved using the following command:

    mongoimport --db uk_food --collection establishments --file establishments.json --jsonArray --drop
 
#### Database Connection: 
Established using the PyMongo library

#### Insertion & Updates: 
Added a new restaurant (Penang Flavours) and updated its details, including setting the correct BusinessTypeID.

#### Data Type Conversion: 
Used the update_many() method to convert latitude, longitude, and rating values to proper numerical types.

### Part 2: Exploratory Data Analysis

#### 1. Identifying Establishments with Poor Hygiene:
    -Queried for establishments with a hygiene score of 20, displaying the results using Pandas DataFrame for clarity.

#### 2. Top-Rated London Establishments:
    -Retrieved establishments in the London area with a rating of 4 or higher using regex filtering.

#### 3. Finding Top 5 Establishments Near a Specific Restaurant:
    -Filtered establishments near the newly added Penang Flavours based on latitude and longitude proximity.

#### 4. Local Authority Analysis:
    -Aggregated and sorted local authority areas based on the count of establishments with a hygiene score of 0.

## Project Outcomes

### The analysis revealed several key insights:

    -Specific establishments with extremely poor hygiene that require immediate attention.
    
    -Top-rated establishments in the London area suitable for feature articles.
    
    -Areas with high concentrations of low-scoring venues, which can be useful for investigative stories.
    
    -By using MongoDB and performing structured analysis, this project helps the magazine team make data-driven decisions for their editorial focus.


## References

ChatGPT was used for README outline and format, and troubleshooting errors for this assignment.

OpenAI. (October, 2024). ChatGPT (GPT-4) [Large language model]. https://chat.openai.com/
