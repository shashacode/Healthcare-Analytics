# Healthcare Analytics
## by (Flora Oladipupo)

## Investigation Overview

The aim of this analysis is to determine the factors behind the Length of stay of patients in hospital 

## Dataset Overview

The Dataset can  be downloaded from Kaggle: https://www.kaggle.com/datasets/anmolkumar/janatahack-healthcare-analytics-part-2?select=train.csv

| Column | Description |
| --- | --- |
| case_id | Case_ID registered in Hospital |
| Hospital_code| Unique code for the Hospital |
| Hospital_type_code|Unique code for the type of Hospital |
| City_Code_Hospital|Code of the Hospital |
| Hospital_region_code|Region Code of the Hospital |
| Available Extra Rooms in Hospital|Number of Extra rooms available in the Hospital |
| Department|Department overlooking the case|
|Ward_Type|Code for the Ward type|
| Ward_Facility_Code|Code for the Ward Facility|
| Bed Grade|Condition of Bed in the Ward|
| patientid|Unique Patient Id|
| City_Code_Patient|City Code for the patient|
| Type of Admission|Admission Type registered by the Hospital|
| Severity of Illness|Severity of the illness recorded at the time of admission|
| Visitors with Patient|Number of Visitors with the patient|
| Age|Age of the patient|
| Admission_Deposit|Deposit at the Admission Time|
| Stay|Stay Days by the patient|


## Summary
After the data was downloaded from Kaggle it was loaded into this notebook it had 318438 rows and, 18 columns. It was then wrangled the first wrangling step was to check for the data tidiness luckily it had good structure so the was nothing to be done. Next the data was checked for dirtiness this also was almost none as it was just a small percentage of the data set (from two columns) that was missing these rows were dropped. 

The data was then visualized in three forms Univariate, Bivariate and Multi variate forms.

They all gave further insight to the data
Countplot, Barchart, Violin plot, Scatter plot, heatmap were all used to visualize.

*Questions explored with the Insights gotten from the Univariate visualization*

**Pattern associated with Length of stay**

The count of days stayed shows that the days people stayed the most was 21-30 days while the lowest number was 61-70 and 91-100 days

**Most popular Admission made by patients**
The highest type of admission is Trauma and the lowest urgent

**The severity of illness**
The highest severity of illness is Moderate while Extreme is the least

**Age range of patients**
Patients between age ranges 31-40 and 41-50 are the most in the hospital while 91-100 are the least

**Admission deposit**
The distribution is skewed to the right and is between 4000 and 6000

**Departments in the Hospital**
The gynecology department is the department where patients go to the most while Surgery is the least

**Extra rooms available**
The 2,3,4 rooms have the highest number of extra rooms in the hospital

### Conclusions on the univariate

The Stay column is ordinal and within an interval so it had to be transformwd into a categorical format to give it more context. The LOS of 21-30 days is the most common days people spend in the Hospital
Most of the other features were also in an ordinal format and had to be placed in category from the hoghest to the lowest format to make it more understandable whic includes Type of admission, Severity of illness and other ordinal data. The most number of age range is the 31-40 and 41-50 age range.

*Questions explored with the Insights gotten from the Bivariate visualization*

**Does severity of illness has to do with length of stay?**
The patients who stayed longer than 100 days had moderate illness followed by an extreme illness. Since it can be seen that almost all other LOS from 41-50 days and below has moderate illness followed by minor but from longer LOS 51-60 and above the chart shows they have more extreme cases than minor cases. Then severity of illness has an impact on the duration of LOS.

**Does type of Admission affect the LOS**
Admission for Trauma is the most common for the LOS and holds the highest number for LOS of more than 100 days

**Age with most severity of illness**
The commonn severity of illness across all age range is Moderate and at some particular age the minor surpasses the Extereme and vice versa. Age 0-10 has more minor cases than extreme while 91-100 has more extreme cases than minor though they are a small amount of Patient.

**Top 10 patients against thier age**
The 10 patients who visited the hospital most were from the age range of 11-20, 31-40, 41-50, 51-60, 61-70

**Age range by the department in the hospital**
The Gynecology department is the most visited and includes mostly patient from the age range 31-40 and 41-50 the least visited is surgery department.

### Conclusions on the Bivariate

In relation to the length of Stay from the visualization of stay with the severity of illness it has seen that the more severe the illness the longer the length of stay.
The age and department had an interesting correlation. Since women are mostly the visitors of Gyneacologist then it implies that the patients are women between the age of 31-40 and 41-50.

*Questions explored with the Insights gotten from the Multivariate visualization*

**Correlation between all the numerical variables in the dataset**
The strongest correlation betweent the variables is 0.3 and the lowest is 0.0 the is betweenn Visitors with patients and Extra rooms

**Relationship between age of patients, visitors and extra rooms**
The younger age group 0-10, 11-20 had fewer number of visitors but had high number of extra rooms while the older patients up to 91-100 had higher number of visitors and lowe extra rooms

**Relationship between Stay of patients, visitors and extra rooms**
Patients with longer stay had lot of visitors but little extra rooms while those who had fewer LOS had not so much visitor with plenty extra rooms

### Conclusions on the Multivariate
Adding the age and stay feature to the extar room and visitor plot gave more insight to the original chart. It was seen that the younger age group 0-10, 11-20 had fewer number of visitors but had high number of extra rooms while the older patients up to 91-100 had higher number of visitors and lowe extra rooms. Also, Patients with longer stay from 91-100 days and more had lot of visitors but little extra rooms while those who had fewer LOS had not so much visitor with plenty extra rooms.

It can be seen that the Longer the length of stay of a patient the less extra room that will be available.
