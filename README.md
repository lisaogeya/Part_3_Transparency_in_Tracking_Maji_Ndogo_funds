# Tracking Maji Ndogo Funds
![](transparency_tracking.webp)

## Introduction

This Power BI project aims to analyze and visualize the budgets allocated to various water sources across the fictional state of Maji Ndogo. Using advanced DAX calculations and interactive visualizations, the project provides detailed insights into which water sources in different provinces require urgent repairs, the budgets necessary to address these issues, and the most efficient allocation of available funds. In addition to infrastructure fixes, the project also includes budget analysis for the engineering teams responsible for maintenance and repairs, tracking the longevity and condition of the infrastructure. 
By identifying urgent needs and ensuring transparent fund management, this project helps guide effective decision-making for sustainable water management in Maji Ndogo.

**_Disclaimer_**: All datasets and reports do not represent any company, institutions or country but just a fictional dataset to demonstrate the capabilities of power BI

## Problem Statement
- What is the total estimated budget required to address water infrastructure challenges across all provinces and towns in Maji Ndogo?
- Which provinces have the highest priority for improvements?
- How can we ensure transparency in tracking the allocation and utilization of funds for water infrastructure improvements?
- What is the budget distribution between rural and urban areas and is the allocation sufficient to address disparities in access to water?
- How can we minimize costs in water infrastructure projects without compromising quality or access?
- What are the long-term financial implications of the current infrastructure improvements, and how can its sustainability be ensured?
- How will budget constraints or surpluses impact the timeline for project completion, and what contingencies can be made for fluctuating costs?

## Power BI concepts demonstrated
- Modelling
- Drill-throughs
- Filters
- Tooltips
- Slicers
- Measures
- Bookmarks
- DAX calculations
  
## Data Sourcing

Downloaded the csv files from ALX Explore AI Course and extracted it into power bi for cleaning, analysis and visualization.
Data used in this project:

[Md_water_services_data.xlsx](https://github.com/lisaogeya/Visualizing_the_currents_of_change_in_Maji_Ndogo/blob/main/Md_water_services_data.xlsx)

## Data Modelling and Data Transformation

Auto model                                |                    Adjusted model
:----------------------------------------:| :----------------------------------------:        
![](tracking_funds_auto_model.png)        |      ![](tracking_funds_adjusted_model.png)


- In the locations table. None of the column names (or headers) were imported correctly. So we changed that to enable relationships be established.
  
- In the queue_composition table, removing the first column establishes the relationships.
- In the water_source_related_crimes table, removing the first column to connect the table to the rest of the model.
- Linked water_source_related_crime table to location table using location_id .
- Created a 1-to-many relationship between infrastructure_cost table and project_progress table.
- In this model:
   - There are 4 dimension tables to the visits fact table.
   - Project_progress and water_source_related_crimes are fact tables on their on.
- Thus the model is a multi-star schema.


## Data Analysis and Visualizations
