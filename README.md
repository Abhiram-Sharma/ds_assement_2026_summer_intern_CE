# Motorq Data Science Assignment 2025 - EDA and Data Parsing

This repository contains the results of an exploratory data analysis (EDA) and data parsing project on a dataset provided by Motorq. The goal of this project was to understand the provided data, clean it, and prepare it for further analysis.

## Project Overview

The project involved the following steps:

1.  **Data Conversion:** The initial dataset included data in JSON format, which was converted to CSV for easier handling and analysis.
2.  **Data Exploration:** An initial exploration of the different data files was conducted to understand their structure and contents.
3.  **Data Cleaning:** The data was cleaned to address issues such as missing values and duplicate entries.
4.  **Data Merging and Transformation:** The different data sources were merged and transformed to create a unified dataset.
5.  **Exploratory Data Analysis:** A deeper analysis of the cleaned and merged data was performed to uncover insights and potentially identify patterns in battery consumption during Candidate Events.

## Dataset Description

The dataset consists of the following files:

*   `telemetry_data.csv`: High-rate telematics data from vehicles.
*   `triggers_soc.csv`: Low-rate trigger data from vehicles.
*   `vehicle_pnid_mapping.csv`: Mapping between vehicle IDs and PNIDs.
*   `artificial_ign_off_data.csv`: Synthetic data for ignition off events.
*   `events.csv`: Vehicle ignition events.
*   `Battery_Data.csv`: Data related to vehicle battery performance. Due to the large file size, the contents of this file were not fully explored.
*   `Assumptions and plan.txt`: A text file outlining the initial plan and assumptions for the project.

### Data Columns

The main data files contain the following columns:

*   **Telematics (TLM):**
    *   `ID`
    *   `VEHICLE_ID`: String
    *   `TIMESTAMP`: datetime (dd-mm-yy hh:mm:ss)
    *   `SPEED`
    *   `IGNITION_STATUS`
    *   `EV_BATTERY_LEVEL`: float
    *   `ODOMETER`
*   **Triggers (TRG):**
    *   `CTS`: datetime (dd-mm-yy hh:mm:ss)
    *   `PNID`: String
    *   `NAME`: String
    *   `VAL`: String
*   **Mapping (MAP):**
    *   `ID`: String
    *   `IDS`: Array of Strings
*   **Synthetic (SYN):**
    *   `Vehicle ID`
    *   `Timestamp`
    *   `type`

## Key Findings and Insights

The analysis of the data revealed the following key insights:

*   The dataset contains information for 19 vehicles.
*   The telematics data spans from September 1, 2021, to January 30, 2022, and contains over 1 million data points.
*   The trigger data is categorized into `Charge_State`, `EV_Charge_State`, and `Ignition_Cycle`.
*   There are 410 synthetic ignition off events in the dataset.
*   A significant number of PNIDs (39,262) in the trigger data are not mapped to any vehicle ID.
*   After cleaning and merging, the trigger data contains 9,935 records, spanning from September 1, 2021, to January 31, 2022.

## Challenges and Issues

The following challenges and issues were encountered during the project:

*   **Timestamp Conversion:** 93 timestamps in the telematics data contained microseconds, which caused issues during the conversion to datetime objects.
*   **Incomplete Mapping:** 6 vehicles in the dataset are not mapped to any PNID, which means they lack trigger data.
*   **Timezone Mismatch:** A timezone mismatch (IST vs. UTC) was identified between the trigger and telematics data.

## Future Work

The following are potential next steps for this project:

*   **Resolve Data Issues:** Develop a Pipeline to store data in the lake to Address the timestamp conversion issues, incomplete mapping, and timezone mismatch.
*   **In-depth Battery Analysis:** Conduct a more in-depth analysis of the rate at which the charge dropsafter each eactivity or trigger to understand battery performance and degradation of each vehicle.
*   **Predictive Modeling:** Develop predictive models to forecast usage and degradation of battery. optimum time for maintainance.
*   **API Integration:** The final processed data can be converted back to JSON format for integration with APIs.
*   **Customer Centric Dashboard:** Integration of all the derived data into an interactive and informative professional dashboard developed with **Customer Centric KPIs** for providing a customised real time tracking experience comprising all use cases in addition to the insights from these data as mentioned above.
