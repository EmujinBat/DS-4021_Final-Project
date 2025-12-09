# DS-4021---Final-Project

# Hard-Hit Percentage Prediction — MLB Statcast Analysis

## Authors: Emujin Batzorig, Tsion Sahle, Dev Aswani

## Project Overview
This project applies machine learning methods to predict a baseball player’s **Hard-Hit Percentage**, a key Statcast metric representing the percentage of batted balls hit at **95 mph or higher**. Because Hard-Hit % strongly correlates with offensive success and future power development, teams can use this prediction task to identify emerging hitters and quantify the underlying quality of contact.

We trained and compared four predictive models:
- **Penalized Ridge Regression**
- **Support Vector Machine**
- **Random Forest Ensemble**
- **PyTorch Neural Network**

Performance was evaluated using **5-fold cross-validated R²** and **Mean Squared Error (MSE)**.

---

## Summary of Results
All four models performed strongly on this dataset, indicating that the included Statcast features have high predictive value for Hard-Hit %. Ridge Regression achieved the **best overall performance**, suggesting that the relationship between swing outcomes and hard-hit percentage is mostly **linear**. Neural Networks and SVMs performed competitively but showed no improvement over simpler models. The Random Forest model achieved slightly weaker accuracy, indicating that tree-based methods may struggle modeling the smoother, continuous statistical relationships within the features.

Because the models performed similarly, this reinforces that hitters’ power indicators (e.g., barrel %, launch angle, exit velocity) are highly informative and linearly related to hard-hit performance.

---

## Software and Platform Requirements
To run the project notebooks, the following tools and libraries are required:
Python 3.8 or above
Jupyter Notebook or JupyterLab
Operating System: Compatible with MacOS, Windows, or Linux
Required Python Packages:
pandas — data manipulation
numpy — numerical computing
scikit-learn — model training + evaluation
matplotlib & seaborn — data visualization
PyTorch — neural network implementation

## Repository Structure

├── data/                                                                                                                                                                           
│ └── training_set.csv                                                                                                                                                              
│ └── test_set.csv                                                                                                                                                                  
│                                                                                                                                                                                   
├── notebooks/                                                                                                                                                                      
│ ├── 01_EDA.ipynb                                                                                                                                                                  
│ ├── 02_Ridge_Regression.ipynb                                                                                                                                                     
│ ├── 03_SVM_Model.ipynb                                                                                                                                                            
│ ├── 04_RandomForest.ipynb                                                                                                                                                         
│ ├── 05_NeuralNetwork.ipynb                                                                                                                                                        
│ └── 06_Final_Testing.ipynb                                                                                                                                                        
│                                                                                                                                                                                   
├── outputs/                                                                                                                                                                        
│ ├── plots                                                                                                                                                                         
│                                                                                                                                                                                   
├── report.pdf # Final written report submission                                                                                                                                    
└── README.md # Project overview                                                                                                                                                                   
