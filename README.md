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



## 1.data cleaning
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


 ## 2.data transformation
To make the dataset easier to analyze, continuous numerical variables were grouped into categories using Excel IF formulas. The transformed variables included Age, Wait Time, and Visit Duration.

Age was grouped into ranges such as 18–24, 25–34, 35–44, and above.
Wait Time was grouped into categories such as 0–10 minutes, 11–30 minutes, 31–60 minutes, and above.
Visit Duration was grouped into intervals such as 2–10 minutes, 11–20 minutes, 21–30 minutes, and above.

Excel IF formulas were used to automatically assign each record to its appropriate category based on the original numerical value.

These transformations helped simplify the dataset, improve analysis, and make patterns easier to identify during visualization





## spotting patterns and relationships

### 1. The "Threshold of Frustration" (Wait Times)

- **The Pattern:** There is a "safe zone" under 20 minutes where almost all 4 and 5-star ratings live. Once wait times cross the 40-minute mark, the "Satisfaction 5" category disappears entirely.
- **The Relationship:** Satisfaction is not just "lower" with long waits; it becomes **capped**. No matter how good the doctor is, a long wait creates a "satisfaction ceiling" that the provider cannot break through.

### 2. The "Quality Compensation" Effect (Tech vs. Score)

One of the most surprising patterns is the **flat line** in the box plots for Technical Issues and Internet Quality.

- **The Pattern:** The median satisfaction for "Poor" internet is nearly identical to "Good" internet.
- **The Relationship:** This suggests a **compensatory relationship**. Patients likely view technical glitches as a "platform flaw" rather than a "provider flaw." If the medical advice is sound, they are willing to overlook a frozen screen or a dropped call, provided the value of the consultation remains high.

### 3. The "Outcome over Output" Rule (Duration)

The scatter plot for Visit Duration shows a **random distribution** (the "vertical cloud").

- **The Pattern:** You have 5-star ratings for 5-minute visits and 1-star ratings for 40-minute visits.
- **The Relationship:** There is **no correlation** between time spent and perceived value. In telehealth, "more" is not "better." This confirms that patients are seeking **efficiency**. A long visit might actually indicate a frustrating technical struggle or a complex issue, whereas a quick, decisive visit fulfills the "mobile" promise of the brand.

### 4. Modality & Specialty Neutrality

The bar charts for Visit Type and Provider Specialty show **uniformity**.

- **The Pattern:** The bars are almost perfectly level (around 3.2).
- **The Relationship:** This indicates **service consistency**. The "Doctor on Mobile" experience is stable regardless of whether the patient is seeing a Pediatrician or a Dermatologist, or whether they are typing or talking. This is a "green light" for scaling because it proves the model isn't dependent on one specific niche to succeed.

---

## Summarize and communicate  your results  and turn them into business insights

### **1. The "Speed over Stability" Paradox**

**Insight:** Patients are surprisingly forgiving of technical glitches and poor internet quality, but they are highly intolerant of long wait times.
**Strategic Action:** BetaHealth should prioritize **queue management and provider punctuality** over expensive infrastructure upgrades. The "convenience" of telehealth is measured by the patient in minutes saved, not pixels displayed.

### **2. Efficiency is Not "rushing."**

**Insight:** Visit duration does not dictate satisfaction. A 5-minute visit can result in a "5-star" rating just as easily as a 45-minute visit.
**Strategic Action:** Train providers on **concise, high-impact communication**. Since patients value their time, the goal should be "effective resolution" rather than "maximum time spent," allowing for higher patient throughput without sacrificing quality.

### **3. Universal Scalability**

**Insight:** The pilot performed consistently across all devices (Mobile, Laptop, Tablet) and all medical specialties.
**Strategic Action:** The program is **highly scalable**. BetaHealth can confidently expand into different medical departments and target users with varying device access (e.g., low-bandwidth chat for rural areas) without fearing a drop in service perception.

### **4. The "Golden Window" for Retention**

**Insight:** To secure a 5-star rating and ensure patient "buy-in," the wait time must stay under **15 minutes**. Beyond 30 minutes, the risk of a "detractor" score (1 or 2) increases exponentially.
**Strategic Action:** Implement an **automated alert system** for administrators when a patient has been in the digital waiting room for more than 10 minutes



 
 


