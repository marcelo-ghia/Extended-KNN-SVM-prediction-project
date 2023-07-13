# Extended-KNN-SVM-prediction-project

In this project, you have to predict the probability of death of a patient that is entering an ICU (Intensive Care Unit).

The dataset comes from MIMIC project (https://mimic.physionet.org/). MIMIC-III (Medical Information Mart for Intensive Care III) is a large, freely-available database comprising deidentified health-related data associated with over forty thousand patients who stayed in critical care units of the Beth Israel Deaconess Medical Center between 2001 and 2012.

Each row of mimic_train.csv correponds to one ICU stay (hadm_id+icustay_id) of one patient (subject_id). Column HOSPITAL_EXPIRE_FLAG is the indicator of death (=1) as a result of the current hospital stay; this is the outcome to predict in our modelling exercise. The remaining columns correspond to vitals of each patient (when entering the ICU), plus some general characteristics (age, gender, etc.), and their explanation can be found at mimic_patient_metadata.csv.

Note that the main cause/disease of patient condition is embedded as a code at ICD9_diagnosis column. The meaning of this code can be found at MIMIC_metadata_diagnose.csv. But this is only the main one; a patient can have co-occurrent diseases (comorbidities). These secondary codes can be found at extra_data/MIMIC_diagnoses.csv.

As performance metric, you can use AUC for the binary classification case, but feel free to report as well any other metric if you can justify that is particularly suitable for this case.

Main tasks are:

Using mimic_train.csv file build a predictive model for HOSPITAL_EXPIRE_FLAG .
For this analysis there is an extra test dataset, mimic_test_death.csv. Apply your final model to this extra dataset and generate predictions following the same format as mimic_kaggle_death_sample_submission.csv. Once ready, you can submit to our Kaggle competition and iterate to improve the accuracy.