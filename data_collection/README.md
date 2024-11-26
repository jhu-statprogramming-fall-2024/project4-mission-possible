# Data Source, database schema and data dictionary

Data Source: AACT database developed by clinicaltrial.gov <https://aact.ctti-clinicaltrials.org/>

Database schema: <https://aact.ctti-clinicaltrials.org/documentation/aact_schema.png>

Data dictionary: <https://aact.ctti-clinicaltrials.org/data_dictionary>

Other useful website for AACT: [Query ClinicalTrials.gov through AACT](https://github.com/reb-greazy/easier_clinicaltrials.gov_searching/tree/master)

What is included in data_wrangling.qmd?
- Code to connect to the SQL database we used
- Summary statistics as exploratory analysis
- Code to extract the data and generate the csv file

Which type of trial is included in the csv file
- trials with a start date later than 2000.01.01
- AND conditions being studied is one of the ('Healthy', 'Breast Cancer', 'Obesity', 
                       'Stroke', 'Depression', 'Hypertension', 
                       'Pain', 'Prostate Cancer', 'Coronary Artery Disease', 
                       'Cancer')

Why three csv files?
- one trials have multiple conditions, intervention types, countries
- tried to create a S3 class object, but we have 49813 trials, my computer tried to run for 15 min to create the 49813 objects and then died (the code is still in .qmd file)
