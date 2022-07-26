# Bank-Marketing

Used a Portugese Bank's marketing data to classify marketing campaigns (calls made to customers) as successful or not. Successful is when the customer subscribes to the bank's product as a result of the campaign. The class is very imbalanced.

## Data
Data comes from UCI Machine Learning Repository
Data can be found here: https://archive.ics.uci.edu/ml/datasets/bank+marketing#

## Plots
Plots are not saved separately in this repository because of file size.

## Data Cleanup and Limitations
We only used the first 7 features to build models. Missing data was identified as "unknown". Data was imputed using the mode. The alternative would have been to drop na rows that would have resulted in about 25% data loss. It can be explored as an alternative option.

## Script to run the code
Script can be found under Bank-Marketing/prompt_III.ipynb

## Model
Models tested are limited to the ones learned so far in the program. Current models come from Sci-kit learn package. Dummy Classifier was used to build the baseline model. Future enhancement using more advanced models (such as RandomForest, XGBoost etc.) recommended.

## Finding based on model evaluation and validation
Our model has a test accuracy of approx. 88.74%. We recommend the logisitc regression model with default parameters as it is simple enough and the best performing one in terms of both test accuracy and time to train the model. KNN with 47 n-neighbors and 'uniform' weights would be the second choice.
This model was adjusted after evaluation but it did not change the outcome. After parameter tuning, the Decision Tree and KNN classification also had very similar test accuracy to the Logistic Regression although the training times were different.

## Future Recommendations
We recommend using all important factors while building the models and not limiting to the first 7 factors as we did here due to perfroamnce limitations of the machine it is being run on. We also recommend using the Grid Search Cv or Randomized Search CV to find the best SVM model, which we could not do here because of performance limitations.
