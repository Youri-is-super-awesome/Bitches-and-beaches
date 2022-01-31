# Pawn Patrol
This is the repository for the machine learning project of AI.
The topic of the project is Housing prices and how to predict these prices for new houses. 

# Short description of the project
This application estimates the value of houses in Ames, Iowa, using 79 explanatory variables. The dataset is fairly small, with only 1460 training samples. The 79 features in the dataset are a mix of categorical and numerical features.

There are 5 milestones of this project, assigned with M-number- at the end of the filenames.

M1: The main focus of milestone 1 was the preprocessing of the data. The data was cleaned, rescaled and tranformed to the correct format for later use in the regression models. A simple first model for the lineair regression was build as well. This model was created with only two features of the cleaned data: General Living Area and Overall Quality. 

M2: After the linear regression model, the polynomial model was made to improve the results of the first model. This version included 11 numeric features.

M3: In the third milestone, the cleaning data part was improved to get the most important features out of the dataset to get better predictions in the polynomial model.

M4: In the fourth stage of the project, there are some whole new models created: Neural Networks (NN). There is a simple NN with only one layer and there is a NN based on a tuner, who picks the best model that fits with your data. This model is rebuild in the 'complex NN'. 

M5: In this final stage of the project, the feature selection is improved with a seperote code that checks the influence of each feature sperately on the performance of the last model. New features are created based on combinations of other features and added to the model as well. The neural network is modified to work on 3 different datasets: cleaned data (M1), feature filtered data (M3) and the best features data (M5). This allowed us to compare the different effects the earlier data processing steps have on the model.

# How to run the project

#### The regression model:
  1. Run the preprocessing_M2 file, but set the boarder value of the variable 'relevent_num_features' on 0.7 to get the two strongest correlated features (General Living Area and Overall Quality).
  2. Now run the regression model itself to see what the results are of the model.

#### The polynomial model:
  1. Run preprocessing_M2 again, but with the boarder value on 0.5 to get more features.
  2. Run polynomial_model_M2 with the 11 numeric features

#### The Neural Network models:
  1. Run preprocessing_clean_M5 to generate a cleaned data file. Run ones with get_dummies set on True and False.
  2. Run preprocessing_featureselection_M5 to generate a feature filtered data file. Run ones with get_dummies set on True and False. The correlation treshold can be adjusted to own preference. (Lower means more features will be selected.)
  3. Run test_features_M5 to generate a best feature data file. You can adjust the number of best features to own preference. Our advise is to set it between 10 and 20. Set export on True if you want to save the filtered datafile with only the best features. 
  4. Run the Neural Network with NN_tuner_M5. If it is the first run, set search_best_model on True to let Keras Tuner search for the best model. For the next time, you can set build the best found model in the function build_NN and set search_best_model on False: the program will then reuse this best model instead of searching for a new one. The neural network will run three seperate gradient descents for the clean data, feature filtered data and the best features data. 

# Special credits
Youri Hemelaar, Jenny Eder, Sien Jansen, Agnes Admiraal
