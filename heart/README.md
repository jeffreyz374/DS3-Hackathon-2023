# Heart Disease Prediction
## About the data
The ``heart_train`` and ``heart_test`` datasets contain 643 and 275 rows, respectively, where each row corresponds to a patient and each column corresponds to a medical characteristic of that patient, such as their cholesterol level. In the case of ``heart_train``, the ``HeartDisease`` column acts as the "ground truth" and indicates whether or not a patient has heart disease. A more comprehensive data dictionary can be found at the end of this README file.

## What this subdirectory contains
This subdirectory contains the work I did individually on the heart disease prediction dataset during the 2024 iteration of the DS3 Hackathon. With the goal of predicting whether a patient has heart disease or not given their medical characteristics, I used decision trees, bagging, random forests, and extreme gradient boosting to train 4 classification algorithms with the ``heart_train`` dataset, where 80% of the data was used for training and 20% was used for testing. Then, I produced predictions for each of the observations found in ``heart_test`` and uploaded them to the corresponding Kaggle competition. These predictions returned the following accuracy scores:
Algorithm | Accuracy Score 
--- | --- 
Decision Tree | 0.8203108 
Bagging | 0.835001
Random Forest | 0.8530977
Extreme Gradient Boosting | 0.8595912

## Data dictionary
- ``Age``: age of the patient [years]
- ``Sex``: sex of the patient [M: Male, F: Female]
- ``ChestPainType``: chest pain type [TA: Typical Angina, ATA: Atypical Angina, NAP: Non-Anginal Pain, ASY: Asymptomatic]
- ``RestingBP``: resting blood pressure [mm Hg]
- ``Cholesterol``: serum cholesterol [mm/dl]
- ``FastingBS``: fasting blood sugar [1: if FastingBS > 120 mg/dl, 0: otherwise]
- ``RestingECG``: resting electrocardiogram results [Normal: Normal, ST: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV), LVH: showing probable or definite left ventricular hypertrophy by Estes' criteria]
- ``MaxHR``: maximum heart rate achieved [Numeric value between 60 and 202]
- ``ExerciseAngina``: exercise-induced angina [Y: Yes, N: No]
- ``Oldpeak``: ST [Numeric value measured in depression]
- ``ST_Slope``: the slope of the peak exercise ST segment [Up: upsloping, Flat: flat, Down: downsloping]
- ``HeartDisease``: output class [1: heart disease, 0: Normal]
