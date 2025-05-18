# IT Asset Inventory: Exploratory Data Analysis

## Project Overview

The aim of this project is to investigate a simulated IT asset inventory data from an organisation. The fields reflect a realistic IT inventory attributes at an organisation starting from 2020. To avoid security risks, the records present in the dataset are fictional and were generated using an LLM. Additionally, the LLM was not provided with any sensitive information for the dataset generation. 

The goal of the analysis is to uncover patterns in asset costs (particularly based on departments and types of asset), usage duration, and e-waste, and provide actionable insights for improving the asset management strategies. 

The IT asset management system is based on the following procedure:
- Procurement staff member requests IT department to source an asset with specified details including the assigned staff member details.
- The asset request is approved and an asset sticker (with a unique identifier) is assigned to the asset after it is sourced.
- The asset is then delivered to the department and/or assigned staff member.
- When an asset fails or finished its lifecycle, it can be requested to be e-wasted (retired).

## Dataset Overview

- **Records**: 2,000 assets
- **Key Columns**:
  - Asset Type
  - Date Ordered
  - Date Assigned
  - Date Returned
  - Department
  - Cost
  - e-Wasted
- Simulated dataset reflecting realistic IT inventory attributes at an organisation.

## Tech Stack
- **Language**: Python  
- **Libraries**: pandas, seaborn, matplotlib  
- **Tools**: Jupyter Notebook

## Data Cleaning Highlights
- Removed duplicates asset entries to ensure data integrity.
- Removed columns not relevant to the analysis.
- Parsed and corrected inconsistent date formats.
- Derived columns for analysis and visualisation.
- Performed standardization for string columns by removing whitespaces and standardizing the text.
- Performed validity checks, such as ensuring that the date assigned and date returned are logical for all records.

## Key Insights
- **Right-skewed asset cost distribution**, with most assets under `$2500` and a few reaching `$10,000`.
- `Social Work` has the highest overall asset spend and with `DOVS` being the lowest (Difference of almost `$145,000`).
- `Laptops` were the most frequently e-wasted with `Printers` being the least. The proportional gap between the two categories is `5%` of all e-wasted assets.
- E-waste rates greatly increased by `2023` but observed a dramatic decline after mid of `2023`.
- There is a strong correlation between the cost of the asset and the lifespan, indicating that cheaper assets tend to have shorter lifecycles.

