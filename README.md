# Uber Request Data Analysis

## Overview
This project analyzes Uber trip request data to identify key patterns and insights related to trip statuses, request times, and pickup locations. The analysis focuses on understanding the supply-demand gap, peak request times, and the distribution of trip statuses.

## Dataset
The dataset used in this analysis contains 6,745 entries with the following columns:

- **Request id**: Unique identifier for each trip request.
- **Pickup point**: Location from where the trip was requested (City or Airport).
- **Driver id**: Unique identifier for the driver. This value is missing when no car is available.
- **Status**: Outcome of the trip request (Trip Completed, Cancelled, No Cars Available).
- **Request timestamp**: Date and time when the trip was requested.
- **Drop timestamp**: Date and time when the trip was completed. This value is missing when the trip is not completed.

## Libraries Used
The following Python libraries are used for data processing and visualization:

- `pandas`: For data manipulation and analysis.
- `numpy`: For numerical operations.
- `matplotlib`: For creating static, animated, and interactive visualizations.
- `seaborn`: For statistical data visualization.
- `statsmodels`: For statistical modeling and analysis.

## Data Preprocessing
1. **Loading Data**: The dataset is loaded into a Pandas DataFrame from a CSV file.
2. **Data Cleaning**:
    - Converted `Request timestamp` and `Drop timestamp` to datetime format.
    - Checked for duplicate entries and missing values.
3. **Feature Engineering**:
    - Extracted the hour from the `Request timestamp`.
    - Extracted the day of the week from the `Request timestamp`.
    - Created a `Time slot` column to categorize requests into time periods (Early Morning, Morning, Day Time, Evening, Late Night).

## Analysis and Visualizations
1. **Trip Status Distribution**:
    - A pie chart showing the percentage of trips that were completed, cancelled, or had no cars available.
2. **Hourly Distribution of Requests**:
    - A histogram showing the distribution of trip requests across different hours of the day.
3. **Daywise Distribution**:
    - A count plot showing the distribution of requests across different days of the week.
4. **Pickup Point Analysis**:
    - A bar chart showing the relationship between trip status and pickup location (City or Airport).
5. **Time Slot Analysis**:
    - A bar chart showing the number of requests during different time slots of the day.

## Key Insights
- **Supply-Demand Gap**: A significant supply-demand gap exists, especially at the Airport during peak hours, as indicated by a high percentage of "No Cars Available" statuses.
- **Peak Request Times**: The highest number of trip requests occurs during the evening and morning time slots.
- **Daywise Trends**: Wednesdays, Fridays, and Mondays are the busiest days, with the highest number of trip requests.

## How to Run this Code
1. Clone this repository:
    ```bash
    git clone https://github.com/your-username/uber-data-analysis.git
    ```
2. Navigate to the project directory:
    ```bash
    cd uber-data-analysis
    ```
3. Install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```
4. Run the Jupyter notebook or Python script to perform the analysis.

## Conclusion
This analysis highlights critical areas where Uber could improve its service, particularly in balancing the supply-demand equation during peak hours and in specific locations like the Airport.

