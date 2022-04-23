# MLP2 
The purpose of this machine learning project is to perform preprocessing and exploratory analysis on the two datasets defined in MLP1.

## File Structure
1. /rawdata - holds the raw data obtained from Kaggle
2. /input - holds the cleaned data 
3. /analysis - holds all of the files related to performing exploratory data analysis. Note that these files use the data from the input directory.
4. data_preprocessing.ipynb - a Jupyter notebook used to preprocess (clean) the data

## Datasets
### heart_2020_cleaned.csv
This dataset contains data about the key indicators of heart disease. It contains more "qualitative" data compared to the other dataset. By this, we mean that this dataset uses engineered features known to have a high correlation to heart disease. This will be explained more in the attributes section. This dataset contains 18 separate columns and 319795 rows.
#### Attributes - Raw
Note that for this dataset, boolean types are defined as features containing either yes or no. 
1. HeartDisease - A boolean type signifying if the person had heart disease.
2. BMI - A decimal type listing the person's body mass index (BMI), the person's weight divided by the square of their height.
3. Smoking - A boolean type signifying if the person has smoked at least 100 cigarettes in their life.
4. AlcoholDrinking - A boolean type indicating if the person is a heavy drinker (more than 14 drinks per week for men and more than 7 drinks per week for women).
5. Stroke - A boolean type indicating if the person had a stroke before.
6. PhysicalHealth - A decimal type indicating how many days within the past 30 days a person was ill or injured (cold, broken bones, etc).
7. MentalHealth - A decimal type indicating how many days within the past 30 days a person's mental health was defined as "not good".
8. DiffWalking - A boolean type indiciating if a person has difficulty walking.
9. Sex - A binary string type (Male/Female) denoting the participant's sex.
10. AgeCategory - A 14-category string type (<= 17, 18-24, 25-29, 30-34, 35-39, 40-44, 45-49, 50-54, 55-59, 60-64, 65-69, 70-74, 75-79, 80+) denoting the participant's age group.
11. Race - A 6-category string type (White, Black, Asian, American Indian/Alaskan Native, Other, Hispanic) denoting the participant's race.
Todo: brief description of each attribute (what the attribute is about and its data type).
12. Diabetic - A 3-category string type denoting what stage of diabetes a person has (No = No Diabetes, "No, borderline diabetes" = Prediabetes, Yes=Diabetes).
13. PhysicalActivity - A boolean type denoting if the patient has done physicial activity or exercise withiin the past 30 days.
14. GenHealth - A 6-category string (poor, fair, good, very good, excellent) denoting how well the person thinks of their health.
15. SleepTime - A decimal type denoting the average amount of time (in hours) the participants sleeps.
16. Asthma - A boolean type denoting if the person has asthma.
17. KidneyDisease - A boolean type denoting if the person has kidney disease.
18. SkinCancer - A boolean type denoting if the persoon has skin cancer.
#### Attributes - After preprocessing 
Note that for this dataset, boolean types are defined as features containing either yes or no. 
18. SkinCancer - A boolean type denoting if the persoon has skin cancer.
1. HeartDisease - A boolean type signifying if the person had heart disease.
2. BMI - A decimal type listing the person's body mass index (BMI), the person's weight divided by the square of their height.
3. Smoking - A boolean type signifying if the person has smoked at least 100 cigarettes in their life.
4. AlcoholDrinking - A boolean type indicating if the person is a heavy drinker (more than 14 drinks per week for men and more than 7 drinks per week for women).
5. Stroke - A boolean type indicating if the person had a stroke before.
6. PhysicalHealth - A decimal type indicating how many days within the past 30 days a person was ill or injured (cold, broken bones, etc).
7. MentalHealth - A decimal type indicating how many days within the past 30 days a person's mental health was defined as "not good".
8. DiffWalking - A boolean type indiciating if a person has difficulty walking.
9. Sex - A binary string type (Male/Female) denoting the participant's sex.
10. AgeCategory - A 14-category string type (<= 17, 18-24, 25-29, 30-34, 35-39, 40-44, 45-49, 50-54, 55-59, 60-64, 65-69, 70-74, 75-79, 80+) denoting the participant's age group.
11. PhysicalActivity - A boolean type denoting if the patient has done physicial activity or exercise withiin the past 30 days.
12. GenHealth - A 6-category string (poor, fair, good, very good, excellent) denoting how well the person thinks of their health.
13. SleepTime - A decimal type denoting the average amount of time (in hours) the participants sleeps.
14. Asthma - A boolean type denoting if the person has asthma.
15. KidneyDisease - A boolean type denoting if the person has kidney disease.
16. SkinCancer - A boolean type denoting if the persoon has skin cancer.
17. American Indian/Alaskan Native - A boolean type denoting if a person is american indian/alaskan native.
28. Asian - A boolean type denoting if a person is asian.
19. Black - A boolean type denoting if a person is black.
20. Hispanic - A boolean type denoting if a person is hispanic.
21. Other - A boolean type denoting if a person is other.
22. White - A boolean type denoting if a person is white.
23. No diabetes - A boolean type denoting if a person does not have diabetes.
24. Borderline diabetes - A boolean type denoting a person has prediabetes.
25. Has diabetes - A boolean type denoting a person has diabetes.
26. Yes (during pregnancy) - A boolean type denoting a person has diabetes but only during pregnancy.
### heart_disease_uci.csv
This dataset contains data about predicting heart disease. Unlike the above dataset, this contains more medically-sound metrics that were measured. For example, instead of looking at the degre someone smoked (2020 dataset), this dataset contains features like resting blood pressure. This dataset contains 16 columns and 920 rows.
#### Attributes - Raw
Note that boolean types in this dataset are defined to be either TRUE or FALSE.
1. id - An integer type denoting the row number.
2. age - An integer type denoting the person's age.
3. sex - A binary string type type denoting the person's sex.
4. dataset - A 4-category string ('Cleveland' 'Hungary' 'Switzerland' 'VA Long Beach') denoting where the data was collected.
5. cp - A n-category string ('typical angina' 'asymptomatic' 'non-anginal' 'atypical angina') denoting the type of chest pain a person has.
6. trestbps - An integer type denoting the person's resting blood pressure.
7. choi - An integer type denoting the person's cholestrol levels.
8. fbs - A boolean type denoting if the person's fasting blood sugar was greater than 120 mg/dl.
10. restecg - A 3-category string type (normal, stt abnormality, lv hypertrophy) denoting the person's resting ecg results.
11. thalach - An integer value denoting the maximum heart rate achieved by the participant.
12. exang - A boolean type denoting if the participant has exercise induced angina.
13. oldpeak - A decimal type denoting the amount of ST depression induced by exercise.
14. slop - A 4-category string ('downsloping' 'flat' 'upsloping' nan) denoting the slope of the ST segment.
15. ca - An integer type (0 - 3) denoting the number of major vessels colored by flourosopy. 
16. thal - A 3-category string type (normal; fixed defect; reversible defect) denoting the degree of Thalassemia a person has.
17. num - An integer value (0 - 4) denoting the stage of heart disease a person has (0 - no heart disease, 4 - stage 4 heart disease).

#### Attributes - After preprocessing
Note that boolean types in this dataset are defined to be either TRUE or FALSE.
1. id - An integer type denoting the row number.
2. age - An integer type denoting the person's age.
3. sex - A binary string type type denoting the person's sex.
4. trestbps - An integer type denoting the person's resting blood pressure.
5. choi - An integer type denoting the person's cholestrol levels.
6. fbs - A boolean type denoting if the person's fasting blood sugar was greater than 120 mg/dl.
7. thalach - An integer value denoting the maximum heart rate achieved by the participant.
8. exang - A boolean type denoting if the participant has exercise induced angina.
9. oldpeak - A decimal type denoting the amount of ST depression induced by exercise.
10. ca - An integer type (0 - 3) denoting the number of major vessels colored by flourosopy. 
11. num - An integer value (0 - 4) denoting the stage of heart disease a person has (0 - no heart disease, 4 - stage 4 heart disease).
12. location_Cleveland - A boolean type denoting if the data was obtained from Cleveland.
13. location_Hungary - A boolean type denoting if the data was obtained from Hungary. 
14. location_Switzerland - A boolean type denoting if the data was obtained from Switzerland.
15. location_VA Long Beach - A boolean type denoting if the data was obtained from VA Long Beach.
16. cp_asymptomatic - A boolean type denoting if a person does not have chest pain.
17. cp_atypical angina - A boolean type denoting if a person has atypical-anginal chest pain.
18. cp_non-anginal - A boolean type denoting if a person has non-anginal chest pain.
19. cp_typical angina - A boolean type denoting if a person has typical anginal chest pain.
20. restecg_Unknown - A boolean type denoting if a person's restecg result was unknown.
21. restecg_lv hypertrophy - A boolean type denoting if a person's restecg result was lv hypertrophy.
22. restecg_normal - A boolean type denoting if a person's restecg result was normal.
23. restecg_st-t abnormality - A boolean type denoting if a person's restecg result was st-t abnormality.
24. slope_Unknown - A boolean type denoting if the slope of the ST segment was unknown.
25. slope_downsloping - A boolean type denoting if the slope of the ST segment was downsloping.
26. slope_flat - A boolean type denoting if the slope of the ST segment was flat.
27. slope_upsloping - A boolean type denoting if the slope of the ST segment was upsloping.
28. thal_Unknown - A boolean type denoting if the degree of Thalassemia was unknown.
29. thal_fixed defect - A boolean type denoting if the degree of Thalassemia was a fixed defect.
30. thal_normal - A boolean type denoting if the degree of Thalassemia was normal.
31. thal_reversable defect - A boolean type denoting if the degree of Thalassemia was a reversable defect.
32. FBS_False - A boolean type denoting if the fasting blood sugar was not above 120 mg/dl.
33. FBS_True - A boolean type denoting if the fasting blood sugar was above 120 mg/dl.
34. FBS_Unknown - A boolean type denoting if the fasting blood sugar was unknown.
35. exang_False - A boolean type denoting if the participant does not have exercise induced angina.
36. exang_True - A boolean type denoting if the participant has exercise induced angina.
37. exang_Unknown - A boolean type denoting their exang status is unknown.