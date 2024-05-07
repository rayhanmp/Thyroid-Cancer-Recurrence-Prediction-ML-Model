# Thyroid Cancer Recurrence Prediction ML Model
This project aims to develop a model that can reliably predicts cancer recurrence based on patient's data. In this model, we will test various algorithms ranging from decision tree algorithms like Random Forest to ANN-based model.


## ⚙ Tools 
Made using Python with various libraries, such as TensorFlow, Keras, SKLearn, Catboost, IMBLearn, Matplotlib, Pandas, and Seaborn.

## 🎯 Success Criteria 
For this project, there are five major success criteria that we will try to achieve:
1.  Accuracy => 85%
2.  Recall >= 85%
3.  AUC-ROC Score >= 80%
4.  F1 Score >= 80%

## Steps Taken
1. Try to gain insights from the data by using various data visualisation methods, but the most important one here is the **heatmap correlation matrix**. We then test whether the two variables are independent/dependent to each other using **Chi-Square Test**.
2. Afterward, do data preparation: since the data is categorical, we need to **encode it using SKLearn Label Encoder**. Also, use **MinMaxScaler** to scale the Age value. Last but not least, **split the data** into two sets (training and validation dataset) and **augment the training dataset using SMOTE** to try to balance the data.
3. Train various classical ML model using **SKLearn** and **Catboost**, then tune the hyperparameters using **GridSearchCV** to make the process more efficient.
4. Make the **ANN** model using **TensorFlow** and tune the **hyperparameter**.
5. **Evaluate each model** to see whether they pass the success criteria.

## Results
| Model | Accuracy | Recall | F1-Score | AUC-ROC |
|-|-|-|-|-|
| KNN | 0.904348 | 0.78125 | 0.819672 | 0.866529 |
| RF | 0.965217 | 0.96875 | 0.939394 | 0.966303 |
| Adaboost | 0.947826 | 0.96875 | 0.911765 | 0.954255 |
| GBoost | 0.956522 | 0.96875 | 0.925373 | 0.960279 |
| Catboost | 0.956522 | 0.96875 | 0.925373 | 0.960279 |
| ANN | 0.930435 | 0.90625 | 0.878788 | 0.967244 |

Based on the table above, we can conclude that `Random Forest` is the best model we have. All models except KNN passed the success criteria; KNN failed to meet the minimum recall score.
## ❤ Acknowledgment 
Dataset was acquired from [Kaggle](https://www.kaggle.com/code/vizeno/thyroid-cancer-prediction-recurrence-eda-ann) by [Joakim Arvidsson](https://www.kaggle.com/joebeachcapital).
