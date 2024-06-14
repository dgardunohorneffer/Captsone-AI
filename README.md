![Opening Pic](https://github.com/dgardunohorneffer/Captsone-AI/blob/main/Data/heartdiseasestock.jpg)

# Beep, Beep, Beep: Detecting Heart Disease

Throughout the world, there are many people who are plagued with diseases, one in particular: cardiovascular disease. The dataset that was used in this project includes patient information, descriptions of their condition, and if the patient has heart disease. This project helps physicians detect heart disease more efficiently by using this tool. The models used in this project were Logistic Regression, Random Forest, and XG Boost, and after evaluating each model for its accuracy, error, and precision, the model that showed the best results was XG Boost. 

## Data
Our model includes mulitple features:
1. Age: age of the patient [years]
2. Sex: sex of the patient [M: Male, F: Female]
3. ChestPainType: chest pain type [TA: Typical Angina, ATA: Atypical Angina, NAP: Non-Anginal Pain, ASY: Asymptomatic]
4. RestingBP: resting blood pressure [mm Hg]
5. Cholesterol: serum cholesterol [mm/dl]
6. FastingBS: fasting blood sugar [1: if FastingBS > 120 mg/dl, 0: otherwise]
7. RestingECG: resting electrocardiogram results [Normal: Normal, ST: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV), LVH: showing probable or definite left ventricular hypertrophy by Estes' criteria]
8. MaxHR: maximum heart rate achieved [Numeric value between 60 and 202]
9. ExerciseAngina: exercise-induced angina [Y: Yes, N: No]
10. Oldpeak: oldpeak = ST [Numeric value measured in depression]
11. ST_Slope: the slope of the peak exercise ST segment [Up: upsloping, Flat: flat, Down: downsloping]
12. HeartDisease: output class [1: heart disease, 0: Normal]

Our complete data set can be seen in: (https://www.kaggle.com/datasets/yasserh/heart-disease-dataset)

## Project Overview
1. Business Understanding
2. Data Understanding
3. Data Preparation
5. Modelling
6. Evaluation

## Business Understanding and Data Understanding

In the competitive healthcare sector, especially in cardiovascular care, providers aim to stand out by delivering excellent patient outcomes and innovative care management. According to World Health Organization, Cardiovascular Diseases (CVDs) are the leading cause of death globally and with early detection, patients can receive medication and counselling to prevent more symptoms and physicians can use this tool as a guide to detect the disease early on. Effective detection and management are crucial for both patient health and the success of healthcare institutions. The image below is a comparison of the leading diseases in the world and CVDs are listed at the top. 
 
![Graph 1](https://github.com/dgardunohorneffer/Captsone-AI/blob/main/Data/download.jpeg)

https://www.who.int/news-room/fact-sheets/detail/cardiovascular-diseases-(cvds)

![Graph 2](https://github.com/dgardunohorneffer/Captsone-AI/blob/main/Data/Picture1.jpg)
 
After doing a deep dive of the data, Age, Old Peak, and Maximum Heart have a high correlation to heart disease, which are factors physicians should consider when detecting heart disease for patients. 

## Data Preparation
1. Divided the target variable and the features
2. Splitted the data into training and testing sets
3. Created a function and a pipe line to return a standarized data frame.
4. Use one hot encoder to deal with categorical columns
5. Used standard scaler to scale our data
   
## Model and Evaluation

Our solution utilized logistic regression, random forest and XGBoost models. Each one was first ran with their default parameters. Each model was then independently tuned for their hyperparameters, with an emphasis on recall score. Feature selection was then used to narrow down the solution to the most important variables. After tuning and feature selection, ROC/AUC curves were calculated alongside a confusion matrix to determine the best model. XGBoost’s recall score was the highest, and thus the choice for our group as the best model. Recall score was chosen over accuracy, as in a medical problem, it is more important to minimize false negatives over false positives.


## Repository Navigation

Each Jupyter notebook contains the code created by each member. The final notebook merges the work of all team members and includes a brief description of the project.
The repository is structured as follows:
*	notebooks/:
    *	Alex_Doytchinov/: Jupyter notebook with code from Alex Doytchinov, team member 1. Notebook_Alex.ipynb
    *	Azi_Arezi/: Jupyter notebook with code from Azi Arezi, team member 2. Notebook_Azi.ipynb
    *	Daniela_Garduno/: Jupyter notebook with code from Daniela Garduno, team member 3. Notebook_Daniela.ipynb
    *	Hinal_Patel/: Jupyter notebook with code from Hinal Patel, team member 4. Notebook_Hinal.ipynb
    *	Final Project:  Jupyter notebook containing all the code from each individual member.
        *	Final_notebook.ipynb
        *	xg_boost.pickle (Trained model, we dont need to train the model once again, the best model has been saved)

      
*	data: Contains the data used in the project.
    *	Heart.csv


