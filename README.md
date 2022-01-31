# Pawn Patrol
This is the repository for the machine learning project of AI.
The topic of the project is Housing prices and how to predict these prices for new houses. 

# Short description of the project
The application can predict housing prices according to new samples (houses) he gets. The models that are created are using the AmesHouses dataset to learn these models. There are 5 different sections/stages in the project, assigned with M-number- at the end of the filenames. 
The first stage (M1) is the also the first model that was build. It is a linear regression model, based on the cleaned data. 
After the linear regression model, the polynomial model (M2) was made to improve the results of the first model. 
In the third section, the cleaning data part was improved to get the most important features out of the dataset to get better predictions in the previous section. It is also possible to clean the data for the already splitted test and training data from Kaggle.
In the fourth and final stage of the project, there are some whole new models created: Neural Networks (NN). There is a simple NN with only one layer and there is a NN based on a tuner, who picks the best model that fits with your data. This model is rebuild in the 'complex NN'. 

# How to run the project
#### The regression model:
  1. Run the preprocessing_M2 file, but set the boarder value of the variable 'relevent_num_features' on 0.7 to get two features          that has the best correlation.
  2. Now run the regression model itself to see what the results are of the model.

#### The polynomial model:
  1. Run preprocessing_M2 again, but with the boarder value on 0.5 to get more features.
  2. Run polynomial_model_M2 to check the results 

#### The Neural Network models:
  1. 


# Special credits
Youri Hemelaar, Jenny Eder, Sien Jansen, Agnes Admiraal
