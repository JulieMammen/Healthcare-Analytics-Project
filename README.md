# Healthcare-Analytics-Project
#Overview
This project involves analyzing healthcare data to gain insights into patient demographics, hospital visits, and medical conditions.

#Dataset
##The dataset used for this project includes the following tables:

#Patients- Contains patient demographic information.

#Encounters- Details about hospital visits.

#Conditions-Lists medical conditions diagnosed.

#Immunizations- Records of vaccinations administered.

##Queries
The SQL queries in this project are designed to extract and analyze various aspects of healthcare data. Here are some of the key queries:


##Patient Information
Retrieves basic patient details such as first name, last name, and birthdate.
```
SELECT first,
       last,
       birthdate
FROM PATIENTS;
'''

##Encounter Types
Identifies distinct types of hospital visits from the encounters table.
```
SELECT distinct encounterclass
FROM ENCOUNTERS;
```
##Inpatient ICU Visits in 2023
Counts the number of patients seen as inpatients in the ICU during 2023.
```
select *
from ENCOUNTERS
where encounterclass='inpatient'
 and description='ICU Admission'
 and stop>='2023-01-01 00:00'
 and stop <='2023-12-31 23:59';
 ```
##Ambulatory and Inpatient Encounters
Lists all ambulatory and inpatient encounters.

##Common Conditions
Identifies conditions that occur more than 2000 times.

##Patients from Boston
Counts the number of patients from Boston.

##CKD Diagnoses
Retrieves all patients diagnosed with Chronic Kidney Disease (CKD).

##Patient Distribution by City
Lists the number of patients from each city, excluding Boston, where the count is more than 200.

##Immunization Data
Retrieves immunization records and joins them with patient information.
