# Google Analytics Capstone Project: Workplace Wellness Analysis
This repository contains code written in January 2022, which was used to analyze the CDC Workplace Health in America Survey, 2017, published December 2018. Link to the original data, codebook and survey instrument are included below.

I conducted this analysis as part of the requirements for the Google Data Analytics Certifcate.

## Overview
In this case study, I used nationally representative survey data to examine workplace stress management programs, employee participation in such programs, and barriers faced in implementing successful programs. I then offer an action plan based on those findings.

## Introduction
The client is a fictional privately owned tech company based in Seattle, WA, with 50 employees. They are a relatively young company, but growing quickly, and a big part of their success is their top-notch workforce. As a start up, the environment is very fast-paced, and can often be stressful, so they want to make sure they are doing all they can to retain their best employees. One thing they are considering is the creation of a comprehensive stress management program for their employees. The co-founders have asked me to look at workplace wellness programs in general, and stress management programs in particular, in order to identify best practices for creating a Culture of Health for their company. They also want to understand any barriers they might face in supporting such programs.

### Key Questions
    • What percentage of for-profit companies offer stress management programs?
    • What types of stress management programming do they offer?
    • What percentage of employees participate in wellness initiatives? 
    • What have been the barriers to offering workplaces wellness programs?
    • How is the presence of stress management programs related to employee turnover?

## Data Background

This analysis utilizes data from the [*CDC Workplace Health in America Survey, 2017*](https://www.cdc.gov/workplacehealthpromotion/survey/data.html), published December 2018
. This ASCII delimited file contains data from a 2017 national survey conducted by the Centers for Disease Control on workplace wellness initiatives across an array of industries and organizational types. Please see the [codebook](https://www.cdc.gov/workplacehealthpromotion/data-surveillance/docs/2017-WHA-Datafile-Codebook-508.pdf) and [survey instrument](https://www.cdc.gov/workplacehealthpromotion/data-surveillance/docs/2017-WHA-Survey-Instrument-508.pdf) for variable coding and descriptions.

## Data Cleaning

I imported the data, which was in an ASCII delimited format, into Google Sheets, then converted it to a comma delimited format. I then ran summary statistics to make sure the data were in the ranges they were supposed to be, comparing them against the data provided by the Centers for Disease Control and Prevention (CDC) in their Workplace Health Promotion [Codebook](https://www.cdc.gov/workplacehealthpromotion/data-surveillance/docs/2017-WHA-Datafile-Codebook-508.pdf). 

The data is in a format that was designed for ease of use for those using SAS for data analysis. Therefore, I had a lot of formatting to do to get it to a place where it was easier to interact with. I replaced the miscellaneous values coded as 95, 96, 97, 98, and 99 to missing values, since they legitimately should be ignored. I then converted the Percentage Question integer variables (e.g., "What percentage of employees work remotely?") into percentages. Here is [the cleaned data set](https://github.com/maryhakearns/Workplace_Wellness_Study/blob/fc1930afc9433eb7cced633b916f654ddaccac54/WHA_2017.csv).

Because the formatting process was quite extensive, I have placed it in a separate [Rmd file](https://github.com/maryhakearns/Workplace_Wellness_Study/blob/1f3fade34c4a256d0256fd79a16302ae6929d3e5/Workplace_Wellness_Data_Cleaning_Code.Rmd) to reduce the amount of clutter in this report. That code produces a clean subset of the data with column names, labels, and correct variable types. I ran tables and a summary of the dataframe to check for missing values, etc. I then saved a csv fiile of the cleaned, labelled data.

## Data Analysis

Using the cleaned, labelled, subset dataset created using the [Data Cleaning Code](https://github.com/maryhakearns/Workplace_Wellness_Study/blob/1f3fade34c4a256d0256fd79a16302ae6929d3e5/Workplace_Wellness_Data_Cleaning_Code.Rmd), I imported it into Google Sheets, and created pivot tables and charts to visualize the data realted to the Key Questions (above).
