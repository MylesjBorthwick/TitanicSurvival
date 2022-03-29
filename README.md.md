  
  # Titanic Prediction ( Kaggle Competition)
  
  ### Author: Myles Borthwick
  
  ### Background
  
The dataset for analysis is taken from the Kaggle Competition "Titanic: Machine Learning From Disaster". The data is split into two sets    training and test. In the training set Survivability is the target to predict with 0's for Died and 1's for Survived. After training the    models with the training set feautres, the test set's survivability can then be predicted.
The training feature set was encoded with OneHotEncoder after rigourous preprocessing and feature analysis.
RandomForestClassifier, GradientBoostingClassifier, SVC, LogisticRegression and GaussianNB were all scored with the training data. Out of the five, RandomForest, GBC and SVC where found to be the best performers. Each of the three top performers were further tuned with GridSearchCV. Finally the best model was used to predict on the data test.csv.
  
  ### Requirements
  
The following package installations are required to run this project:
  
  - numpy
  - pandas
  - matplotlib.pyplot
  - seaborn
  - sklearn
  
  ### How to Run
  
The notebook is set up to run through all of the code, simply run all cells and browse the procedures and visualizations that allowed me  to arrive at my final result. The above packages are required to run these cell's. For the best results use the most updated versions of these packages. Make sure to have all necessary csv datafiles in the same folder as the notebook. They are currently in the right spot for the data to load in. Finally, for the last cell where the prediction is output to csv, either delete the current file named      'submission.csv' from the folder or rename the output csv in the code.
  
  
  ### Results
  
Through testing different models, I found RandomForestClassifier to be the best performer. After tuning my model with GridSearchCV it      achieved a mean training score (average precision) of 0.931 and a mean test score of 0.851. With this model I predicted that around 66%   of the passengers in the test set would not have survived based on their:
  
  - Age Group
  - Sex 
  - Passenger Class
  - Port of Embarkment
  - Number of Siblings, Parents and Children also on board
  - Ticket Fare Price Range
  
The highest predictors for determining survial after applying my model to the test set seem to be Sex, Age and Passenger Class/Ticket Fare range. This lines up with intuition and the effects we can see when evalutating the training set's features.

Overall I am quite happy with this model however I am sure further tuning could increase it's performance. The main difficulties I encountered in this project had to do with preprocessing the data to feed it into my models. Slight differences in the test.csv and training.csv also proved to be a challenge but I was able to overcome these problems through further feature inspection. 
Following my prediction, I decided to adjusted the threshold to see the model perform with no false survival predictions. Although not necessarily useful it was cool to see how we could attain high recall for survival reporting.
  
  
  ### Reflection
  
This was a great challenge and showed me how intense/important preprocessing data for machine learning models can be. This project reinforced my ability to train and test classification models and was an exciting first to be able to compete in a Kaggle competition.
  
