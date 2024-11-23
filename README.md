# diabetes_analysis
Analysis of CDC BRFSS survey data on diabetes

This analysis is aided by use for Claude 3 Sonnet LLM running on Cursor IDE.


Hey Claude 3 Sonnet,

I want to create a project to analyse CDC BRFSS Diabetes data. First I'll give you the essential information. Then I'll explain what I would like you to do; see "What I want you to do".

Language: Python
Data: "https://www.cdc.gov/brfss/annual_data/2022/files/LLCP2022XPT.zip".
Notes on the data:
    1. The .xpt file in the zip file above has a trailing space in the file extension. You'll need to handle this.
    2. SAS formats: https://www.cdc.gov/brfss/annual_data/2022/files/FORMAT22.sas
    3. Data dictionary: https://raw.githubusercontent.com/timur-hassan/diabetes_analysis/refs/heads/main/data_dictionary.txt

Target variable for modelling: DIABETE4
Date columns to convert to datetime format.
Models to run: XGBoost
Predictors: I want you to select the predictors by referring to the data dictionary linked above.

## What I want you to do
Create a set of python scripts, with filenames starting with two integers, incrementing the number with each subsequent file.
1. Create a Python script to create a folder in ~/Documents/sandpit/py called "diabetes_bot". This folder will be the working directory for this project.
2. In this subfolder, create a python virtual environment called env_diab.
3. In this subfolder, create subfolders called: in, out, doc, rpt.
4. If the data doesn't exist in the "in" subfolder, download the data, unzip it, remove the trailing space character in the file extension, remove the .zip file.
5. Read in the data file.
6. Referring to the SAS formats, create a format class.
