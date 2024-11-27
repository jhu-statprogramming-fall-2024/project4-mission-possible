# Data Source, database schema and data dictionary

Data Source: AACT database developed by clinicaltrial.gov <https://aact.ctti-clinicaltrials.org/>

Database schema: <https://aact.ctti-clinicaltrials.org/documentation/aact_schema.png>

Data dictionary: <https://aact.ctti-clinicaltrials.org/data_dictionary>

Other useful website for AACT: [Query ClinicalTrials.gov through AACT](https://github.com/reb-greazy/easier_clinicaltrials.gov_searching/tree/master)

In data_extraction_cleaning.Rmd
- **Final data extraction and cleaning**
- code to connect to AACT database, filter the top 10 countires and 10 diseases
- the following filteration is used to generate the final data.csv
  - trials start_date after 2015.01.01 and before 2024.12.31
  - Top 10 most studies disease worldwide between 2015 and 2024 (exlcuing healthy, COVID-19)
    - ('Breast Cancer', 'Obesity', 'Stroke', 'Depression', 
                       'Pain', 'Anxiety', 'Cancer', 'Heart Failure', 
                       'Prostate Cancer', 'Hypertension')
  - No missing variable in Phase
  - Top 10 countires that conducted the most trials in the selected disease and between 2015 and 2024
    - ('United States', 'China', 'France', 'Canada', 
                       'United Kingdom', 'Turkey', 'Spain', 'Italy', 
                       'Germany', 'Korea, Republic of')





What is included in data_wrangling.qmd?
- **Inital data exploration and data extraction**
- Code to connect to the SQL database we used
- Summary statistics as exploratory analysis
- Code to extract the data and generate the csv file
- Which type of trial is extracted 
  - trials with a start date later than 2000.01.01
  - AND conditions being studied is one of the ('Healthy', 'Breast Cancer', 'Obesity', 
                       'Stroke', 'Depression', 'Hypertension', 
                       'Pain', 'Prostate Cancer', 'Coronary Artery Disease', 
                       'Cancer')


