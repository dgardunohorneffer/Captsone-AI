# Beep, Beep, Beep: Detecting Heart Disease

Throughout the world, there are many people who are plagued with diseases, one in particular: cardiovascular disease. The dataset that was used in this project includes patient information, descriptions of their condition, and if the patient has heart disease. This project helps physicians detect heart disease more efficiently by using this tool. The models used in this project were Logistic Regression, Random Forest, and XG Boost, and after evaluating each model for its accuracy, error, and precision, the model that showed the best results was XG Boost. 

## Business Understanding and Data Understanding

In the competitive healthcare sector, especially in cardiovascular care, providers aim to stand out by delivering excellent patient outcomes and innovative care management. According to World Health Organization, Cardiovascular Diseases (CVDs) are the leading cause of death globally and with early detection, patients can receive medication and counselling to prevent more symptoms and physicians can use this tool as a guide to detect the disease early on. Effective detection and management are crucial for both patient health and the success of healthcare institutions. The image below is a comparison of the leading diseases in the world and CVDs are listed at the top. 
 
![Graph 1](https://github.com/dgardunohorneffer/Captsone-AI/Data/download.jpeg)

https://www.who.int/news-room/fact-sheets/detail/cardiovascular-diseases-(cvds)

 
After doing a deep dive of the data, Age, Old Peak, and Maximum Heart have a high correlation to heart disease, which are factors physicians should consider when detecting heart disease for patients. 

## Model and Evaluation

Our solution utilized logistic regression, random forest and XGBoost models. Each one was first ran with their default parameters. Each model was then independently tuned for their hyperparameters, with an emphasis on recall score. Feature selection was then used to narrow down the solution to the most important variables.
After tuning and feature selection, ROC/AUC curves were calculated alongside a confusion matrix to determine the best model. XGBoost’s recall score was the highest, and thus the choice for our group as the best model. Recall score was chosen over accuracy, as in a medical problem, it is more important to minimize false negatives over false positives.

## Repository Navigation

Each Jupyter notebook contains the code created by each member. The final notebook merges the work of all team members and includes a brief description of the project.
The repository is structured as follows:
•	notebooks/:
o	Alex_Doytchinov/: Jupyter notebook with code from Alex Doytchinov, team member 1.
Notebook_Alex.ipynb
o	Azi_Arezi/: Jupyter notebook with code from Azi Arezi, team member 2.
Notebook_Azi.ipynb
o	Daniela_Garduno/: Jupyter notebook with code from Daniela Garduno, team member 3.
Notebook_Daniela.ipynb
o	Hinal_Patel/: Jupyter notebook with code from Hinal Patel, team member 4.
Notebook_Hinal.ipynb

o	Final Project:  Jupyter notebook containing all the code from each individual member
Final_notebook.ipynb
xg_boost.pickle (Trained model, we dont need to train the model once again, the best model has been saved)
•	data: Contains the data used in the project.
o	Heart.csv


