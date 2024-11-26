## Specification

Language: Python

Data: "https://www.cdc.gov/brfss/annual_data/2022/files/LLCP2022XPT.zip".

SAS formats: https://www.cdc.gov/brfss/annual_data/2022/files/FORMAT22.sas

Data dictionary: https://raw.githubusercontent.com/timur-hassan/diabetes_analysis/refs/heads/main/data_dictionary.txt

Target variable for modelling: DIABETE4

Models to run: XGBoost

Python Virtual Environment name: venv_diab


## What I want you to do
Create a Python script that achieves the following:

1. Create a folder in ~/Documents/sandpit/py called "diabetes_bot". This folder will be the working directory for this project. If the folder already exists, delete it.
2. In this folder, create a python virtual environment.
3. In this folder, create subfolders called: in, out, doc, rpt.
4. Set working directory to ~/Documents/sandpit/py/diabetes
5. Check ~/Documents/sandpit/py/downloads for LLCP2022.XPT, if it's there copy it to ~/Documents/sandpit/py/diabetes_bot/in. Otherwise download it to ~/Documents/sandpit/py/download, unzip it, remove the trailing space character from the file extension, delete the original zip file. Show download progress bar.
6. Read in the data file to a dataframe called df. This dataframe should be stored in the workspace namespace so that once I've run the script you produce, I can continue to query the dataframe.
7. The IDATE column has invalid values like this: b'07002022'. It is otherwise in mmddyyyy form surrounded by single quotes and lead by a "b". Fix the invalid valid values then convert it to datetime.
9. Referring to the SAS formats (see github link under the "Specification" heading), create a format class and save it as a permanent file.
10. Store the format class as a file on disk.
