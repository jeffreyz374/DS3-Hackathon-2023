# Celestial Prediction
## About the data
The ``celestial_train`` and ``celestial_test`` datasets each contain 50,000 rows, where each row corresponds to a celestial body and each column corresponds to an astronomical feature of that celestial body, such as its redshift. In the case of ``celestial_train``, the ``class`` column acts as the "ground truth" and classifies the celestial body either as a galaxy, a star, or a quasar. A more comprehensive data dictionary can be found at the end of this README file.

## What this subdirectory contains
This subdirectory contains the work I did individually on the celestial prediction dataset during the 2023 iteration of the DS3 Hackathon. With the goal of predicting whether a celestial body is a galaxy, a star, or a quasar given its astronomical features, I used decision trees, bagging, random forests, and extreme gradient boosting to train 4 classification algorithms with the ``celestial_train`` dataset, where 80% of the data was used for training and 20% was used for testing. Then, I produced predictions for each of the observations found in ``celestial_test`` and uploaded them to the corresponding Kaggle competition. These predictions returned the following accuracy scores:
Algorithm | Accuracy Score 
--- | --- 
Decision Tree | 0.9688396 
Bagging | 0.971105 
Random Forest | 0.9711846 
Extreme Gradient Boosting | 0.9715283

## Data dictionary
Columns
- ``id``: Object Identifier, the unique value that identifies the object in the image catalog used by the CAS.
- ``alpha``: Right Ascension angle (at J2000 epoch).
- ``delta``: Declination angle (at J2000 epoch).
- ``u``: Ultraviolet filter in the photometric system.
- ``g``: Green filter in the photometric system.
- ``r``: Red filter in the photometric system.
- ``i``: Near Infrared filter in the photometric system.
- ``z``: Infrared filter in the photometric system.
- ``run_ID``: Run Number used to identify the specific scan.
- ``rerun_ID``: Rerun Number to specify how the image was processed.
- ``cam_col``: Camera column to identify the scanline within the run.
- ``field_ID``: Field number to identify each field.
- ``spec_obj_ID``: Unique ID used for optical spectroscopic objects (this means that 2 different observations with the same spec_obj_ID must share the output class).
- ``redshift``: redshift value based on the increase in wavelength.
- ``plate``: plate ID, identifies each plate in SDSS.
- ``MJD``: Modified Julian Date, used to indicate when a given piece of SDSS data was taken.
- ``fiber_ID``: fiber ID that identifies the fiber that pointed the light at the focal plane in each observation.
- ``class``: object class (GALAXY: a galaxy, STAR: a star, QSO: a quasar object).
