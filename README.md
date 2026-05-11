# telehealth-

## project overview
Explain:

what the project does
what problem it solves


## problem statement
Doctor on Mobile is a telehealth pilot program launched by BetaHealth Clinic to provide remote medical consultations. The program aims to improve access to healthcare while reducing patient wait times and increasing convenience.

Before expanding the program, healthcare administrators need to evaluate whether it delivers a positive patient experience and identify the key factors influencing patient satisfaction during virtual visits.

Understanding these factors helps administrators determine whether the telehealth service meets patient expectations and whether the pilot should be scaled. If issues affecting satisfaction are not addressed, patients may be less likely to recommend or continue using the service, which could limit adoption and reduce the potential benefits of telehealth.

Using telehealth visit data, this analysis explores how operational factors, technological conditions, and visit characteristics influence patient satisfaction, helping administrators make data-driven decisions about improving and scaling the program.


## dataset


## tools used


## project workflow
1. data cleaning
2. data transformation



### data cleaning
- **Duplicates**
    - Checked for duplicate records and confirmed true duplicates.
    - Removed duplicates, reducing the dataset from 5,100 to 5,000 rows.
- **Missing Values**
    - Identified 2,272 missing entries using `COUNTBLANK`.
    - Imputed numerical columns (e.g., `age`) with the mean.
    - Filled categorical columns (e.g., `state`) with the mode.
    - Verified that no missing values remained after cleaning.
- **Text and Categorical Data**
    - Standardize text by converting to lowercase for consistency.
    - Removed extra spaces using `TRIM`.
    - Checked unique values to correct inconsistent categories.
- **Dates**
    - Converted date columns to the correct datetime format.
    - Standardized date representation across the dataset.
- **Data Types**
    - Ensured all columns have the correct datatype (numerical, categorical, or datetime).
- **Verification**
    - Inspected each column individually to confirm correctness and consistency.


 ### data transformation
To make the dataset easier to analyze, continuous numerical variables were grouped into categories using Excel IF formulas. The transformed variables included Age, Wait Time, and Visit Duration.

Age was grouped into ranges such as 18–24, 25–34, 35–44, and above.
Wait Time was grouped into categories such as 0–10 minutes, 11–30 minutes, 31–60 minutes, and above.
Visit Duration was grouped into intervals such as 2–10 minutes, 11–20 minutes, 21–30 minutes, and above.

Excel IF formulas were used to automatically assign each record to its appropriate category based on the original numerical value.

These transformations helped simplify the dataset, improve analysis, and make patterns easier to identify during visualization

 
 


