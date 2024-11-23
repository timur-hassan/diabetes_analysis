# diabetes_analysis
Analysis of CDC BRFSS survey data on diabetes

This analysis is aided by use for Claude 3 Sonnet LLM running on Cursor IDE.


Hey Claude 3 Sonnet,

I want to create a project to analyse CDC BRFSS Diabetes data. First I'll give you the essential information. Then I'll explain what I would like you to do; see "What I want you to do".

## Specification
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
Create a Python script that achieves the following:

1. Create a folder in ~/Documents/sandpit/py called "diabetes_bot". This folder will be the working directory for this project. If the folder already exists, delete it. Don't write code to check if this or any subsequent subfolder already exists.
3. In this folder, create a python virtual environment called env_diab.
4. In this folder, create subfolders called: in, out, doc, rpt.
5. If the data doesn't exist in the "in" subfolder, download the data, unzip it, remove the trailing space character in the file extension, remove the .zip file.
6. Read in the data file then save it as pickle.
7. Referring to the SAS formats (see github link under the "Specification" heading), create a format class and save it as a permanent file.
8. Store the format class as a file on disk.
